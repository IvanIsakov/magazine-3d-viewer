# Magazine 3D Viewer

A single-file web app that turns any PDF magazine into an interactive, realistically animated 3D book. Drop in a PDF — the first page becomes the front cover, the last page the back cover — and flip through it in 3D.

**Try it:** open `index.html` in a modern browser (Chrome, Edge, Firefox, Safari). No install, no build step, no server. Your PDF is processed entirely locally in the browser and never leaves your computer.

A sample zine (`Cowzine ver1.pdf`) is included for a quick test.

## Features

- **Drag & drop any PDF** — automatic page-format detection (A3–A6, Letter, Legal, Tabloid, Square) with confirm/override of the exact page size in millimetres.
- **Realistic page turning** — pages bend with a curved curl as they turn, rest with a convex bow like real paper, and every sheet stays bound at the seam; the left pile slides down one sheet thickness per turn. A black spine grows and shrinks with the stacks.
- **Flip by grabbing a page corner** and peeling it over, or use the ◀ ▶ buttons / arrow keys — all the way to the back cover.
- **Full 3D orbit & zoom** at any moment, including mid-flip.
- **Two controllable lights** (RGB colour, intensity, direction, height) plus ambient level.
- **Paper finish slider** — one physical axis from uncoated matte stock to coated gloss, backed by a soft studio-sheen reflection.
- **Backgrounds** — white, black, any custom colour, a coffee-table scene (PBR wood, depth of field, contact shadows), or a living-room scene.
- **Snapshot button** — saves the current view as a PNG.

## Tech

- [Three.js](https://threejs.org/) (r160) for rendering — custom sheet geometry with numerically integrated curl/drape deformation, VSM soft shadows, ACES tone mapping, bokeh depth of field.
- [PDF.js](https://mozilla.github.io/pdf.js/) for rasterizing PDF pages to textures.
- Everything lives in one HTML file; libraries load from CDN.

## License

[MIT](LICENSE)
