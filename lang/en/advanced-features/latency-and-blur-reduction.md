# Latency Reduction

## Latency Reduction settings

This function can be used to reduce the inherent built-in amount of lag that each game has and can also help to compensate fore input display lag.
It's a function that only applies to Retroarch systems.

To reduce the lag to its minimum, one can pause emulation, press and hold a direction on the controller and advance emulation frame by frame until the character moves.
The frames of lag are the amount of frames advanced - 1.
Beware that the higher the number of frames you are going to run ahead of emulation, the higher demands it places on your CPU.

Many of the cores do not leave audio emulation in a clean state after loading state, so you could get buzzing. 
Using Two-Instance mode makes the primary core not do any load states and avoids that.

Preemptive Frames is a more modern way to achieve the same result than Run-ahead with less computing power needed.
It's normally faster but it is game or system dependant.

More information are available [in the libretro docs](https://docs.libretro.com/guides/runahead/) used as reference for this wiki page.
