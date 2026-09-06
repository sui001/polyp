# polyp

The "notwled" project: PCA9685 servo patches arranged into a shared grid, with
effects (ripple, sweep, chase, wind, dominoes) running across the stitched
space the same way WLED's 2D panel setup does for LED matrices. See
[CLAUDE.md](CLAUDE.md) for the full concept and how it relates to
[Tuft](../tuft).

## Console

**[sui001.github.io/polyp →](https://sui001.github.io/polyp/)**

Arrange boards, tune each servo (type, horn length/thickness/orientation,
mount tilt/pan), pick wall/floor/roof mounting aspect, run a directional
effect, then export the whole configuration as JSON, enough to hand to real
PCA9685 firmware. Repo is public so the free GitHub Pages plan can serve it;
there's no research/thesis content here, just the tool.

`index.html` at the repo root is what Pages serves, keep it in sync with
`visualizer/polyp-console.html` when the console changes.

Also live as a private Claude artifact:
[polyp console (Claude)](https://claude.ai/code/artifact/7287ed4f-2422-4c04-92ac-a139fcdd5c02).
