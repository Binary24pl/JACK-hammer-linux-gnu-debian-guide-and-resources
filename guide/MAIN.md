# Installing J.A.C.K. on GNU/Linux

## Get installer on your system
Instalation of J.A.C.K. on Linux is as easy as installing one on Windows, main difference is that instalation is completely CLI.

First get installer matching your system architecture.

- **(32-bit filename)**: *jack_\<version\>_linux_x86.run*
- **(64-bit filename)**: *jack_\<version\>_linux_x64.run*
- **(Local repo filepath)**: *[(repo root)/guide/resources/installers](./resources/installers/)*
- **(External link - homepage of JACK editor)**: *[Download](https://jack.hlfx.ru/en/download.html)* - page
  
Then create a folder for your J.A.C.K. editor files, I recommend to do it at your ***home directory(~)***:
```sh
mkdir ~/JACK
```

Move to directory where you downloaded your installer .run file and ***give execution permission*** through
```sh
chmod +x jack_<version>_linux_<architecture>.run
```

Replace ***\<version\>*** with whatever version of installer you are running, as well as ***\<architecture\>*** to **x86** if you are using 32-bit version, and if you are using 64-bit version change that field to **x64**.

Now let's run that installer.
- *Side note: if you were following my recomendation for JACK directory location, please do not use "sudo" command*
```sh
./jack_<version>_linux_<architecture>.run
```
And when installer will inform you that it is ready, you can enter just "JACK" or whatever directory name you chose to store installed J.A.C.K. editor.

## Solving libaudio2 dependencies
At this point, if your installed J.A.C.K. editor isn't launching, even if you added +x permissions to it just-in-case, this is most probably because J.A.C.K. can't find libaudio2 (**File name: *libaudio.so.2***) shared object file.

- *Side note: libaudio2 isn't required to be anywhere in your system for J.A.C.K. to work, **it only has to be in the root directory of your installed J.A.C.K. files.***

If you don't feel like installing libaudio2 files through *apt manager*, then you can get libaudio2 files ***[here](./resources/sharedobjects/)***, from this repo. And use cp command from whereever you installed those files, or install them directly into the JACK root folder.
- Copy command
```sh
cp libaudio.so.2 ~/JACK
```

- *Side note:* **Remember to choose matching architecture!**

**libaudio2 apt instalation guide: [here](./LIBA2.md)**

## Getting HLAM on your system
- *Side note:* Unfortunately this guide section will only for **64-bit architecture**.
- *Author note:* I will try to find in the future 32-bit architecture solution, or I will link whoever found such

### Even after HLAM repo became archived, only official release is for gnu/linux distros of *debian origin* that use *apt package manager*.
- ### [Debian/apt based instalation guide](./HLAM-OD.md)
- ### [Non-debain/apt based instalation guide](./HLAM-ND.md)

## Getting VHLT tools

First, let us create folder for our binaries and other tools included in VHLT package.

I recommend doing it on your **home directory(~)**, and will refer to directory as *VHLT binaries root directory*. I recommend naming your binaries directory as **bin-vhlt**.

Again we use mkdir on our home directory like that:
```sh
cd ~
mkdir <your chosen name>
```

Once you have done that, you can either download ready for you compiled tools from this repo, or go to the VHLT repository and build tools yourself.

If you chose to use compiled tools from my repo download all the contents **from:*[ (repo root)/guide/resources/compiled_tools](./resources/compiled_tools/)***

And then copy and paste it, do it all from directory where you got compiled tools set installed.
```sh
cp * <your vhlt binaries folder>
```

Or follow my guide on how to build VHLT tools on your own ***[here](./VHLT.md)***.

# The end

Congratulations, you now have all needed assets and tools for proper functionality of J.A.C.K. on debian-like distro of gnu/linux.

All that is left for you is to set up a game profile for GldSrc game of your choice.

For this, I recommend ***[Dimebeak's game profile set up tutorial](https://www.youtube.com/watch?v=sjX96WdY9iE).*** It covers all you need to set up your profile.

*Side notes:*
- *Technical side note: When searching for files and executables in J.A.C.K. you will be forced to use gtk-file-manager. If you can't find hidden directories and files don't worry. Use **CTRL + H**, it will expose all hidden files, and won't translate to main application of file manager.*

- *GTK Custom themes related side note: J.A.C.K. uses gtk library, which means it is gtk-themese complicit, however, custom themes may result in **unresponsive behavior of fill-the-screen** button on title bar of the application. However latest Gnome supports **edge snaping** use that to yeild similar results.*