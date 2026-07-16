# M3PUIM 2026 Flipbook Booklet

An interactive 3D HTML5 flipbook viewer designed for the M3PUIM 2026 conference booklet. Allows attendees to read through conference slides and booklets like a physical book directly on their mobile phones, tablets, or desktop browsers.

## ✨ Features

- **No Server Dependencies**: Pure static HTML/CSS/JS frontend application. Can be hosted for free anywhere (GitHub Pages, Netlify, Vercel).
- **On-Demand Page Rendering**: Dynamically renders PDF pages to `<canvas>` only when visible or adjacent. This prevents high memory usage and browser tab crashes on mobile devices even with very large PDFs.
- **Mobile Optimized**: Custom touch gesture listeners (including **double-tap to zoom** to read small text) and thumb-navigable page controls.
- **Synthesized Audio**: Dynamically generates page-flipping audio cues using the browser's native **Web Audio API** (avoiding heavy network asset downloads).
- **Premium Aesthetics**: Harmonious dark theme layout with floating glassmorphic control panels.

## 🛠️ Built With

- **[PDF.js](https://mozilla.github.io/pdf.js/)** (v2.16.105) - Crisp client-side PDF loading and parsing.
- **[StPageFlip](https://github.com/Nodlik/StPageFlip)** (v2.0.7) - Fluid 3D page turning animations.
- **Web Audio API** - Custom synthesized paper rustling effects.

## 🚀 Running Locally

Due to browser security policies governing Web Workers and CORS, PDF.js cannot load local files directly via `file://` URLs. You must run a local web server:

1. Open your terminal and navigate to the directory:
   ```bash
   cd "/Users/usernname/Documents/M3PUIM/app"
   ```
2. Start a simple Python HTTP server:
   ```bash
   python3 -m http.server 8000
   ```
3. Open your browser and visit: **[http://localhost:8000/index.html](http://localhost:8000/index.html)**.

## 🔄 Updating the Document

To change the displayed document:
1. Delete or rename the current `book.pdf` in the `app` folder.
2. Put your new PDF in the `app` folder and rename it to exactly `book.pdf`.
3. Refresh the web page.
