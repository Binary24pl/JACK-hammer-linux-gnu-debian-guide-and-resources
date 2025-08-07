# Assumptions:
I will assume that you followed my location and naming convention for files.

# Instalation and compiling a tools build

## Instalation

Visit TWHL repository of VHLT ***[here](https://github.com/twhl-community/VHLT-V34)***, and unpack it. After that you may open your terminal and go to the VHLT root directory.

```sh
cd <path/to/your/VHLT/localrepository>
```

Now, you want to copy tools that are already *os universal*, for that head to the **tools** directory. And copy listed listed:
- zhlt.wad
- zhlt.fgd

```sh
cd tools
cp zhlt.* <your vhlt binaries directory>/
cd ..
```

Then, it has came time to compile binary tools to linux object format. Head to the **src** and then **zhlt-vluzacn** directory like this.

```sh
cd src/zhlt-vluzacnn/
```

Then proceed to compile tools, with make command.

- *Side note:* Ignore all g++ and gcc warnings, they are irrelevant to the success of compilation

```sh
make
```

After that, you may enter newly created **bin** directory, and copy all its contents.

```sh
cd bin
cp * <your vhlt binaries directory>
```