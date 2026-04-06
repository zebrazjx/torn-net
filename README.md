# Torn Net → Birds

**Drag your mouse across the net to tear it apart. Each broken thread transforms into a bird and flies away.**

🔗 **[Try it live](https://zebrazjx.github.io/torn-net)**

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

## Built with

- [p5.js](https://p5js.org) v1.11.1
- No external assets. Sky, cloth, and birds are all generated at runtime.
- Built with [Verdent](https://www.verdent.ai) — an AI coding agent that took this from idea to deployed project in one session.

## Inspiration

- [Cloth Simulation](https://openprocessing.org/sketch/2901171) by OpenProcessing
- [Murmuration](https://openprocessing.org/sketch/2867259) by OpenProcessing
- Craig Reynolds' original [Boids](https://www.red3d.com/cwr/boids/) (1986)
