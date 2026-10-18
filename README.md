# Shashank B R — Portfolio

A scroll-driven, first-person walk through an **Autonomous Systems Lab**. Scrolling
walks you forward down one long hall; at each bench, one object carries one chapter
of my career and a text panel fades in beside it.

Single self-contained `index.html` — [three.js](https://threejs.org) from a CDN,
all geometry built in code and all textures drawn to `<canvas>`. No build step, no
external assets.

## Run it

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Deploy on GitHub Pages

1. Push this repo to GitHub.
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch.**
3. Branch: `main`, folder: `/ (root)`. Save.
4. Your portfolio is live at `https://<username>.github.io/<repo>/`.

## Debug hook

`window.__x` drives the camera without scrolling:

- `__x.station(i)` — jump to station `i`
- `__x.seek(p)` — jump to walk-progress `p` (0–1)
- `__x.info()` — station count and current position

---

## Note (per the brief)

### Station → chapter mapping

The theme is a robotics/AI research lab, and each object was chosen so its *actual
nature* argues the chapter — not just decoration:

| # | Object | Chapter | Why this object |
|---|--------|---------|-----------------|
| Overture | The hall itself | Name + role + hook | You're standing at the lab door. |
| 1 | Drafting table + blueprint board | **Education** (B.E. ISE, GAT) | Where the fundamentals were drawn up. |
| 2 | Voice console + two paired robots | **AI & Robotics Intern** | The speech-to-speech pipeline (console) and the MCP-based multi-robot coordination (the pair). |
| 3 | Robot arm + RGB coordinate gizmo | **Perception validation** | Pose / coordinate-transform accuracy — the gizmo *is* the coordinate frame being calibrated. |
| 4 | GPU server rack + benchmark screen | **VLM stack swap & latency** | LLaVA/Qwen-VL + SAM2 + Grounding DINO v2 replacing Cosmos, −30% chatbot latency, refactor/tests. |
| 5 | Video wall + panning dome camera | **Thili** | Detection/action modules, and one track hopping between camera feeds (cross-camera tracking). |
| 6 | Radar + 4×4 acoustic array + LWIR imager, fused display | **Sensor-fusion research** | Radar (ARD 548 RDI), acoustic array (UMA-16) and thermal imager for infiltration detection. |
| 7 | Autonomous rover + LiDAR on a nav map | **Nayantra** | A Nav2 robot on a planned path — the thing itself. Meta line links to the GitHub repo. |
| 8 | Pan-tilt camera head, three lenses | **Cosmic Eyes** | A perception rig that reads a scene and predicts the next step. |
| 9 | Instrument wall of lit tiles | **Skills** | Breadth of the stack wired to one bench. |
| 10 | Access terminal + lit doorway | **Contact** | The exit — real, clickable links, a "Thank you!" and a **Go to start** button. |

### Deliberately left out

- **AMAR** and the education coursework list — neither is on the current résumé, so
  both were removed (they are still in git history).
- The ARTPARK work email; the contact station uses the personal email, phone,
  LinkedIn and GitHub from the résumé.
- Contact links: GitHub is `github.com/shashankbr27`; LinkedIn points at and
  displays `linkedin.com/in/shashankbr2709`.

### Notes

- **Station 2 (voice workstation)** was rebuilt to lead with an upright monitor
  showing the dual STT/TTS waveform facing the walk path, with a desk mic and the
  two paired robots for the multi-robot coordination work — a stronger silhouette
  than the original dark console.
- **Panels** are `visibility: hidden` unless active, so off-screen links/buttons
  can't be clicked or tabbed to. The closing panel stays up through the end of the
  scroll, and **Go to start** smooth-scrolls back to the door (instant when the
  visitor prefers reduced motion).
