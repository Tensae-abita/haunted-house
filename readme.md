<div align="center">

# 🏚️ Haunted House — Three.js Journey

**A spooky procedural 3D scene built with Three.js: a fog-shrouded house, a graveyard of tombstones, and wandering ghost lights, all rendered in real time on the web.**

[![Three.js](https://img.shields.io/badge/Three.js-r174-000000?logo=three.js&logoColor=white)](https://threejs.org)
[![Vite](https://img.shields.io/badge/Vite-6.x-646CFF?logo=vite&logoColor=white)](https://vitejs.dev)
[![lil-gui](https://img.shields.io/badge/lil--gui-0.20-blue)](https://lil-gui.georgealways.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

</div>

## Overview

This is exercise 16 from the [Three.js Journey](https://threejs-journey.com/) course — a from-scratch, WebGL-rendered haunted house scene. It's built with raw Three.js (no game engine, no React wrapper) to practice core rendering concepts: PBR materials driven by texture maps, real-time shadows, fog, animated point lights, and a `lil-gui` debug panel for tweaking the scene live.

The scene composes a textured house (walls, roof, door with door-light), scattered bushes, a graveyard of low-poly tombstones, and a set of ghost lights that orbit the house on independent sinusoidal paths — all wrapped in exponential fog and moonlit ambient/directional lighting for atmosphere.

## ✨ Features

- **Textured house** — walls, roof, and door built from color, ambient-occlusion, normal, and roughness texture maps for realistic PBR shading
- **Animated ghost lights** — multiple colored point lights orbit the house on independent trigonometric paths, casting moving shadows
- **Graveyard** — procedurally scattered, randomly rotated and tilted tombstones around the house for an unsettling, uneven layout
- **Atmospheric fog** — exponential fog blends the scene into darkness at a distance, reinforcing the night setting
- **Real-time shadows** — shadow-casting/receiving configured across the house, ghosts, and ground
- **Live debug controls** — `lil-gui` panel exposes lighting, fog, and material parameters for real-time tweaking
- **Fast dev loop** — powered by Vite for instant HMR while iterating on the scene

## 🧱 Tech Stack

| Layer | Choice |
|---|---|
| 3D rendering | [Three.js](https://threejs.org) `^0.174` |
| Build tool | [Vite](https://vitejs.dev) `^6.2` |
| Debug UI | [lil-gui](https://lil-gui.georgealways.com/) `^0.20` |
| Language | Vanilla JavaScript (ES modules) |

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en/download/) (LTS recommended)

### Installation

```bash
git clone https://github.com/Tensae-abita/16-haunted-house.git
cd 16-haunted-house
npm install
```

### Run locally

```bash
npm run dev
```

Vite will print a local URL in your terminal (typically `http://localhost:5173`) — open it in your browser to view the scene.

### Build for production

```bash
npm run build
```

Outputs an optimized, static build to the `dist/` directory, ready to deploy anywhere that serves static files (Netlify, Vercel, GitHub Pages, etc.).

## 📁 Project Structure

```
src/
├── script.js        # Scene setup: camera, renderer, lights, meshes, animation loop
└── style.css         # Base page styling

static/
└── textures/          # Color, normal, AO, and roughness maps for house, floor, and door
```

## 🎨 Customizing the Scene

Most tweakable values (light colors/intensities, fog density, material roughness) are wired into the `lil-gui` panel at runtime — open the panel in the corner of the page and adjust live without touching code. For structural changes (house dimensions, tombstone count, ghost paths), edit `src/script.js` directly.

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](./LICENSE) file for details.

---

<div align="center">
Built while learning WebGL fundamentals through <a href="https://threejs-journey.com/">Three.js Journey</a>.
</div>
