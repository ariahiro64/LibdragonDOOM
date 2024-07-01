---------------
-64DOOM README-
---------------


Updated 2023/05/21


-------------------------
-git repository contents-
-------------------------

`README.md` is this file

`src` directory contains all 64Doom C source, header files, menu graphics and Makefile used to build 64Doom

`doc` directory contains many text files including

`  ORIGINAL_README.TXT` is the original `README.TXT` from the 1990s DOOM open source release
  
`  DOOMLIC.TXT` is the DOOM open source license documentation
  
`  CREDITS.TXT` which provides attribution for various components and code contributors
  
`  LICENSE_generic-hashtable.TXT`, `README_generic-hashtable.TXT` required attribution for Hashtable implementation used
  
`  GPLV3.TXT` is a copy of the GPL V3 License as required

--------------
-how to build-
--------------
Setup libdragon UNSTABLE branch: https://github.com/DragonMinded/libdragon/wiki/Installing-libdragon

Get a copy of a supported version of Doom (Doom shareware, retail, Ultimate Doom, Doom II, Plutonia, TNT).

Set two variables in the Makefile:

`IWAD_DIRECTORY` -- the path of the directory that contains your IWAD file

`IWAD_PREFIX` -- the actual IWAD filename prefix (one of `DOOM1`, `DOOMR`, `DOOM`, `DOOM2`, `PLUTONIA`, `TNT` - these are case sensitive. Must be uppercase and your wad filename must be uppercase i.e. `DOOM2.WAD`)

And run make.

-----------
-SAVEGAMES-
-----------

64Doom uses the Controller Pak to save and load your game progress from the Save Game / Load Game menu options.

One savegame slot is presented, mapped to a single note on the Controller Pak.

The name of the note is the same as the game version (`$IWAD_PREFIX`) you are playing.

When you save or load a game, you will see a message in the Doom HUD if it is successful:

`SAVED GAME TO MEMPAK`

`LOADED GAME FROM MEMPAK`

Savegames are compressed using the lzfx library. However, the compressed saves are still large relative to the capacity of a fully-formatted Controller Pak. 

In the event that there is not enough free space on the Controller Pak to save the game, you will see a message in the Doom HUD:

`NOT ENOUGH SPACE FOR SAVE (NEED #, HAVE #)`

It is very likely you will see this message if you have notes from other games on your Controller Pak, so it is desirable to play with a dedicated, initially empty
Controller Pak. 

It is possible that there are rare occasions where this may happen even with an empty Controller Pak. 

If it does, kill some more enemies, pick up some more items, try again. :-)

----------
-CONTROLS-
----------

D-PAD UP / ANALOG STICK UP :: move forward

D-PAD DOWN / ANALOG STICK DOWN :: move backward

D-PAD LEFT / ANALOG STICK LEFT :: turn left

D-PAD RIGHT / ANALOG STICK RIGHT :: turn right

L TRIGGER :: strafe left

R TRIGGER :: strafe right

C LEFT :: switch to previous weapon

C RIGHT :: switch to next weapon

C UP :: toggle auto-map

C DOWN :: ENTER key

Z :: toggle run on/off (defaults to on)

A :: shoot

B :: use (open doors, flip switches)

START :: ESCAPE key


Enjoy.
