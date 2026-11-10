# Participant setup

Please install and test everything before day 1. If something doesn't work, get in touch beforehand so we don't lose workshop time on installation.

## Hardware

- **Windows 10 or 11.** vvvv runs on Windows only. If you are on a Mac, please let us know in advance.
- **Dedicated graphics card** (NVIDIA or AMD). Integrated graphics may be too slow.
- **Second monitor (required).** It acts as the "projector" during the workshop. Have HDMI and DisplayPort cables ready.
- Optional: a smartphone for the 3D scan after day 1.
- Optional: a projector, if you want to try the exercises for real.

## Software

1. **vvvv 7.4** – download and install: https://visualprogramming.net
2. **NuGet packages** – install from the command line in your vvvv folder (see [Managing NuGets](https://thegraybook.vvvv.org/reference/hde/managing-nugets.html)):
   ```
   nuget install VL.BadMapper -pre
   nuget install VL.Mapper
   ```
3. **Test patch** – open `patches/00_Setup-Test.vl`. If a window with a spinning cube appears, you're all set.

## 3D scanning app (for the assignment after day 1)

Install one of these apps on your smartphone:
- Polycam
- Scaniverse
- KIRI Engine

Export as `.obj`. Optional, to reduce the polygon count: [Blender](https://www.blender.org).
