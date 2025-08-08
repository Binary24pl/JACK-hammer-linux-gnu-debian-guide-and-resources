# Non Debian/APT Half-Life asset manager instalation guide

## Before we begin
I will warn you that this method might not work on all distributions, but with it I have managed to *make it work on redhat-based distros on **OpenSUSE***.

Additionally, install this repository if you haven't already. We will be using files found only in this repository.

**This tutorial will work only for 64bit architecture!**

## Prepare dependencies

First, make sure you have **x86_64-linux-gnu** directory at *`/usr/lib/`*.

For that head to the before mentioned sup-directory.
```sh
cd /usr/lib/
```

Then run `ls` command and *pipe it* to `grep` to filter out the `ls` output, like this:
```sh
ls | grep x86_64-linux-gnu
```

If you are seeing nothing, then it means you need to create such directory.
- Remember to use sudo as you are out of the scope of your home directory
```sh
sudo mkdir x86_64-linux_gnu
```


Then go to the ***[(repo root)/guide/resources/sharedobjects](./resources/sharedobjects/)*** in your terminal. When you find yourself there, we may begin copying of all required dependencies.

I will asume that you are dooing it from this repository's sharedobjects directory.

```sh
sudo cp ./opengl2/64-bit/* /usr/lib/x86_64-linux-gnu
sudo cp ./Qt5-dependencies/64-bit
```

## Inserting depackaged files

With sudo, use cp and follow the paths of the sub-directories at ***[(repo root)/guide/resources/dpkg/hlam/root/](./resources/dpkg/hlam/root/)***, and apply it to your system root **( / )**.

This is how an end result should look like.

```
/
└── usr
    ├── bin
    └── share
        ├── applications
        ├── Half-Life Asset Manager
        │   └── Half-Life Asset Manager
        └── icons
            └── hicolor
                └── 128x128
                    └── apps

```

Verify if you have all the required directories from above, if not - create them.

And here I will provide *bulk `sudo cp`* command for you to use once verify if everything is at place. This command will wokr only if you are at `(repo root)/guide/resources/dpkg/hlam/root`.

```sh
sudo cp ./usr/bin/hlam /usr/bin ; sudo cp ./usr/share/applications/* /usr/share/applications ; sudo cp ./usr/share/Half-Life\ Asset\ Manager/Half-Life\ Asset\ Manager/* /usr/share/Half-Life\ Asset\ Manager/Half-Life\ Asset\ Manager ; sudo cp ./usr/share/icons/hicolor/128x128/apps/* /usr/share/icons/hicolor/128x128/apps
```