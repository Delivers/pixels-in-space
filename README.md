# Pixels in Space

**Projection Mapping & Immersive Setups in vvvv**
Mapping, edge blending and networked sync with Simon Weckert

Online workshop, part of the vvvv Intermediates Program Winter 2026/27 at the [NODE Institute](https://thenodeinstitute.org/courses/pixels-in-space-projection-mapping-immersive-setups-in-vvvv).

- **Dates:** Tuesday, December 8 and 15, 2026, 18:00–21:00 CET
- **Format:** two live online sessions, recordings available for at least one year
- **vvvv version:** 7.4
- **Announcement:** [vvvv blog](https://vvvv.org/blog/2026/pixels-in-space-projection-mapping-immersive-setups-in-vvvv/)

From the 16:9 monitor to real surfaces and whole rooms: from simple 2D homography to mapping onto 3D objects, all the way to multi-projector and multi-PC setups. By the end, you have the technical foundation for interactive installations, stage designs and immersive exhibition spaces.

Since the course runs online, everyone works in a virtual scene (Stride) that simulates projectors and lets you load your own objects as `.OBJ`. A second monitor stands in for the projector.

## Schedule

### Day 1 – From 2D to 3D

| Time | Block | Content |
|---|---|---|
| 0:00–0:15 | Welcome, setup check | vvvv and packages running for everyone |
| 0:15–0:35 | History & terminology | Magic lantern, Haunted Mansion (1969), *Displacements* (1980), *Shader Lamps* (2001), facade mapping. Throw ratio, lens shift, keystone |
| 0:35–0:55 | What is a homography? | 3×3 matrix, 8 degrees of freedom, 4 point pairs, planar surfaces only |
| 0:55–1:35 | Exercise: 2D homography | Single quad → facade → cube |
| 1:35–1:45 | Break | |
| 1:45–2:00 | Limits of homography | Curved surfaces, Bezier/grid warping, transition to 3D |
| 2:00–2:45 | Virtual space | Template scene, load OBJ, virtual projector, spectator camera |
| 2:45–3:00 | Assignment & questions | 3D scan an object before day 2 |

Details: [day-1/README.md](day-1/README.md)

### Day 2 – Content, multi-setups, outlook

| Time | Block | Content |
|---|---|---|
| 0:00–0:15 | Import scans | Load your scans, fix common issues |
| 0:15–0:55 | Prerendered content | UV texture or rendering from the projector's perspective |
| 0:55–1:30 | Realtime content | Shaders, animation, audio-reactive |
| 1:30–1:40 | Break | |
| 1:40–2:10 | Multiple projectors | Hard edge vs. soft edge, blending with BadMapper |
| 2:10–2:40 | Multi-PC & sync | UDP exercise, hardware sync (frame lock / genlock) |
| 2:40–3:00 | Outlook: Scalable | Automatic camera-based calibration with VL.ScalableDisplay |

Details: [day-2/README.md](day-2/README.md)

## Repository structure

```
setup/        Installation guide for participants
day-1/        Schedule and exercises, day 1
day-2/        Schedule and exercises, day 2
patches/      vvvv patches (templates and exercises)
assets/
  photos/     Photos used as projection surfaces in the 2D exercises
  objects/    Example objects (.obj)
content/      Prerendered example content
slides/       Slides
docs/         Preparation and sources
```

## Requirements

Windows PC with a dedicated GPU, **a second monitor**, vvvv 7.4 and a few NuGet packages. See [setup/INSTALL.md](setup/INSTALL.md).
