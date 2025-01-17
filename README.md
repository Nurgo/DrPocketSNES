## INTRO

This project is a rework of 7.2.1 available src release, aimed at MiyooCFW compatible devices (armv5).

## What's needed TO be DOne:

- ~~fix ALSA output~~ (credits @tiopex)
- ~~add basic bilinear [upscaler](https://github.com/m45t3r/snes9x2002/blob/b65e88f52329696ce04beef8527ab159bcb56903/shell/scalers/scaler.c#L31) from snes9x2002 codebase.~~
- correct input mapping
- ~~add argument reading for loading ROM file.~~ (credits @tiopex)
- ~~optimize output target~~
- ~~remove redundant settings options.~~

## Future Plans
- move code to pure C
- add quick load/savestate (initLoad, exit, hotkey event)
- savestate sreenshots in saveMenu

## Build steps for MiyooCFW

Docker cross-compilation with uClibc-shared setup:
```sh
git clone https://github.com/Apaczer/DrPocketSNES
cd DrPocketSNES/
docker pull miyoocfw/toolchain-shared-uclibc:latest
docker run --volume ./:/src/ -it miyoocfw/toolchain-shared-uclibc:latest
cd /src
make clean
make
```
It is recommended to use COMPATIBLE build, thus `make comp`
