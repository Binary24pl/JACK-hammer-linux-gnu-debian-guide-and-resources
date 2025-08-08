# J.A.C.K. hammer gnu linux, on debian-like distros, instalation guide and resources repository.

## Introduction:
This repository contains instalation guide for **J.A.C.K. hammer editor** on debian-like linux distribution(think Debian, Ubunutu, Linux mint, Pop_OS!).

## Content taken under consideration:
We will be basing this guide using **25th-anniversary edition of Half-Life** and as for *GldSrc tools* we will be using for compilation **[Vluzacn's ZHLT v34](https://github.com/twhl-community/VHLT-V34)** and for model viewing we will be using **[SamVanheer's Half-life asset manager](https://github.com/SamVanheer/HalfLifeAssetManager)**.

Further more, we will also take dive into solving dependencies issues that come with **post installed** J.A.C.K. hammer editor, from installer avaible on **[official J.A.C.K. webpage application installers](https://jack.hlfx.ru/en/download.html)**.

## Main guide: *[(goto: MAIN.md)](./guide/MAIN.md)*
- *Main guide structured to contain major steps in simplified manner, each containing link to more detailed sub-guide of each step* 


# Reference list
### Credits:

**JACK hammer authors:**
- Chain studios
- Crystice Softworks
- Community contributors
  
**Vulcan's Half-Life tools:**
- Zoner Half-Life tools author: *Sean "Zoner" Cavanaugh*
- Vluzacn *email: vluzacn@163.com*
- TWHL community: ***[main page](https://twhl.info/)*** ; ***[discord](https://discord.com/invite/NgN6JBu)***

**Half-Life asset manager:**
- SamVanheer *github **[account](https://github.com/SamVanheer)***
  
**J.A.C.K. Game profile set-up**
- Dimbeak: ***[Youtube](https://www.youtube.com/user/Dimbark)*** ; ***[TWHL](https://twhl.info/index.php/user/view/5749)***

**Libsound2 issue solution(my primary search which led to inclusion of dependency issues in this repo for JACK):**
- ***[Github issue thread](https://github.com/ValveSoftware/steam-runtime/issues/709)***
- *Issue reporter:* **[FreeSlave](https://github.com/FreeSlave)**
- *Issue solution contributors:* **[FreeSlave](https://github.com/FreeSlave)** ; **[smcv](https://github.com/smcv)**

### Resources:
- *Installers:* ***[click here](./guide/resources/installers/)*** - includes: *JACK editor's .run file* ; *HLAM .deb file*
- *Linux shared object files:* ***[click here](./guide/resources/sharedobjects/)*** - includes: *libaudio2 so files*(both in 32 and 64 format) ; *opengl2* ; *Qt5 library*
- *Compiled tools for map compilation:* ***[click here](./guide/resources/compiled_tools/)*** - includes: *VHLT compilation tools* ; *ZHLT .wad and .fgd files*

- *Depackaged .deb files: **[click here](./guide/resources/dpkg/)*** - includes: *Half-Life asset manager*

### Todo list:
- ~~As for now (Aug 8 2025) I will be for a day or two working to combine *`master`* and *`hlam-no-deb`* branches.~~ (Done)

- ~~On *`hlam-no-deb`* I will create first scratch of non-debian tutorial for hlam instaletion.~~ (Aborted)

### Change list:

- ***Aug 8 2025:***
    - *`hlam-no-deb`* branch contains all necessary resources to make Half-Life asset manager work on non-debian gnu/linux distros.