# Softpatching

A patch is a file containing a number of modifications to an original ROM, which may be bug fixes, hacks or, more generally, translations. Patches come in various formats: `.UPS` (Universal Patching System), `.IPS` (International Patching System), `.BPS` (Binary Patch Support)...

Softpatching is a function for applying these game patches, without having to modify the original rom. This allows you to define when you want to apply available patches and when you don't.

## Installing patches

Patches can be applied in 3 different ways. Depending on which method you choose, you'll need to select the corresponding option in the RetroBat menu:

<figure><img src="https://i.imgur.com/EGOj6hU.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://i.imgur.com/iAzzbbP.png" alt=""><figcaption></figcaption></figure>

* Patch in the corresponding roms directory
  *   The patch file is placed next to the rom. The patch must be named exactly like the rom (except for the extension).

      > Select the AUTO option in the Softpatching menu
* Patch in a sub-directory named `“patches”.`
  *   In the system, a patches sub-directory contains patches for the various games. They are named after the roms for which they are intended.

      > Select the PATCH IN PATCH FOLDER option in the Softpatching menu
* Patch in a folder named after the game
  *   In the system, a subdirectory is named like the game. It can then contain different patches, all of which will be applied (subject to compatibility).

      > Select the PATCH TO FOLDER BY GAME option in the Softpatching menu.

## Compatible cores

This feature will only work for the following libretro cores: \
\
**Bandai - WonderSwan/Color**\
Mednafen\_wswan&#x20;

**Coleco - ColecoVision**\
Gearcoleco&#x20;

**Nec - PC Engine/TurboGrafx-16** \
Mednafen\_pce - Mednafen\_pce\_fast

**Nintendo - Game Boy / Color**\
Gambatte - Mesen - mGBA - TGB Dual - VBA-M

**Nintendo - Game Boy Advance**\
Meteor - mGBA - VBA-M - VBA Next

**Nintendo - NES / Famicom**\
bnes - FCEUmm - Mesen - Nestopia UE - QuickNES

**Nintendo - Satellaview**\
Mesen-S - Snes9x

**Nintendo - SNES / Famicom**\
bsnes - bsnes HD Beta - bsnes JG - bsnes mercury accuracy - bsnes mercury balanced - mednafen\_snes - Mesen-S

**Nintendo - Nintendo 64**\
mupen64plus - parallel

**Sega - Master System**\
SMS Plus GX - Gearsystem

**Sega - MegaDrive / Genesis**\
Genesis Plus GX - Picodrive

**SNK - Neo Geo Pocket / Neo Geo Pocket Color**\
Mednafen\_ngp

