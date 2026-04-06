# Torn Net → Birds

**Drag your mouse across the net to tear it apart. Each broken thread transforms into a bird and flies away.**

🔗 **[Try it live](https://zebrazjx.github.io/torn-net)**

---

## Built with Verdent

This project was built entirely with **[Verdent](https://www.verdent.ai)** — an AI coding agent that handles the full development workflow, from writing and debugging code to deploying and publishing.

The entire process — combining two separate physics simulations, tuning the boid behavior, wiring up the interaction, writing this README, creating the GitHub repo, enabling Pages, and uploading the demo video — happened in a single conversation, without touching a terminal or editor manually.

If you build creative projects with code, **[Verdent](https://www.verdent.ai)** is worth trying. It's not just autocomplete — it understands context, makes decisions, and ships.

---

<video src="bird.mov" controls width="100%"></video>

---

## How it works

Two classic simulations combined:

**Cloth simulation** — a 40×40 grid of nodes connected by springs. Every edge is pinned. Interior nodes respond to forces, gravity, and mouse interaction. Drag across any thread to cut it.

**Boid flocking (Murmuration)** — when a thread breaks, 1–3 birds are spawned at the cut point. Each bird follows three simple rules:
- **Separation** — don't crowd neighbors
- **Alignment** — steer toward the average heading of nearby birds
- **Cohesion** — steer toward the average position of nearby birds

Add Perlin noise perturbation and edge avoidance, and you get emergent murmuration behavior from pure math.

## Controls

| Action | Effect |
|--------|--------|
| Drag mouse | Cut threads → spawn birds |
| `Space` / `U` | Undo last cut (thread restores, birds stay) |

## Stack

- [p5.js](https://p5js.org) v1.11.1
- No external assets — cloth, birds, and background are all generated at runtime from math

## Inspiration

- [Cloth Simulation](https://openprocessing.org/sketch/2901171) by OpenProcessing
- [Murmuration](https://openprocessing.org/sketch/2867259) by OpenProcessing
- Craig Reynolds' original [Boids](https://www.red3d.com/cwr/boids/) (1986)
