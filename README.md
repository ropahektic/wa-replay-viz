# WA Replay Viewer

A minimal online viewer for Worms Armageddon replays: open a `.watrace` file and play it back with
simple shapes: terrain (with craters as they happen), worms as team-coloured circles with health,
the turn worm ringed with its path, ropes, parachutes, projectiles with trails, mines, drums and
crates.

**https://ropahektic.github.io/wa-replay-viz/**

- Model layer (M): each projectile's path as our model predicts it at spawn (dashed: blue = matches WA to the
  end, red = leaves it, with a red cross where), and fire checked against our fire model every frame (red rings =
  fires the model got wrong; panel bottom-left). Traces made with the current converter include it.
- Space: play / pause · ← →: 0.5 s · Shift+← →: previous / next turn · Home / End
- Speed 0.5× to 16×, timeline with turn marks

A `.watrace` is made locally from a `.WAgame` replay: WA plays it headless and records what happened.
The file holds positions only (gzip'd JSON lines). Everything runs in your browser; nothing is uploaded.
