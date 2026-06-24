# Microchip's AVR-GCC15.1 toolchains

This repo contains copies of the [AVR-GCC 15.1 toolchains built by Microchip](https://www.microchip.com/en-us/tools-resources/develop/microchip-studio/gcc-compilers) for different platforms. Unfortunately, ARM64 for Linux is missing. May be it will be added in the future. The toolchains are intended to be used in connection with Arduino and PlatformIO. All archives contain a `package.json` manifest so that they can be used in PlatformIO.

Docs have been removed, and AVR-GDB has been replaced by a [patched version (17.1.4)](https://github.com/felias-fogg/avr-gdb). Otherwise, no patching or other changes have been performed. For obvious reasons, I have not applied the Arduino patches from 8 years ago.

Since it has not yet been tested extensively, your milage may vary. I moved to the new version mainly because some of the debugging quirks have been resolved in the last 10 years. What I noticed is:

- The `-mrelax` optimization option works now without playing havoc with the line numbering information (which made debugging impossible).
- Link time optimization does not remove class structure information any longer. 

Please share your experience (positive or negative) here in the [dicussion section](https://github.com/felias-fogg/avr-gcc-15/discussions). Bug reports should be posted as an [issue](https://github.com/felias-fogg/avr-gcc-15/issues).