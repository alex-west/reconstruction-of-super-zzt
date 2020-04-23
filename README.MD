# The Reconstruction of Super ZZT

This is a personal fork of the Reconstruction of Super ZZT, which is a reverse-engineered recreation of the source code to the last official release of Super ZZT, Super ZZT 2.0.

## Features

- Wider viewport
  - Video mode is still 40 columns, but the viewport is now 36 columns wide, instead of 24.
  - HUD is now a single row above the viewport.
  - The Z-counter name, Z-counter amount, and timer are displayed below the viewport, if they are defined for the board/world.
- Editor is accessible without using a command-line switch
- Adjustable game speed (press S on the title screen)
  
## Planned Features

- Support for user-made splash screens
- Minor editor enhancements
- New cheats

## Directory structure

* **BIN** - output directory for EXE and TPU files,
* **DIST** - output directory for the binary distribution,
* **SCREENS** - 80x25 .BIN screen video data for graphical screens used in Super ZZT,
* **SRC** - the reconstructed Super ZZT source code,
    * **SUPERZ.PAS** - main source file,
* **TOOLS** - tools used when building:
    * **BIN2PAS.PAS** - BIN2PAS, a tool for converting binary files into Pascal units,
    * **CSIPACK.PAS** - CSIPACK, a tool for compressing and decompressing Crunched Screen Images,
    * **LZEXE.EXE** - LZEXE, a .EXE compression tool by Fabrice Bellard,
* **BUILD.BAT** - source code build script,
* **LICENSE.TXT** - licensing terms for the source code release.

## License

The Reconstruction of Super ZZT is licensed under the terms of the MIT license as described in LICENSE.TXT, with the exception of certain files included with this release:

* **TOOLS/LZEXE.DOC**, **TOOLS/LZEXE.EXE**:

```
    LZEXE.EXE v0.91    (c) 1989 Fabrice BELLARD

    Ce programme fait parti du domaine public (FREEWARE),  donc vous pouvez
  l'utiliser, le copier et le distribuer sans problème. Et vous pouvez même
  en faire un usage commercial, c'est à dire compacter des fichiers EXE que
  vous allez vendre. Mais la vente de LZEXE.EXE est interdite.
```

## Compiling

### Requirements

* DOS-compatible environment (f.e. DOSBox),
* Turbo Pascal 5.5 (if you don't have it, it's officially available for free via Embarcadero's Antique Software website).

### Instructions

1. Ensure that TPC.EXE from Turbo Pascal is available on your PATH (f.e. `SET PATH=C:\TP;%PATH%`).
2. From the source code directory, run `BUILD.BAT`.
3. The DIST directory will contain files comprising the release as outlined in the FAQ.