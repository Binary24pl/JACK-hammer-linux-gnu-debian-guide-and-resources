# Debian/APT Half-Life asset manager instalation guide

## Get installer
You can get a *.deb installer* in **this very *[repository](./resources/installers/)*** at ***(repo root)/guide/resources/installers*** ; or you may want to download it from the ***[official releases](https://github.com/SamVanheer/HalfLifeAssetManager/tags)*** - with the latest version being ***[3.0.0](https://github.com/SamVanheer/HalfLifeAssetManager/releases/tag/HLAM-V3.0.0)***.

I will however assume that we are working with 3.0.0 version.

## Resolve dependencies

Now that you got an installer, before you install you should resolve some dependencies.

You can do it manually or through an APT manager.

For manual resolving check a ***[non-debian tutorial](./HLAM-ND.md)*** at *`resolve dependencies`* step.

As for APT manager, here it is how it goes:

### Install opengl2

Use command:
```sh
sudo apt -y install glmark2
```

### Instal Qt5

Use command:
```sh
sudo apt install qtbase5-dev
```

## Using the installer

In your terminal, go to the directory where you store your hlam .deb file.

Then enter this command:
```sh
sudo apt install ./halflifeassetmanager_<version>_amd64.deb
```

- *Don't forget to replace **\<version\>** with whatever version you are running for Half Life asset manager.*