# 🏙️ MiniMetro — 3D City Builder

An interactive 3D city-building simulator that runs entirely in the browser from a single HTML file. Build roads, houses, shops, factories, parks, and power infrastructure, then watch traffic, population, tax revenue, and power demand evolve in real time through a full day/night cycle.

![City builder](https://img.shields.io/badge/Three.js-r160-blue) ![No build step](https://img.shields.io/badge/build-none-success)

## ✨ Features

- **Click-to-build 3D city** — place roads (drag to paint), houses, apartments, shops, offices, factories, parks, power plants, and wind turbines on a grid.
- **Real-time simulation**
  - **Population** grows toward road-connected housing capacity, modulated by jobs, power, and happiness.
  - **Tax revenue** from residents and commerce, minus building upkeep and power-plant fuel.
  - **Traffic** — cars path-find along your road network; congestion lowers income and happiness.
  - **Power grid** — every building draws power; brownouts cripple growth until you add generation.
  - **Pollution** from factories/power plants, offset by parks.
- **RCI demand bars** — live Residential / Commercial / Industrial demand indicators show what the city needs next.
- **Day/night cycle** — moving sun with shadows, dynamic sky gradients, stars, glowing windows at night, and a moon fill light.
- **Generative ambient music** — a procedural Web Audio soundtrack that mellows at night (no audio files needed).
- **Save / load** — the city auto-saves to `localStorage` and reloads on startup.

## 🚀 Running it

No build step, no dependencies to install. Either:

- **Open directly:** double-click `city.html` (needs an internet connection — Three.js loads from a CDN), **or**
- **Serve locally:**
  ```bash
  python -m http.server 8000
  # then visit http://localhost:8000/city.html
  ```

## 🎮 Controls

| Action | Control |
| --- | --- |
| Orbit camera | Drag |
| Zoom | Scroll |
| Place building | Pick a tool, click the ground |
| Paint roads | Drag with the Road tool |
| Demolish | Right-click a tile, or the Demolish tool |
| Select tools | Keys `1`–`9`, `0` |
| Pause / resume | `Space` |
| Toggle music | `M` |
| Game speed | `1× / 2× / 4×` buttons |

## 🛠️ Tech

Plain HTML + JavaScript with [Three.js](https://threejs.org/) (loaded via CDN import map) and the Web Audio API. Everything lives in one self-contained `city.html`.

## 📄 License

MIT
