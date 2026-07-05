# 3D World Starter

A polished, **zero-build** starting point for making a 3D browser game with
[**three.js**](https://threejs.org) and [**anime.js**](https://animejs.com) —
designed to be extended by describing what you want to
[**Claude Code**](https://claude.com/claude-code).

Open it and you already have a good-looking world: a lit courtyard with a
fountain, trees, floating crystals, a real sky with a movable sun, bloom, an
animated loading screen, and WASD/arrow-key movement. From there you just say
*"add a river"* or *"make the crystals collectible"* and build your game one
idea at a time.

> **No build step. No CDN. No internet required.** three.js and anime.js are
> vendored into `vendor/` and loaded through an importmap, so the code reads
> exactly like the official docs and runs from any static file server.

---

## Get started in 60 seconds

### 1. Make your own copy
Click **“Use this template” → “Create a new repository”** at the top of this
repo's GitHub page (or use the CLI):

```bash
gh repo create my-3d-game --template markjeromecruz/threejs-claude-starter --public --clone
cd my-3d-game
```

### 2. Run it locally
Module scripts + importmaps need a real `http://` origin (not `file://`), so
serve the folder with any static server:

```bash
python3 -m http.server 8765
# then open http://127.0.0.1:8765/
```

You should see the loading screen fade into a sunny courtyard. Drag to look,
scroll to zoom, WASD/arrow keys to move.

### 3. Build with Claude Code
This is the fun part. Open the folder in [Claude Code](https://claude.com/claude-code)
and just describe what you want:

```
> add a bouncing beach ball I can push around
> make it night with glowing lanterns
> spawn a character I can walk around as, instead of a free camera
> add coins that float and disappear when I touch them
```

Claude reads [`CLAUDE.md`](CLAUDE.md) (the house rules for this repo), edits
`src/main.js`, and can even pull **free CC0 assets** from the web when you
describe a theme. Refresh the browser to see each change.

---

## Project layout

```
.
├── index.html          # importmap + loading screen + HUD (start here)
├── CLAUDE.md           # how Claude Code should build on this starter
├── src/
│   └── main.js         # the whole scene: renderer, sky, lights, post-fx, controls, loop
├── assets/
│   ├── models/         # CC0 .glb models (drop new ones here)
│   └── CREDITS.md      # asset licenses
└── vendor/             # local copies of the libraries — committed, no install needed
    ├── three/          # three.js core + the FULL examples/jsm addons
    └── anime/          # anime.js
```

## Using the libraries

The importmap in `index.html` wires up bare specifiers, so imports read like the
official docs:

```js
import * as THREE from 'three';
import { OrbitControls } from 'three/addons/controls/OrbitControls.js';
import { GLTFLoader }    from 'three/addons/loaders/GLTFLoader.js';   // load 3D models
import { animate, createTimeline, stagger, utils } from 'animejs';
```

Everything under three.js's `examples/jsm/` is available at `three/addons/…` —
controls, loaders (GLTF/FBX/OBJ/Draco), postprocessing (bloom, SSAO, outline),
Sky, Water, lil-gui, noise, and much more. No extra downloads.

## What's already wired up

- **Renderer** with ACES filmic tone mapping and soft shadows
- A real **Sky** with a sun you can move (`setSun(elevation, azimuth)`)
- Hemisphere + directional **lighting**
- **Ground** plane and a subtle build grid
- **Bloom** post-processing for that production glow
- **OrbitControls** + **WASD/arrow-key** movement across the world
- An animated **loading screen → HUD** reveal (anime.js)
- A 60 fps **render loop** with an FPS readout
- Example **GLTF models** loaded from `assets/models/` (the asset pipeline)

Replace the placeholder floating crystals in `src/main.js` with your real game.

## Free assets

When you describe a theme, pull **license-clean** assets and drop them in
`assets/`:

- **Models:** [Poly Pizza](https://poly.pizza) · [Quaternius](https://quaternius.com) · [Kenney](https://kenney.nl) (CC0)
- **Textures / HDRIs:** [Poly Haven](https://polyhaven.com) · [ambientCG](https://ambientcg.com) (CC0)
- **Audio:** [Freesound](https://freesound.org) · [Kenney audio](https://kenney.nl) (CC0)

`GLB/GLTF` models load with `GLTFLoader`; HDR environments with `RGBELoader`.
See [`assets/CREDITS.md`](assets/CREDITS.md).

## Deploy it

It's a static site — host it anywhere. The simplest is **GitHub Pages**:
push to `main`, then in **Settings → Pages** set the source to the `main` branch
root. Your world goes live at `https://<you>.github.io/<repo>/`.

## Origin

This started as a real 3D game two kids built with Claude Code, one described
idea at a time — a whole town with neighbors, quests, and a pet dog grew out of
this exact starter file. Their original characters and art are *not* included
here; this is the clean, reusable canvas they began from, shared so you can start
your own. 💎

## License

[MIT](LICENSE) for the template code. Bundled three.js and anime.js keep their
own MIT licenses; bundled models are CC0 (see [`assets/CREDITS.md`](assets/CREDITS.md)).
