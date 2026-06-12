# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

This is a collection of LEGO MINDSTORMS EV3 saved programs (`.lmsp` files), intended to be shared publicly on GitHub.

## LMSP file format

`.lmsp` files are zip archives containing:

| Entry | Description |
|-------|-------------|
| `manifest.json` | Project metadata (name, creation date, hardware config, extensions used, program mode) |
| `scratch.sb3` | The actual program — a Scratch 3.0 project (itself a zip archive) |
| `icon.svg` | Project icon/thumbnail |

### Key manifest fields

- `type`: `"word-blocks"` — LEGO's Scratch-based block programming language
- `hardware`: EV3 brick connection info (Bluetooth Classic, brick ID)
- `extensions`: EV3-specific Scratch extensions used (e.g. `ev3events`, `ev3display`, `ev3sensors`, `ev3sound`, `ev3motor`)
- `state.playMode`: `"download"` (runs on the brick) or `"stream"` (streamed from the app)
- `progress`: Tracks which lesson/activity this program belongs to in the LEGO Education curriculum

## How to open and use these files

- Open `.lmsp` files with the [LEGO MINDSTORMS Education EV3](https://education.lego.com/en-us/downloads/mindstorms-ev3/software) desktop application (Windows/macOS)
- Files can also be unzipped to inspect the underlying `manifest.json` and `scratch.sb3`:
  ```
  unzip "Robot Arm H25.lmsp"
  ```
- The inner `scratch.sb3` can be opened in [Scratch 3](https://scratch.mit.edu/) or extracted further for inspection
