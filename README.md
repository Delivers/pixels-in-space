# Pixels in Space

**Projection Mapping & Immersive Setups in vvvv**
Mapping, Edge Blending und Netzwerk-Sync mit Simon Weckert

Online-Workshop im Rahmen des vvvv Intermediates Program Winter 2026/27 am [NODE Institute](https://thenodeinstitute.org/courses/pixels-in-space-projection-mapping-immersive-setups-in-vvvv).

- **Termine:** Dienstag, 8. und 15. Dezember 2026, jeweils 18:00–21:00 CET
- **Format:** zwei Live-Sessions online, Aufzeichnungen bleiben mindestens ein Jahr verfügbar
- **vvvv-Version:** 7.4
- **Ankündigung:** [vvvv Blog](https://vvvv.org/blog/2026/pixels-in-space-projection-mapping-immersive-setups-in-vvvv/)

Vom 16:9-Monitor auf echte Oberflächen und ganze Räume: von der einfachen 2D-Homographie über das Mapping auf 3D-Objekte bis zu Multi-Projektor- und Multi-PC-Setups. Am Ende steht die technische Grundlage für interaktive Installationen, Bühnenbilder und immersive Ausstellungsräume.

Da der Kurs online stattfindet, arbeiten alle in einer virtuellen Szene (Stride), in der Projektoren simuliert und eigene Objekte als `.OBJ` geladen werden. Ein zweiter Monitor dient als Ersatz für den Beamer.

## Ablauf

### Tag 1 – von 2D nach 3D

| Zeit | Block | Inhalt |
|---|---|---|
| 0:00–0:15 | Begrüßung, Setup-Check | vvvv und Pakete laufen bei allen |
| 0:15–0:35 | Geschichte & Begriffe | Laterna Magica, Haunted Mansion (1969), *Displacements* (1980), *Shader Lamps* (2001), Fassaden-Mapping. Throw Ratio, Lens Shift, Keystone |
| 0:35–0:55 | Was ist eine Homographie? | 3×3-Matrix, 8 Freiheitsgrade, 4 Punktpaare, nur für ebene Flächen |
| 0:55–1:35 | Übung 2D-Homographie | Foto als Projektionsfläche: Viereck → Fassade → Würfel |
| 1:35–1:45 | Pause | |
| 1:45–2:00 | Grenzen der Homographie | Gekrümmte Flächen, Bezier-/Grid-Warping, Überleitung zu 3D |
| 2:00–2:45 | Virtueller Raum | Template-Szene, OBJ laden, virtueller Projektor, Zuschauer-Kamera |
| 2:45–3:00 | Aufgabe & Fragen | 3D-Scan eines Objekts bis Tag 2 |

Details: [tag-1/README.md](tag-1/README.md)

### Tag 2 – Content, Multi-Setup, Ausblick

| Zeit | Block | Inhalt |
|---|---|---|
| 0:00–0:15 | Scans importieren | Eigene Scans laden, Probleme lösen |
| 0:15–0:55 | Prerendered Content | UV-Textur oder Rendering aus Projektorperspektive |
| 0:55–1:30 | Realtime Content | Shader, Animation, audioreaktiv |
| 1:30–1:40 | Pause | |
| 1:40–2:10 | Mehrere Projektoren | Hard Edge vs. Soft Edge, Blending mit BadMapper |
| 2:10–2:40 | Multi-PC & Sync | UDP-Übung, Hardware-Sync (Frame Lock / Genlock) |
| 2:40–3:00 | Ausblick: Scalable | Automatische Kamera-Kalibrierung mit VL.ScalableDisplay |

Details: [tag-2/README.md](tag-2/README.md)

## Aufbau des Repos

```
setup/        Installationsanleitung für Teilnehmende
tag-1/        Ablauf und Übungen Tag 1
tag-2/        Ablauf und Übungen Tag 2
patches/      vvvv-Patches (Templates und Übungen)
assets/
  photos/     Fotos als Projektionsflächen für die 2D-Übungen
  objects/    Beispiel-Objekte (.obj)
content/      Prerendered Beispiel-Content
slides/       Folien
docs/         Vorbereitung und Quellen
```

## Voraussetzungen

Windows-Rechner mit dedizierter GPU, **zweiter Monitor**, vvvv 7.4 und einige NuGet-Pakete. Siehe [setup/INSTALL.md](setup/INSTALL.md).
