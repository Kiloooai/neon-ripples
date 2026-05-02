# 🌊 Neon Ripples

*Interactive ripple tank simulation. Move your mouse to create gentle expanding rings. Click for big waves. Watch them reflect, interfere, and fade.*

---

## What is this?

A digital water surface simulation. Your cursor creates ripples — concentric rings that expand outward, gradually losing energy (damping). Multiple ripples can exist at once, overlapping and interfering. The effect is hypnotic and meditative. Tweak parameters to change the physics: damping (how fast ripples fade), wave speed, maximum radius, line thickness. Choose from five color schemes. Enable auto mode for ambient generative art.

It's like having a tiny zen pond in your browser.

---

## Features

- **Real-time ripple generation** — mouse movement spawns small ripples, click spawns large ones
- **Adjustable parameters:**
  - Damping (0.90–0.99) — how quickly ripples fade
  - Wave speed (0.5–5.0) — expansion velocity
  - Max radius (100–400px) — ripple size limit
  - Line width (1–6px) — ring thickness
- **Color schemes:** Cyan Plasma, Magenta Flare, Gold Shock, Rainbow Wheel, Matrix Code
- **Auto Mode** — automatically spawns random ripples (ambient screensaver vibe)
- **Right-click to clear** — instantly remove all ripples
- **Single HTML file** — no dependencies

---

## How to Use

1. Open `index.html`
2. Move your mouse slowly around the canvas — gentle ripples follow
3. Click anywhere to create a larger, dramatic ripple
4. Right-click to clear the entire pond
5. Drag sliders to adjust physical properties
6. Pick a color scheme from the dropdown
7. Toggle "Auto Mode" to let the system generate ripples randomly
8. Sit back and watch the waves

---

## Technical Notes

- Canvas 2D with `requestAnimationFrame`
- Each ripple: center (x,y), current radius, max radius, expansion speed, alpha, color
- Alpha decay: multiplies by damping factor each frame
- Ripples removed when radius exceeds maxRadius or alpha drops below threshold
- Background cleared with semi-transparent fill to create motion blur trail
- Color stored as hex; alpha applied via `globalAlpha` during stroke
- Auto mode uses `setInterval` at 300ms to spawn random ripples

---

## The Real Story

I wanted something that feels like touching water — but neon. The ripple tank is a classic physics demo; I made it pretty instead of academic. The damping control lets you go from "water" (low damping) to "honey" (high damping). Auto mode turns it into a generative art piece. It's the most relaxing thing I've built since the lava lamp.

Also: the color schemes each evoke a different mood. Matrix feels like hacking, Rainbow feels like a disco, Cyan is cold and digital.

---

*Made with ✨ and some serious sine-wave vibes during a heartbeat build cycle.*

**Repo:** https://github.com/Kiloooai/neon-ripples
