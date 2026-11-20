# Alltoolkit

**Zero-Upload PDF, Image, Archive & Document Studio.**  
Alltoolkit is a privacy-first, single-file web utility that processes PDFs, images, animated GIFs, ZIP archives, Markdown documents, and structured data **100% locally in your browser**. Files never leave your device.

---

## Key Features

### Universal Smart Dropzone
- Drop any supported file (`.pdf`, `.png`, `.jpg`, `.webp`, `.gif`, `.zip`, `.md`, `.json`, `.csv`) onto the top dropzone to automatically detect its format and launch the matching studio tool with the file pre-loaded.

### Section A — Dedicated PDF Suite
- **Merge & Organize PDFs**: Combine multiple PDFs, view live page thumbnails, reorder pages, rotate `90°`, delete unwanted pages, filter via page ranges (e.g., `1-3, 5`), and export merged or split PDFs.
- **PDF to High-DPI Images**: Rasterize PDF pages at `1x`, `2x`, or `3x` DPI scale into PNG or JPEG and download individually or bundled as a `.zip`.
- **Watermark, Stamp & Page Numbers**: Apply custom diagonal watermarks or header stamps with opacity and font-size controls, plus automatic `Page X of Y` footers.
- **Metadata & Privacy Sanitizer**: Inspect PDF page dimensions and document info, edit Title/Author/Subject/Keywords, or strip all hidden metadata cleanly.

### Section B — All-Format & Docs Studio
- **Universal Image Converter & Resizer**: Batch convert between PNG, JPEG, and WebP (with support for BMP, ICO, and SVG inputs), adjust compression quality, resize with locked aspect ratios, and view byte-savings telemetry.
- **Images to PDF Builder**: Compile photos and scans into a multi-page PDF with A4, US Letter, or native image sizing and customizable margins.
- **GIF Frame Extractor & Sprite Sheet**: Deconstruct animated GIFs into individual PNG frames, download a `.zip` frame pack, or stitch a horizontal PNG sprite sheet.
- **ZIP Archive Inspector & Creator**: Browse `.zip` directory trees and preview inner text, code, or images inline without extracting to disk—or compress staged files into a new `.zip` archive.
- **Markdown & Document Studio**: Split-pane live Markdown editor with XSS-safe preview, word/read-time counter, and one-click export to `.pdf`, `.html`, or `.md`.
- **Data, Base64 & Crypto Hash**: Format/minify JSON, convert bidirectionally between JSON and CSV with live table preview, encode/decode Base64 text or files, and compute client-side SHA-256 / SHA-512 checksums.

### Design & UX
- Tactile bento-card layout with generous rounded corners (`20px`) and layered depth.
- Instant **Light / Dark** studio theme switcher.
- Zero tracking, zero telemetry, zero backend servers.

---

## Quick Start & Local Usage

No build tools, Node.js, or package managers are required.

1. Download `index.html`.
2. Double-click `index.html` to open it directly in any modern browser (Chrome, Edge, Firefox, Safari).
3. Drag and drop your files to begin processing immediately.

*(Note: An active internet connection is used on initial page load to fetch client-side libraries from `cdnjs` and fonts from `fonts.googleapis.com`.)*

---

## Deployment

Because Alltoolkit is a single static HTML file, you can host it for free on any static web host with zero server costs:

- **Netlify Drop**: Drag the folder containing `index.html` onto [app.netlify.com/drop](https://app.netlify.com/drop).
- **Cloudflare Pages**: Upload `index.html` directly or connect a GitHub repository (no build command required).
- **GitHub Pages**: Push `index.html` to a repository and enable Pages under **Settings → Pages** (`main` branch, `/ (root)`).
- **Vercel**: Import your repository or deploy via `npx vercel`.

---

## Tech Stack (Client-Side)

| Library / API | Purpose |
| :--- | :--- |
| **pdf-lib** | PDF merging, splitting, rotation, watermarking, metadata editing, and image-to-PDF assembly |
| **PDF.js** | Local PDF page rendering, thumbnails, and high-DPI rasterization |
| **JSZip** | In-browser `.zip` inspection and archive creation |
| **HTML5 Canvas & ImageDecoder** | Image format conversion, resizing, GIF frame extraction, and sprite sheet stitching |
| **marked & DOMPurify** | Markdown parsing and HTML sanitization |
| **Web Crypto API** | Native browser SHA-256 and SHA-512 file hashing |

---

## Privacy & Architecture

All file operations execute inside your browser's memory (`ArrayBuffer`, `Blob`, `FileReader`, `Canvas2D`). Because no files are ever uploaded to a remote server, file size limits depend only on your device's available browser RAM.

---

## License

MIT License — free to use, modify, self-host, and deploy.

```
