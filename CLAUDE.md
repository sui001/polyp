# polyp

The "notwled" project. WLED drives addressable LED protocols with a 2D panel
arrangement (multiple physical matrices stitched into one virtual canvas) and an
effects engine that runs over that stitched space without knowing panel
boundaries exist. Polyp is the same two ideas, panel layout + effects-over-a-
virtual-grid, rewritten for PCA9685-driven servo patches instead of LED strips.
It is not a WLED fork; the output layer (PWM angle vs. RGB brightness) is
different enough that forking bought nothing but a codebase built for the wrong
peripheral.

Named after the coral/anemone polyp: one body, one PCA9685 "patch," a ring of
reaching parts. Grew out of [[project_tuft_concept]] but is meant to be reusable
by anything in gen3d wanting a servo grid, not scoped to Tuft.

## Core model

- A **patch** = one PCA9685 board = up to 16 channels, arranged as rows x cols.
- Patches sit in a shared virtual grid (position + orientation), same as WLED's
  panel setup screen.
- **Effects** are `value = f(worldX, worldY, t)` and address the stitched grid,
  never a literal channel number. The layout layer is what turns
  `(worldX, worldY)` into `(I2C address, channel)`.

## Contents

- `visualizer/` — WebGL concept console: arrange patches, preview an effect
  running across them as servo-paddle tilt. Concept stage, not driving real
  hardware yet.

Repo is private. No thesis/theory writing here, that belongs in
`affective-devices/docs/`.

## Conventions

- No em dashes in anything written for Sui.
- Default ESP32 board is the SuperMini, GPIO 1-13 only, see gen3d memory
  `esp32s3-supermini-board`.
