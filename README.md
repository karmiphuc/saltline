# Saltline

An unofficial, source-preserving fork of **Saltline**, the browser FPS originally created and shared by **Felix Rieseberg using Claude Fable 5.2**.

This repository exists to make the shared game easy to play through GitHub Pages and to keep its provenance visible. The original game, design, procedural art and audio are not presented as my own work.

## Play

Use the website link in this repository's **About** section. The game runs in your browser with no installation or account integration.

Your mission is to disable three uplink relays in a container port and reach the extraction boat while avoiding hostile drones and robotic hounds.

## Original creator and inspiration

Credit for the original Saltline experiment goes to **[Felix Rieseberg](https://github.com/felixrieseberg)** and **Claude Fable 5.2**.

- [Felix's original launch post](https://x.com/felixrieseberg/status/2119925633564463609)
- [Original playable Claude artifact](https://claude.ai/artifact/BGY1SztrAYcJQHSsnHHGmp)

Felix described the project as an experiment with one-shot prompts and no human feedback during the initial run. He reported roughly eight hours and $550 at API pricing. Those are the creator's reported figures, not measurements made by this fork. The original artifact can change; this repository preserves a specific shared export.

The inspiration here is the original experiment's compact, code-generated game world. This is a direct code-derived fork, rather than a new game that merely borrows the idea. It is unofficial and does not imply endorsement by Felix Rieseberg, Anthropic or the mirror maintainer.

## Fork lineage and provenance

This is a GitHub fork of **[realcodebear/saltline-fable-5.2](https://github.com/realcodebear/saltline-fable-5.2)**, a community mirror that credits Felix and links to his original artifact. **realcodebear is the mirror maintainer, not the original game's creator.** This is not a fork of a Felix-owned GitHub repository.

The starting upstream snapshot is [4a737fb54eee314a9763202507329391bc0fe088](https://github.com/realcodebear/saltline-fable-5.2/commit/4a737fb54eee314a9763202507329391bc0fe088).

The game published here comes from the separately shared `saltline_1.html` export received on 11 November 2026. Its complete JavaScript block was compared with the community mirror and matched exactly. The differences were limited to the document title and formatting of the HTML head.

The shared export is preserved byte-for-byte as `index.html`:

- Size: 1,423,581 bytes
- SHA-256: `039890a0fa3fbe2c8d6b6b907e937d47c5a0b80b742f32fb3a4f19f0f15e0cac`

## What this fork changes

- Publishes the supplied export through GitHub Pages.
- Expands the README with creator credit, lineage, controls and technical context.
- Adds `.nojekyll` for direct static hosting and third-party license notices.

No gameplay, balance, rendering or audio code has been changed. There is no claim that this is the latest version of the original artifact.

## Controls

| Action | Keyboard / mouse |
| --- | --- |
| Move | W, A, S, D |
| Look | Mouse |
| Fire / aim | Left / right mouse button |
| Reload | R |
| Cut relay | Hold E |
| Jump / sprint | Space / Shift |
| Crouch | C or Ctrl |
| Melee | F |
| Pause | Esc or P |

Touch controls are included: the left side moves, the right side looks, and on-screen buttons handle actions. The game also contains standard gamepad support. Use Settings to adjust quality, sensitivity, volume and field of view.

## Technical notes

- A single HTML file containing CSS and bundled JavaScript.
- Uses Three.js revision 180 and WebGL.
- Geometry, textures and sound are generated in the browser.
- Optional typefaces load from Google Fonts; fallback fonts are defined.
- Settings are stored locally in the browser under `saltline.settings.v1`.
- No server-side application, database, API keys or build process is required.

For local use, serve this directory with a static web server, for example:

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000. A modern browser with WebGL enabled is required.

## Licensing and third-party notices

No project-wide license was included in the supplied game export or the upstream community mirror when this fork was prepared. No new license is being asserted over the original game, and attribution does not itself grant reuse rights. Check with the original rights holders before relying on permission to redistribute, modify or use the game commercially.

The bundled Three.js library has its own MIT license, reproduced in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). That license applies to Three.js, not automatically to the entire game.

## Verification

The supplied HTML was checked for completeness, and its JavaScript passed `node --check`. Its checksum was verified against the supplied export. Gameplay and device compatibility have not been tested as part of this hosting-only update.
