# Open GSG Proto

A minimal grand-strategy map prototype for Android, built in Godot 4.5.

This is stage 1 of a larger project: a clickable political map you can pan, zoom, and select
provinces/countries on. It's the foundation the rest of the game (nations, turns, economy, AI)
will be built on top of.

## What's here right now

- Smooth-bordered political map rendering (HQX border shader)
- Pan with arrow keys, zoom with middle mouse wheel
- `Ctrl + Click` to select a country, `Click` to reassign a province's owner
- A second, simpler scene (`simple_political_map.tscn`) with no border rendering, for comparison

## Credits / built on

- [gs-map-editor](https://github.com/OneBogdan01/gs-map-editor) by Bogdan Mocanu (MIT) — the
  GDExtension providing the province/country data pipeline, custom inspector, and map rendering.
  This repo vendors its `demo/` project (trimmed to Android binaries only) as the starting point.
- The border shader technique originates from [opengs](https://github.com/Thomas-Holtvedt/opengs)
  by Thomas Holtvedt, adapted for GDExtension by gs-map-editor.
- Border rendering approach references this
  [Intel paper on gradient border rendering](https://www.intel.com/content/dam/develop/external/us/en/documents/optimized-gradient-border-rendering-in-imperator-rome.pdf).

See `LICENSE-gs-map-editor.md` for the upstream MIT license.

## Building

Open in Godot 4.5 and run, or push to `main` — GitHub Actions will build a debug APK
automatically (see Actions tab → artifacts).

## Roadmap (not built yet)

- Nation data model (stats, ownership persistence, save/load)
- Turn or tick-based time system
- Basic AI behavior
- War/diplomacy systems
