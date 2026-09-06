# polyp

The "notwled" project: PCA9685 servo patches arranged into a shared grid, with
effects (ripple, sweep, chase, wind, dominoes) running across the stitched
space the same way WLED's 2D panel setup does for LED matrices. See
[CLAUDE.md](CLAUDE.md) for the full concept and how it relates to
[Tuft](../tuft).

## Console

Live, interactive WebGL build-out of the concept:

**[polyp console →](https://claude.ai/code/artifact/7287ed4f-2422-4c04-92ac-a139fcdd5c02)**

Arrange boards, tune each servo (type, horn length/thickness/orientation,
mount tilt/pan), pick wall/floor/roof mounting aspect, run a directional
effect, then export the whole configuration as JSON, enough to hand to real
PCA9685 firmware.

Private artifact link, sign in as the repo owner to open it.
