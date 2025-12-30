# DosUAE 

With DosUAE you can emulate an Amiga 500 under DOS but also 68020 CPU + FPU, up to 2MB Chip RAM, 8 MB fast RAM and another 1 MB of RAM. You get something like an Amiga 2500 if you all max out. 

The minimal host-system should be a Pentium or Dx PC with an SVGA board and 20 MB disk free space. 

## Key-settings

| Key | Description |
|---|---|
| Esc | exit the settings menu |
| F12 | exit from emulation |
| Page Up, Page Down | These are the two `Amiga` special key |
| Print Screen | dump the current screen to a Targa 24 bits file. |

- The Dithered, Correct On options slow down a lot : better not to be used.
- Use only 256 or 32K colors.
- DosUAE is imcompatible with what need AGA or an MMU.
- All Dos floppies MUST be inserted before doing RUN UAE!

## Amiga-ROM 

Put the KICK.ROM in the same folder with UAE.EXE and rename it to something more specific if you want to use several ROMs, something like KICK31.500 for Kick 3.1 for Amiga 500. 

## Folders 

Put your files in different folders like ADF and HDF so you can better find them. 

**For Workbench 1.3 configure DosUAE something lick that**:

```
DosUAE v.69 - Main Menu                   ________________________________________________ 
_______________________________________   | DF0:- c:/uae/bubble.adf 
RUN UAE!                                  | DF0:-  
Disk settings                             | DF0:-  
Video settings                            | DF0:- 
Memory settings                           |  
Hard Disk settings                        | VIDEO:320*240 256 colors 
Sound settings                            | X centered (clever) Y centered (clever)  
Other settings                            | double on drawing every 5 frame. 
About UAE                                 | Immediate Blits On. 32 bit Blits On 
_______________________________________   | Copper Cheat disabled 
RUN UAE!                                  | GFXLIB replacement Off 
_______________________________________   MEMORY: 512k chip, 0 fast, 512K bogo 
BUILD OPTIONS                             ROM IMAGE: c:/uae/kick.12  
CPU 68000 no FPU                          | SOUND: 0 (Off) 
Fast version                              | 8 bits 11000 Hz 
PC SYSTEM                                 | Buffer: Min 2048 Max 8192 
Physical Mem: 20MB                        | Dont adjust frequency dynamicly 
Virtual Mem: 21 MB                        | JOYSTICK 0 CONFIG: M | JOYSTICK 1 CONFIG: A 
OS: DOS                                   | SERIAL: AUX: (inactive) | PARALLEL: PRN:  
                                          | ACCURACY: 0 | 68K SPEED: 3 
UAE FILESYS VOLUMES                       | HARDDISK: No hard disk file available
```

All other settings should be off

**For a system with Workbench 3.0 or 3.1 use something like this**:

```
DosUAE v.69 - Main Menu                   ________________________________________________ 
_______________________________________   | DF0:- c:/uae/wb31.adf 
RUN UAE!                                  | DF0:- c:/uae/extras.adf 
Disk settings                             | DF0:- c:/uae/locale.adf 
Video settings                            | DF0:- c:/uae/storage.adf 
Memory settings                           |  
Hard Disk settings                        | VIDEO: 640*480 32768 colors 
Sound settings                            | X centered (clever) Y centered (clever)  
Other settings                            | double on drawing every frame. 
About UAE                                 | Immediate Blits On. 32 bit Blits On 
_______________________________________   | Copper Cheat disabled 
RUN UAE!                                  | GFXLIB replacement Off 
_______________________________________   MEMORY: 2048k chip, 8192 fast, 1024K bogo 
BUILD OPTIONS                             ROM IMAGE: c:/uae/kick.30 
CPU 68020/68881                           | SOUND: 0 (Off) 
Fast version                              | 8 bits 11000 Hz 
PC SYSTEM                                 | Buffer: Min 2048 Max 8192 
Physical Mem: 20MB                        | Dont adjust frequency dynamicly 
Virtual Mem: 21 MB                        | JOYSTICK 0 CONFIG: M | JOYSTICK 1 CONFIG: A 
OS: DOS                                   | SERIAL: AUX: (inactive) | PARALLEL: PRN:  
                                          | ACCURACY: 0 | 68K SPEED: 3 
UAE FILESYS VOLUMES                       | HARDDISK: No hard disk file available
DH0: C/UAE/AMIGA.HD - virtual - size 8 
PC0: A:
```

**Hard Disk Settings**: add a virtual volume/Name `DH0`, Path `c:/uae/disque.dur`, Size type Return.
**Hard Disk Settings**: add a normal volume/Name `PC0`, Path `a:`

Then you got a false Amiga hard drive called `DH0:` and a DOS floppy drive called `PC0:` those are standard Amiga names

All other settings should be off.
