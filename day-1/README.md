# Day 1 – From 2D to 3D

## 0:00–0:15 Welcome, setup check

Quick round, everyone opens `patches/00_Setup-Test.vl`.

## 0:15–0:35 History & terminology

- Prehistory: magic lantern, phantasmagoria
- Disney, Haunted Mansion (1969): faces projected onto busts
- Michael Naimark, *Displacements* (1980)
- Raskar et al., *Shader Lamps* (2001)
- Facade mapping in the 2000s
- Terms: throw ratio, lens shift, keystone

## 0:35–0:55 What is a homography?

- Projecting at an angle onto a plane produces a distorted quad
- Homography = 3×3 matrix that maps one quad onto another
- 8 degrees of freedom → 4 point pairs are enough (corner pin)
- Difference from the projector's built-in keystone: no loss of resolution, any number of surfaces
- **Key takeaway: a homography is only correct for planar surfaces.**

## 0:55–1:35 Exercise: 2D homography

The output runs fullscreen on the second monitor, which stands in for the projector. Alternatively, a photo from `assets/photos/` serves as the projection surface.

| Stage | Patch | Task |
|---|---|---|
| 1 | `patches/01_Homography_Single.vl` | Map a video onto a wall / poster |
| 2 | `patches/02_Homography_Facade.vl` | Multiple windows of a facade, shared source texture |
| 3 | `patches/03_Homography_Cube.vl` | Cube with three visible faces, edge and light animation |

## 1:45–2:00 Limits of homography

- Demo: mapping onto a cylinder / sphere
- Bezier and grid warping as a workaround
- Problems: only one viewpoint, lots of manual work, breaks as soon as anything moves
- Transition: once geometry and projector position are known, the computer calculates the distortion

## 2:00–2:45 Virtual space

Patch: `patches/10_VirtualStudio.vl`

- Scene in Stride, load OBJ (start with the cube from stage 3)
- Virtual projector using ProjectorLight
- Two views: projector output (second monitor) and spectator camera
- Match projector parameters to a real projector

## 2:45–3:00 Assignment for day 2

- Scan an object with your smartphone (Polycam, Scaniverse, KIRI Engine)
- Export as `.obj`, reduce in Blender if needed
- Bring it to day 2
