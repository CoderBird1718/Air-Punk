# AIR // DRAW — Neon Cyberpunk

Draw in thin air using just your hand — no mouse, no touch, no stylus. A webcam-based gesture drawing app powered by [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands), wrapped in a magenta/cyan cyberpunk HUD. Point to draw, open your palm to erase, pinch to reposition, and make a fist to pause the ink. Runs entirely client-side — nothing is recorded or uploaded.

**[Live demo →]  https://coderbird1718.github.io/Air-Punk/**

## Gestures

| Gesture | Action |
|---|---|
| ☝️ Point (only index finger up) | **Draw** a glowing neon line |
| 🖐️ Open palm (all four fingers up) | **Erase** around your palm |
| 🤏 Pinch (thumb + index touching) | **Move** the cursor without drawing |
| ✊ Fist | **Idle** — ink paused |

## Features

- Real-time hand tracking via MediaPipe, no installs required
- Dual-pass neon line rendering (colored glow + bright core) for a true light-trail look
- 6 preset neon colors + custom color picker
- Adjustable brush size and eraser size
- Toggle to hide the camera feed and draw on a plain dark grid instead
- Save your artwork as a PNG
- Clear error handling for camera permissions, HTTPS requirement, and CDN load failures

## Running it

No build step — it's a single HTML file.

### Locally
Just open `index.html` directly in a browser, or serve it with any static server:
```bash
python3 -m http.server 8000
```
Then visit `http://localhost:8000`.

### Deployed (GitHub Pages)
1. Push this repo to GitHub.
2. Go to **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main`, folder: `/ (root)`.
3. Your app will be live at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

> Camera access requires HTTPS or `localhost` — GitHub Pages serves over HTTPS by default, so it works out of the box.

## Notes

- Requires a webcam and browser permission to use it.
- The hand-tracking model loads from a CDN (`cdn.jsdelivr.net`) at runtime, so an internet connection is needed even when self-hosted.
- Best results in good, even lighting with one hand clearly visible to the camera.

## Tech

- Vanilla HTML/CSS/JS — no framework, no build tooling
- [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands) + Camera Utils (via CDN)
- Fonts: Orbitron, Share Tech Mono (Google Fonts)

## License

Feel free to fork, modify, and reskin for your own themes.
