# OpenGL Projects

Four real-time 3D graphics projects built in **C / C++ with OpenGL** (legacy fixed-function pipeline) using Visual Studio. Built for the *Computer Graphics* course at "Lucian Blaga" University.

---

## 1. Forest_Scenery_V2.2 — 3D Forest Landscape

A 3D forest scene with terrain, trees, sky and grass textures. Demonstrates skyboxes, texture mapping and a navigable camera.

- Skybox: `pos_x.tga`, `neg_x.tga`, `pos_y.tga`, `neg_y.tga`, `pos_z.tga`, `neg_z.tga`
- Ground: `groundText.tga`, `grassMare.tga`

**Run:** open `Forest_Scenery_V2.2/Proiect PeisajV2.2.sln` in Visual Studio.

---

## 2. Planets — Solar System

A simple solar system / planet scene rendered in OpenGL.

- `PLANET.C` — main scene (ANSI C)

**Run:** open `Planets/Proiect Planete.sln` in Visual Studio.

---

## 3. PokeBall — Polygon Drawing

A Poké Ball rendered using basic OpenGL polygon primitives.

- `Desenare_poligoane.c` — polygon-drawing logic
- `PokeBallIco.ico` — application icon

**Run:** open `PokeBall/PokeBall.sln` in Visual Studio.

---

## 4. Ship v3.0 — Animated 3D Ship Scene

A 3D ship on water with interactive camera controls.

**Controls:**
- `↑ / ↓ / ← / →` — move the ship
- `W / A / S / D` — camera movement
- `P` — pause
- `O` — options
- `R` — reset

**Run:** open `Ship v3.0/Vapor v3.0.sln` in Visual Studio.

---

## Tech

C / C++, OpenGL (legacy fixed-function pipeline), GLUT, Visual Studio

> Note: the precompiled `.exe` files are included in each project's `Debug/` folder for quick testing without rebuilding.
