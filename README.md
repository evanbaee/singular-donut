# Singular Donut

**A torus in motion.**

`Three.js` · `GLSL` · `WebGL`

An interactive Three.js experiment with a torus animated by custom GLSL shaders.

## Features

- Procedural noise displaces the torus geometry over time.
- A custom fragment shader colors the deformed surface.
- OrbitControls lets you explore the object with the camera.
- A dat.GUI panel exposes displacement, spread, and noise controls.
- The code includes an EffectComposer and a bloom pass for post-processing experiments.

## Run locally

Install Node.js and npm, then run:

```sh
npm install
npx vite --host 127.0.0.1
```

Open the local URL printed by Vite in a browser with WebGL support.

To build the static site:

```sh
npm run build
```

The build is written to `dist/`. Vite is invoked through `npx` in this repository and is not pinned in `package.json`.

## Code map

| Path | Purpose |
| --- | --- |
| `src/index.js` | Scene, camera, torus, controls, and render loop |
| `src/shaders/vertexShader.js` | Noise-based vertex displacement |
| `src/shaders/fragmentShader.js` | Procedural surface color |
| `index.html` | Browser entry point |

## Status

A graphics learning experiment from 2024. The render loop calls both the post-processing composer and the renderer directly; the final visible output should not be treated as a verified bloom showcase. It is retained as a reference for shader and geometry experiments.
