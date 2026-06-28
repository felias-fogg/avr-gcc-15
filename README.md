# Microchip's AVR-GCC15.1 toolchains

This repo contains copies of the [AVR-GCC 15.1 toolchains built by Microchip](https://www.microchip.com/en-us/tools-resources/develop/microchip-studio/gcc-compilers) for different platforms. Unfortunately, a Linux ARM64 version is missing. Maybe it will be added in the future. The toolchains are intended to be used in connection with **Arduino** and **PlatformIO**. The only differences to the original archives are the addition of a `package.json` manifest and the replacement of AVR-GDB by a mostly statically linked, [patched version (17.1.4)](https://github.com/felias-fogg/avr-gdb). 

Since it has not yet been tested extensively in the Arduino and PlatformIO context, your mileage may vary.  It may well be the case that the new version breaks some existing libraries. I moved to the new version mainly because some of the debugging quirks have been resolved in the last 10 years. What I noticed is:

- The `-mrelax` optimization option works now without playing havoc with the line numbering information (which made debugging impossible).
- Link time optimization does not remove class structure information any longer. 

Please share your experience (positive or negative) here in the [discussion section](https://github.com/felias-fogg/avr-gcc-15/discussions). Bug reports should be posted as an [issue](https://github.com/felias-fogg/avr-gcc-15/issues).