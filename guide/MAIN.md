# Installing J.A.C.K. on GNU/Linux

## Get installer on your system
Instalation of J.A.C.K. on Linux is as easy as installing one on Windows, main difference is that instalation is completely CLI.

First get installer matching your system architecture.

- **(32-bit filename)**: *jack_\<version\>_linux_x86.run*
- **(64-bit filename)**: *jack_\<version\>_linux_x64.run*
- **(Local repo filepath)**: *[(repo root)/resources/installers](https://github.com/Binary24pl/JACK-hammer-linux-gnu-debian-guide-and-resources/tree/master/resources/installers)*
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

If you don't feel like installing libaudio2 files through *apt manager*, then you can get libaudio2 files ***[here](https://github.com/Binary24pl/JACK-hammer-linux-gnu-debian-guide-and-resources/tree/master/resources/sharedobjects)***, from this repo. And use cp command from whereever you installed those files, or install them directly into the JACK root folder.
- Copy command
```sh
cp libaudio.so.2 ~/JACK
```

- *Side note:* **Remember to choose matching architecture!**

**libaudio2 apt instalation guide: [here](https://github.com/Binary24pl/JACK-hammer-linux-gnu-debian-guide-and-resources/blob/master/guide/LIBA2.md)**