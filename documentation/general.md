The IC10 chip has the following features:
1. 16 general purpose registers (64-bit signed) labeled r0 through r15
2. 6 device IO registers d0 through d5 connected to physical pins
3. 512 64-bit stack memory values
4. SP stack pointer register
5. RA address register
6. "db" device housing

The IC10 programming language is roughly based on MIPS assembly, with some additional limitations:

The maximum size of an IC10 program is 128 lines and a total of 4096 bytes. Comments count towards both size limits.

The IC10 chip can run ~128 instructions per game tick (~0.5 seconds). If the user does not perform a "yield" instruction at least once every ~128 lines, the game engine will force a yield at a random interval, which could cause unexpected behavior.

A chip is not guaranteed to sleep/yield for an exact amount of time, so timing is mostly limited to rough 0.5 second intervals without additional lag.

Stack memory is persistent to the chip. If you modify the stack of a chip and then replace the code with a new program, the stack values will remain until replaced.

Note: The IC10 chip does not draw any power itself, but the housing it is placed in does. The basic IC housing draws 50W, which can make integrating the IC into another device, such as a gas filtration device, a power saving option.

https://stationeers-wiki.com/IC10