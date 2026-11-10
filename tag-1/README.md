# Tag 1 – von 2D nach 3D

## 0:00–0:15 Begrüßung, Setup-Check

Kurze Runde, alle öffnen `patches/00_Setup-Test.vl`.

## 0:15–0:35 Geschichte & Begriffe

- Vorgeschichte: Laterna Magica, Phantasmagorie
- Disney, Haunted Mansion (1969): auf Büsten projizierte Gesichter
- Michael Naimark, *Displacements* (1980)
- Raskar et al., *Shader Lamps* (2001)
- Fassaden-Mapping der 2000er Jahre
- Begriffe: Throw Ratio, Lens Shift, Keystone

## 0:35–0:55 Was ist eine Homographie?

- Schräge Projektion auf eine Ebene erzeugt ein verzerrtes Viereck
- Homographie = 3×3-Matrix, die ein Viereck in ein anderes überführt
- 8 Freiheitsgrade → 4 Punktpaare reichen (Corner Pin)
- Unterschied zum Keystone im Beamer: kostet keine Auflösung, beliebig viele Flächen
- **Merksatz: Eine Homographie stimmt nur für ebene Flächen.**

## 0:55–1:35 Übung 2D-Homographie

Ein Foto aus `assets/photos/` dient als Ersatz für die echte Projektionsfläche.

| Stufe | Patch | Aufgabe |
|---|---|---|
| 1 | `patches/01_Homography_Single.vl` | Ein Video auf eine Wand / ein Plakat im Foto mappen |
| 2 | `patches/02_Homography_Facade.vl` | Mehrere Fenster einer Fassade, gemeinsame Quelltextur |
| 3 | `patches/03_Homography_Cube.vl` | Würfel mit drei sichtbaren Seiten, Kanten- und Lichtanimation |

## 1:45–2:00 Grenzen der Homographie

- Demo: Mapping auf Zylinder / Kugel
- Bezier- und Grid-Warping als Notlösung
- Probleme: nur ein Blickpunkt, viel Handarbeit, bricht bei Bewegung
- Überleitung: Kennt man Geometrie und Projektorposition, rechnet der Computer die Verzerrung

## 2:00–2:45 Virtueller Raum

Patch: `patches/10_VirtualStudio.vl`

- Szene in Stride, OBJ laden (zuerst der Würfel aus Stufe 3)
- Virtueller Projektor mit ProjectorLight
- Zwei Ansichten: Beamer-Ausgabe und Zuschauer-Kamera
- Projektorparameter an einen realen Beamer angleichen

## 2:45–3:00 Aufgabe bis Tag 2

- Ein Objekt mit dem Smartphone scannen (Polycam, Scaniverse, KIRI Engine)
- Als `.obj` exportieren, ggf. in Blender reduzieren
- Mitbringen zu Tag 2
