# Claude Planet

A tiny 3D world where every one of your Claude projects is a building on a floating island.
Pinned projects rise as skyscrapers downtown; chats and tasks are little houses in the
neighborhoods around them. Each building has a hard-hatted worker who hammers away while the
project is active and dozes off (with floating z's) after 45 quiet minutes. Robots jog the
sidewalks, cars roll down the streets, planes circle overhead, clouds drift, and the lighting
follows your clock from sunrise through golden hour to a moonlit night.

Built with plain HTML/JS and [three.js](https://threejs.org) (loaded from cdnjs). No build step.

## Using it

Open `index.html` in a browser, or serve the folder with any static file server.

- **Drag** to orbit, **scroll** to zoom, **hover** a building for its name.
- **Click** a building to open the linked chat; **shift-click** to wake or rest its worker.
- The pills at the top are filters (multi-select): skyscrapers, houses, working, napping.
  The other pills cycle label visibility (hover / pinned + working / all) and the time of day (auto / day / golden hour / night).
- The side panel adds projects (name, optional link, pinned or not), edits links, and demolishes buildings.

Out of the box the world is saved in the browser's `localStorage`. The page also looks for a
`window.claude.use("db")` capability, which is how the original ran as a live-updating
[claude.ai artifact](https://claude.ai) with a shared database; without it, everything simply
stays local.

## Customizing

- `SEED` near the top of the script is the starter list of projects.
- `pal` / `roofs` are the daytime wall and roof colors; `palNight` / `roofsNight` are the softer night palette.
- `IDLE_MS` controls how long a project stays "working" before its worker falls asleep.
- `HOME` sets the default camera angle.

## License

MIT — see [LICENSE](LICENSE).
