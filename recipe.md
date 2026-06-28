How to generate a new version:

1. Download platform-specific archives (and maybe sources) from Microchip using **wget** (in order to avoid that quarantine bits are added) to the platform-specific folders.

2. Then go into each platform-specific folder:

      - Unzip/untar the archives.

      - Rename the top-level archive folder to `avr`.

      - Edit `patch/package.json`.

      - Download the newest avr-gdb version from the [AVR-GDB patched repo](https://github.com/felias-fogg/avr-gdb) using **wget** to `patch/bin`

      - `cp -r patch/* avr/`

      - `tar cvzf avr-gcc-15.1.0-microchip4.0.0.52-PATCHLEVEL-PLATFORM.tar.gz avr`

      - `rm -rf avr`

3. Finally, commit all changes and push.

4. Make a new release.

5. Upload the new archives as release assets.

6. Switch to the branch `dummy`.

7. Change `package.json`.

8. Commit and push.



