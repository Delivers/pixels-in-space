# Tag 2 – Content, Multi-Setup, Ausblick

## 0:00–0:15 Scans importieren

Typische Probleme: Polygonzahl, Maßstab, Normalen, fehlende UVs.

## 0:15–0:55 Prerendered Content

Zwei Wege:
1. **UV-basiert:** Textur über das UV-Layout des Objekts erstellen
2. **Projektorperspektive:** Kamera in Blender an die Position des virtuellen Projektors setzen und von dort rendern

Beispieldateien in `content/`. Video in vvvv abspielen und mappen.

## 0:55–1:30 Realtime Content

- Prozedurale Shader
- Animation auf der Geometrie
- Audioreaktiv
- Vergleich: Flexibilität (realtime) vs. Kontrolle (prerendered)

## 1:40–2:10 Mehrere Projektoren

Patch: `patches/20_Blending.vl`

- Zwei virtuelle Projektoren überlappen → doppelte Helligkeit
- Hard Edge vs. Soft Edge
- Soft Edge manuell mit BadMapper

## 2:10–2:40 Multi-PC & Sync

### Drei Ebenen von Sync
- **Content-Sync:** gleicher Frame / gleiche Zeit (Software)
- **Frame Lock:** Bildwechsel im selben Moment (Hardware)
- **Genlock:** gemeinsames Taktsignal (Hardware)

### Übung: UDP-Sync
Patches: `patches/30_Sync_Server.vl`, `patches/31_Sync_Client.vl`

- Zwei vvvv-Instanzen auf einem Rechner, verbunden über UDP auf localhost
- Server schickt Framenummer, Client rendert seine Bildhälfte
- Schalter für simulierten Paketverlust / Delay → Drift an der Blend-Kante beobachten

Praxis-Tipps: Kabel statt WLAN, ein Switch, Firewall-Regeln, Pakete unter MTU (ca. 1472 Bytes), stabile Framerate auf jedem PC.

### Hardware-Sync
- NVIDIA Quadro Sync II / RTX PRO Sync: RJ-45 für Frame Lock, BNC für Genlock
- Bis zu 4 GPUs pro Karte, bis zu 8 GPUs / 32 Displays pro System
- Nur mit professionellen RTX-GPUs
- Wann nötig: geblendete Flächen, schnelle Bewegung über Kanten, Stereo, LED-Wände

## 2:40–3:00 Ausblick: Scalable

1. **Problem:** Manuelles Mapping muss bei jeder Verschiebung wiederholt werden
2. **Prinzip:** Kameras sehen Testmuster, Software berechnet Warping, Blending, Farbkorrektur
3. **Workflow:** Scalable Display Manager (Trial) → `.ol` / `.pol` → VL.ScalableDisplay, Help-Beispiel „HowTo Apply a mapping from a Scalable mesh file“
4. **Einordnung:** lohnt sich bei vielen Beamern und Dauerinstallationen. Für Einzelobjekte und temporäre Arbeiten reicht manuell
