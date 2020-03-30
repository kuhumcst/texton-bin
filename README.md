# texton-bin
Binary executable files used by services in the Text Tonsorium.

These binary executable files are built from source in other GitHub repos.

In this readme, we assuma that the `bin` directory is `/opt/texton/bin`.

## bracmat, bracmat.jar and libbracmat.so.1.0
```bash
git clone https://github.com/BartJongejan/Bracmat.git
```

### bracmat
```bash
cd Bracmat/src/
make
cp bracmat /opt/texton/bin/
```

### bracmat.jar and libbracmat.so.1.0
You need administrator rights for this.

```bash
cd Bracmat/java-JNI/
./compileAndTestJNI.sh
```

