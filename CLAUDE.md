# CLAUDE.md — how to build on this starter

This repo is a **zero-build 3D game starter** made with three.js + anime.js.
Someone will describe what they want their world to do; your job is to make it
happen by editing the scene. This is how the project it came from was built:
**one described idea at a time, always runnable.** Follow these rules.

## What this project is
- A single static site. `index.html` sets up an **importmap** and loads
  `src/main.js` as an ES module. That's the whole app.
- All libraries are **vendored** in `vendor/` and committed. There is **no npm
  install, no bundler, no build step, and no internet requirement** at runtime.
- `src/main.js` holds the entire scene: renderer, sky/sun, lights, ground,
  post-processing (bloom), OrbitControls, WASD/arrow movement, the anime.js
  intro, and the render loop. Most changes happen here.

## Golden rules (do not break these)
1. **Never add a build step or a package manager requirement.** No Vite, no
   webpack, no bundling, no transpiling. It must keep running from
   `python3 -m http.server`.
2. **Import through the importmap**, exactly like the three.js docs:
   ```js
   import * as THREE from 'three';
   import { OrbitControls } from 'three/addons/controls/OrbitControls.js';
   import { GLTFLoader }    from 'three/addons/loaders/GLTFLoader.js';
   import { animate, createTimeline, stagger, utils } from 'animejs';
   ```
   Every three.js addon already exists under `vendor/three/addons/…` — use it,
   don't fetch from a CDN. If you import a new addon, confirm the file exists in
   `vendor/three/addons/` first.
3. **No CDN `<script>` tags and no new runtime dependencies.** If something truly
   needs a new library, vendor it into `vendor/` and add it to the importmap.
4. **Keep it one file where reasonable.** New systems can go in `src/` as ES
   modules imported by `main.js`, but don't over-engineer. Prefer clear,
   readable code that matches the existing style and comment density.
5. **Use anime.js for animation and transitions** (pops, fades, timelines). It
   animates numeric properties on any object, including `THREE.Vector3`s — see
   the crystal entrance and intro timeline in `main.js` for the pattern.

## The build loop
1. Read the person's request and turn it into a concrete change in the scene.
2. Edit `src/main.js` (or add a small module in `src/`).
3. **Verify it runs**: serve the folder (`python3 -m http.server 8765`) and load
   `http://127.0.0.1:8765/`. Check the browser console for errors. If you have
   browser automation, take a screenshot to confirm it looks right.
4. Keep each change small and shippable. Don't rewrite the whole scene for one
   request — extend it.

## Assets — free and license-clean only
- When a theme is described, you may pull **free CC0** assets from the web and
  drop them in `assets/` (models in `assets/models/`).
- Good CC0 sources: Poly Pizza, Quaternius, Kenney (models); Poly Haven,
  ambientCG (textures/HDRIs); Freesound, Kenney (audio).
- Load `.glb`/`.gltf` with `GLTFLoader` (see the `loadModel()` helper in
  `main.js`), HDRs with `RGBELoader`.
- **Only use assets that are license-clean** (CC0 preferred). Record every added
  asset and its license in `assets/CREDITS.md`. Do not commit copyrighted art,
  logos, or characters you don't have the rights to.

## Audience & tone
- This starter is meant to be approachable — it may be driven by kids or
  first-time builders. Prefer additive, delightful changes. Explain what you
  changed in plain language.
- Honor explicit requests (a specific number, color, or name) literally. If a
  request would make the game worse (e.g. a value that breaks balance or
  performance), implement what was asked and fix the underlying *mechanic*
  rather than silently overriding the request.

## Performance
- Target a smooth 60 fps. Reuse geometries/materials, avoid allocating in the
  render loop, and cap `renderer.setPixelRatio` (already capped at 2).
- Shadows and bloom are on and look good; if the scene gets heavy, reduce shadow
  map size or lower bloom before ripping features out.

## Handy hooks
- `window.WORLD` exposes `{ THREE, scene, camera, renderer, controls, composer,
  crystals, setSun, animate, utils }` for quick console tinkering.
- `setSun(elevationDeg, azimuthDeg)` moves the sun and re-aims the shadow light —
  use it for day/night.
