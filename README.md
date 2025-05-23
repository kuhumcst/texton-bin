# texton-bin
Binary files used by services in the Text Tonsorium.

Please make sure that all files in opt\texton\bin are executable
```bash
$> cd opt/texton/bin
$> sudo chmod ugo+x *
``` 
From Text Tonsoriums `bin` folder (/opt/texton/bin), you can create symbolic links to the opt/texton/bin in this repository.

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
```bash
$> wget https://raw.githubusercontent.com/kuhumcst/cstlemma/master/doc/makecstlemma.bash
$> chmod ugo+x makecstlemma.bash
$> ./makecstlemma.bash
$> sudo cp cstlemma/cstlemma /opt/texton/bin/
```

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
$> chmod ugo+x makerepver.bash
$> ./makerepver.bash
$> sudo cp repetitiveness-checker/repver /opt/texton/bin/
```

## rtfreader
```bash
$> wget https://raw.githubusercontent.com/kuhumcst/rtfreader/master/doc/makertfreader.bash
$> sudo chmod ugo+x makertfreader.bash
$> ./makerepver.bash
$> sudo cp rtfreader/rtfreader /opt/texton/bin/
```

## taggerXML
Copy https://github.com/kuhumcst/taggerXML/blob/master/doc/maketaggerXML.bash to your disk and run it.
Copy `taggerXML/taggerXML` to `/opt/texton/bin`.
```bash
$> wget https://raw.githubusercontent.com/kuhumcst/taggerXML/master/doc/maketaggerXML.bash
$> sudo chmod ugo+x maketaggerXML.bash
$> ./maketaggerXML.bash
$> sudo cp taggerXML/taggerXML /opt/texton/bin/
```
