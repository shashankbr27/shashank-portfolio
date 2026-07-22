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
| 2 | Voice console + two paired robots | **AI & Robotics Intern** | The speech-to-speech pipeline (console) and the multi-robot OpenRMF work (the pair). |
| 3 | Robot arm + RGB coordinate gizmo | **Perception validation** | Pose / coordinate-transform (tf2) accuracy — the gizmo *is* the coordinate frame being calibrated. |
| 4 | GPU server rack + benchmark screen | **Model selection & latency** | Benchmarking VLMs, cutting GPU overhead, −30% latency. |
| 5 | Autonomous rover + LiDAR on a nav map | **Nayantra** | A Nav2 robot on a planned path — the thing itself. |
| 6 | Glowing memory core (rings + emitter) | **AMAR** | Persistent memory + recursive reasoning as stacked, lit layers. |
| 7 | Pan-tilt camera head, three lenses | **Cosmic Eyes** | A perception rig that reads a scene and predicts the next step. |
| 8 | Instrument wall of lit tiles | **Skills** | Breadth of the stack wired to one bench. |
| 9 | Access terminal + lit doorway | **Contact** | The exit — real, clickable links. |

### Deliberately left out

- The résumé's *"refactored and cross-verified the Vision Analytics codebase, added
  test coverage, reduced retrieval latency"* bullet — folded into the model/latency
  station rather than given its own bench, to keep that panel tight.
- The ARTPARK work email; the contact station uses the personal email, phone,
  LinkedIn and GitHub from the résumé.
- Contact links: GitHub is `github.com/shashankbr27`; LinkedIn points at and
  displays `linkedin.com/in/shashankbr2709`.

### Notes

- **Station 2 (voice workstation)** was rebuilt to lead with an upright monitor
  showing the dual STT/TTS waveform facing the walk path, with a desk mic and the
  two paired robots for the multi-robot OpenRMF work — a stronger silhouette than
  the original dark console.
