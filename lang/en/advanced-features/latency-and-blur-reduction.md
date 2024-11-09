# Latency Reduction

## Latency Reduction settings

This function can be used to reduce the inherent built-in amount of lag that each game has and can also help to compensate fore input display lag.
It's a function that **only applies to Retroarch systems**.

To reduce the lag to its minimum, one can pause emulation, press and hold a direction on the controller and advance emulation frame by frame until the character moves.
The frames of lag are the amount of frames advanced - 1.
Beware that **the higher the number of frames you are going to run ahead of emulation, the higher demands it places on your CPU**.

Many of the cores do not leave audio emulation in a clean state after loading state, so you could get buzzing. 
Using **Two-Instance mode** makes the primary core not do any load states and avoids that.

**Preemptive Frames** is a more modern way to achieve the same result than Run-ahead with less computing power needed.
It should be faster but it is game or system dependant.

More information are available [in the libretro docs](https://docs.libretro.com/guides/runahead/) used as reference for this wiki page.


# Reducing Motion Blur

Black Frame Insertion (BFI) allows the emulator to insert black images between game images to reduce the inherent motion blur of sample-and-hold screens (LCD, QLED and OLED). 
It's a function that **only applies to Retroarch systems**.

This issue was absent on CRTs due to their rolling scan technology and explain why motion appeared smoother.

## Screen Sync settings

The Black Frame Insertion setting in Retrobat follows the graduation of RetroArch so it should be set as follow:
1 - For 120Hz displays
2 - For 180Hz displays
3 - For 240Hz displays
4 - For 300Hz displays
5 - For 360Hz displays
6 - For 420Hz displays
7 - For 480Hz displays
8 - For 540Hz displays
9 - For 600Hz displays
10 - For 660Hz displays
11 - For 720Hz displays
12 - For 780Hz displays
13 - For 840Hz displays
14 - For 900Hz displays
15 - For 960Hz displays

It's important to note that **BFI cannot be set to ON if using the G-sync/Freesync compatibility option** (otherwise known as VRR). 
The VRR option can be very beneficial for games that run at a non-60hz frequency (many arcade games for example) to preserve game timing. 

For such scenarios, advance users can create a CUSTOM resolution in Windows using [Custom Resolution Utility](https://github.com/radamar/Custom-Resolution-Utility-ToastyX) to set as close to the mathematically correct a frequency that is a multiple of the one the game needs. 
For example MK1, 2 and 3 run at around 54.7 FPS, so you need approximately 109.4Hz to work with BFI if using a 120hz monitor and the first setting in Retrobat. **This has to be done on a game-basis**.
