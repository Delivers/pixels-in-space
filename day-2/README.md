# Day 2 – Content, multi-setups, outlook

## 0:00–0:15 Import scans

Common issues: polygon count, scale, normals, missing UVs.

## 0:15–0:55 Prerendered content

Two approaches:
1. **UV-based:** create a texture using the object's UV layout
2. **Projector perspective:** place a camera in Blender at the virtual projector's position and render from there

Example files in `content/`. Play back the video in vvvv and map it.

## 0:55–1:30 Realtime content

- Procedural shaders
- Animation on the geometry
- Audio-reactive
- Comparison: flexibility (realtime) vs. control (prerendered)

## 1:40–2:10 Multiple projectors

Patch: `patches/20_Blending.vl`

- Two overlapping virtual projectors → double brightness in the overlap
- Hard edge vs. soft edge
- Manual soft edge with BadMapper

## 2:10–2:40 Multi-PC & sync

### Three levels of sync
- **Content sync:** same frame / same time (software)
- **Frame lock:** buffer swaps at the same moment (hardware)
- **Genlock:** shared timing reference (hardware)

### Exercise: UDP sync
Patches: `patches/30_Sync_Server.vl`, `patches/31_Sync_Client.vl`

- Two vvvv instances on one machine, connected via UDP on localhost
- Server sends the frame number, client renders its half of the image
- Toggle for simulated packet loss / delay → watch the drift at the blend edge

Practical tips: cable instead of Wi-Fi, a single switch, firewall rules, keep packets below the MTU (approx. 1472 bytes), stable frame rate on every PC.

### Hardware sync
- NVIDIA Quadro Sync II / RTX PRO Sync: RJ-45 for frame lock, BNC for genlock
- Up to 4 GPUs per card, up to 8 GPUs / 32 displays per system
- Professional RTX GPUs only
- When you need it: blended surfaces, fast motion across edges, stereo, LED walls

## 2:40–3:00 Outlook: Scalable

1. **Problem:** manual mapping has to be redone every time something moves
2. **Principle:** cameras capture test patterns, software calculates warping, blending and color correction
3. **Workflow:** Scalable Display Manager (trial) → `.ol` / `.pol` → VL.ScalableDisplay, help patch "HowTo Apply a mapping from a Scalable mesh file"
4. **When it's worth it:** many projectors and permanent installations. For single objects and temporary work, manual mapping is enough
