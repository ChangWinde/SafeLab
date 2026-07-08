# SafeLab Project Page

This package contains a self-contained static project page for SafeLab.

## Quick Open

Open `index.html` in a browser.

For the most reliable video/PDF behavior, run a local static server from this folder:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

If the browser toolbar shows 80% zoom, press `Cmd+0` on macOS or `Ctrl+0` on Windows/Linux. Chrome and Edge remember zoom per site, so `localhost` may keep an old zoom setting even when the page itself is designed at 100%.

## Contents

- `index.html`: project homepage
- `assets/images/`: optimized WebP images and poster previews used by the page
- `assets/videos/`: H.264 MP4 videos; non-hero videos are lazy-loaded by the page
- `assets/docs/`: paper and poster PDFs

## Asset Notes

- Images are stored directly under `assets/images/` as WebP files.
- Current optimized footprint is about 59 MB total: 2.5 MB images, 49 MB videos, and 8.0 MB docs.
- Videos are the main size driver. They are H.264 MP4 files with fast-start metadata, and non-hero videos are loaded only when needed.
- PDFs are linearized and are not loaded on first paint; they are opened only from resource links.
