# Computer Graphics Explorables

Interactive, browser-based teaching modules on computer graphics algorithms. Each module runs the real algorithm live, lets you step through it one stage at a time, covers its history, and shows how GPUs make it fast. Built for self-study and classroom use.

**Live site:** https://shanem73.github.io/computer-graphics-explorables/

## Modules

| Module | Status | What it covers |
|---|---|---|
| [Ray Tracing](ray-tracing/) | Available | A live GPU path tracer; a step-by-step 3D walkthrough of one pixel (primary, reflected, refracted and shadow rays); history from 1968 to 2025; the DXR/Vulkan ray tracing pipeline, BVH traversal and RT cores |
| [Gaussian Splatting](gaussian-splatting/) (Splat Lab) | Available | From drone photos to a real-time splat: keypoints, matching and Structure from Motion; 3D Gaussians and spherical-harmonic colour; EWA projection; tile rasterisation and alpha blending; loss, backpropagation, Adam and densification; a four-Gaussian gradient lab with every derivative shown; quizzes and instructor notes on every step |

## Using the modules

- **In class:** every module and part has its own link, e.g. `ray-tracing/#render`, `#algorithm`, `#history`, `#hardware`, or `gaussian-splatting/#setting`, `#sh`, `#gradlab`, so you can link a specific step from slides, a syllabus or an LMS.
- **Self-study:** work through each module's parts in order with the Next button or the left/right arrow keys.
- **Locally:** each module is a single self-contained HTML file with no build step. Clone the repo and open `index.html` in a browser.

## Requirements

A current desktop or mobile browser with WebGL 2 (Chrome, Edge, Firefox, Safari). The live renderer uses the GPU; on older hardware, lower the render resolution in Part 1. Fonts (Google Fonts), [three.js](https://threejs.org/) r128 and [MathJax](https://www.mathjax.org/) 3 load from a CDN.

## Repository layout

```
index.html          landing page listing all modules
ray-tracing/        Ray Tracing module (single HTML file)
gaussian-splatting/ Gaussian Splatting module, Splat Lab (single HTML file)
.nojekyll           tells GitHub Pages to serve files as-is
```

New modules follow the same pattern: one folder per module with its own `index.html`, plus a card on the landing page.

## Sources

Ray Tracing module history and hardware sections draw on: Appel (1968), Whitted (1980), Cook, Porter & Carpenter (1984), Kajiya (1986), Purcell et al. (2002), Woop, Schmittler & Slusallek (2005), and vendor architecture whitepapers for NVIDIA Turing, Ampere, Ada and Blackwell, AMD RDNA 2–4, and Intel Xe HPG.

Gaussian Splatting module draws on: Kerbl, Kopanas, Leimkühler & Drettakis (2023), *3D Gaussian Splatting for Real-Time Radiance Field Rendering*; Zwicker, Pfister, van Baar & Gross (2002), *EWA Splatting*; Schönberger & Frahm (2016), *Structure-from-Motion Revisited* (COLMAP); Lowe (2004), SIFT; Hartley & Zisserman (2004), *Multiple View Geometry*; Ramamoorthi & Hanrahan (2001) on spherical harmonics for lighting; He et al. (2016) on residual connections. The demo site, photos and camera poses are synthetic.

## License

Code is released under the [MIT License](LICENSE). three.js and MathJax are licensed by their authors (MIT and Apache 2.0).

## Contributing

Corrections, classroom feedback and module ideas are welcome. Please open an issue or a pull request.
