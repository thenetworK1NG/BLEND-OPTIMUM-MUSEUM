# My Art (FPS Octree Demo)

A self-contained page that recreates the `examples/games_fps.html` demo from this repo, served from a new folder.

## Run

From the repository root (this folder is `my art/` at the root):

1) Install deps (once):

```powershell
npm ci
```

2) Start the local server:

```powershell
npm run dev
```

3) Open the page:

- http://localhost:8080/my%20art/

This page uses CDN-hosted scripts and the example CSS/model, so you can also open it with any simple static server that serves just this folder:

- http://localhost:8000/ (if you serve `my art/` directly)

## Controls

- Mouse: look around; click/hold to charge, release to throw a ball
- WASD: move
- Space: jump

If you fall off the world, you'll be teleported back to the start.

## Notes

- This page now uses CDN paths:
  - three: `https://unpkg.com/three@0.180.0/build/three.module.js`
  - addons: `https://unpkg.com/three@0.180.0/examples/jsm/`
  - examples CSS + model: `https://threejs.org/examples/...`
- If you prefer local assets instead, change `index.html`:
  - CSS to: `../examples/main.css`
  - import map to: `three -> ../build/three.module.js`, `three/addons/ -> ../examples/jsm/`
  - GLB path to: `../examples/models/gltf/`