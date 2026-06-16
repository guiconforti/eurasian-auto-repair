# Eurasian Auto Repair — Demo Site

Single-page marketing site for Eurasian Auto Repair (San Antonio import & European specialist),
featuring a **scroll-driven cinematic hero** that scrubs through a video frame sequence on a
pinned, DPR-aware canvas.

## Highlights

- **Scroll-scrub hero** — a 300vh scroll track with a pinned `100vh` canvas. Scroll progress
  maps to a frame index; frames are preloaded, drawn "cover", and updated inside
  `requestAnimationFrame`.
- **Per-device frame sets** — desktop uses 150 frames @1600px (`scroll-hero/frames/`); mobile
  uses a lighter 60 frames @720px (`scroll-hero/frames-mobile/`).
- **Accessibility** — `prefers-reduced-motion` falls back to a single static frame, no scrub.
- Self-contained: all CSS/JS inline in `index.html`. Only external assets are the WebP frames.

## Run locally

Any static server works (needed so the WebP frames load over HTTP):

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Or just open `index.html` directly in a browser.

## Deploy (GitHub Pages)

Settings → Pages → Deploy from branch → `main` / root. `index.html` serves automatically.
