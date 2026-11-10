# Setup für Teilnehmende

Bitte vor Tag 1 installieren und testen. Wenn etwas nicht klappt, meldet euch vorher, damit wir im Workshop keine Zeit mit Installation verlieren.

## Hardware

- **Windows 10 oder 11.** vvvv läuft nur unter Windows. Mit einem Mac bitte vorher melden.
- **Dedizierte Grafikkarte** (NVIDIA oder AMD). Onboard-Grafik kann zu langsam sein.
- **Zweiter Monitor (Pflicht).** Er dient im Workshop als „Beamer“. HDMI- und DisplayPort-Kabel bereithalten.
- Optional: ein Smartphone für den 3D-Scan an Tag 1.
- Optional: ein Beamer, falls ihr die Übungen auch real ausprobieren wollt.

## Software

1. **vvvv 7.4** herunterladen und installieren: https://visualprogramming.net
2. **NuGet-Pakete** installieren (Kommandozeile im vvvv-Ordner, siehe [Managing NuGets](https://thegraybook.vvvv.org/reference/hde/managing-nugets.html)):
   ```
   nuget install VL.BadMapper -pre
   nuget install VL.Mapper
   ```
3. **Test-Patch** `patches/00_Setup-Test.vl` öffnen. Wenn ein Fenster mit einem sich drehenden Würfel erscheint, ist alles bereit.

## 3D-Scan-App (für die Aufgabe nach Tag 1)

Eine dieser Apps auf dem Smartphone installieren:
- Polycam
- Scaniverse
- KIRI Engine

Export als `.obj`. Optional zum Reduzieren der Polygonzahl: [Blender](https://www.blender.org).
