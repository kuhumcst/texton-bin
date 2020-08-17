# texton-bin
Binary executable files used by services in the Text Tonsorium.

These binary executable files are built from source in other GitHub repos.

In this readme, we assume that the `bin` directory is `/opt/texton/bin`.

## bracmat, bracmat.jar and libbracmat.so.1.0
```bash
$> git clone https://github.com/BartJongejan/Bracmat.git
```

### bracmat
```bash
$> cd Bracmat/src/
$> make
$> sudo cp bracmat /opt/texton/bin/
```

### bracmat.jar and libbracmat.so.1.0
You need administrator rights for this.

```bash
$> cd Bracmat/java-JNI/
$> ./compileAndTestJNI.sh
```

This script creates the symbolicv links /usr/lib/libbracmat.so and /usr/lib/libbracmat.so.1 and creates the share object /usr/lib/libbracmat.so.1.0.
The script also creates bracmat.jar and attempts to copy it to Tomcat's "lib" folder. This is because bracmat runs as a JNI, its functions being called from the DK-CLARIN java code. 

## cstlemma
Copy https://github.com/kuhumcst/cstlemma/blob/master/doc/makecstlemma.bash to your disk and run it.
Copy `cstlemma/cstlemma` to `/opt/texton/bin/`.

## jsoncat
```bash
$> git clone https://github.com/pantuza/jsoncat.git
```
Follow the instructions in `README.md`. Copy jsoncat to `/opt/texton/bin/`.  

## lapos
`$> git clone https://github.com/cltk/lapos.git`

Follow the build instructions. Copy the executable file `lapos` to `/opt/texton/bin`.

## repver
```bash
$> wget https://raw.githubusercontent.com/kuhumcst/repetitiveness-checker/master/doc/makerepver.bash
$> chmod u+g makerepver.bash
$> ./makerepver.bash
$> cp repetitiveness-checker/repver /opt/texton/bin/
```

## rtfreader
Copy https://github.com/kuhumcst/rtfreader/blob/master/doc/makertfreader.bash to your disk and run it.
Copy `rtfreader/rtfreader` to `/opt/texton/bin`.

## taggerXML
Copy https://github.com/kuhumcst/taggerXML/blob/master/doc/maketaggerXML.bash to your disk and run it.
Copy `taggerXML/taggerXML` to `/opt/texton/bin`.
