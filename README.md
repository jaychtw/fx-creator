# FX Creator

**AI-operated, code-driven visual effects production for our games.**

FX Creator is an experimental **skill-first** workflow for ChatGPT and Codex. It begins by teaching collaborators to find, generate, inspect, refine, validate, and package pixel VFX using [PixelFX](https://github.com/patch-gg/pixelfx), not by inventing a renderer or deploying a service.

## Status

**M0 — documentation and feasibility specification only.** No FX Creator renderer, installed ChatGPT plugin, packaged assets, or successfully executed end-to-end generation has been demonstrated yet.

### Intended collaboration

- **Creative director (human):** defines style and intended experience; approves consequential visual choices and release.
- **ChatGPT:** interprets creative direction, coordinates variations and visual review, produces assets **only where the conversation's tools actually permit execution**.
- **Codex:** evaluates feasibility, operates and adapts tooling when needed, and integrates approved assets into game projects.
- **FX Creator:** a portable, versioned skill and (eventually) repeatable production recipes, validation, and handoff conventions.

An AI-readable skill file is **instructions, not an installed executable**. GitHub hosting does not automatically make the tool callable in a ChatGPT conversation. The first experiment must prove the actual execution path; do not claim conversational asset generation before it is observed.

## Start here

- [Production skill](skills/fx-creator/SKILL.md): capability-aware instructions and bounded workflow.
- [M0 feasibility brief](docs/M0-FEASIBILITY.md): what Codex should inspect, test, and report **before** proposing additional implementation.
- [Asset package contract](docs/ASSET-PACKAGE.md): minimum regenerable source and handoff.
- [Project state](PROJECT_STATE.md): verified status, decision boundaries, next steps.
- [Attribution](NOTICE.md): source lineage and conditions to check when adapting code.

## Scope and constraints

First target: one **original heavy cannon-impact pixel effect** as a visual experiment relevant to Armorheart; this is **not** authorization to change Armorheart. Default $0 cost, local-first, no account or paid service, no unapproved merge, deployment, or material game change. Protect human artistic approval separately from automated validation.

FX Creator is deliberately limited to **pixel VFX** in M0. Avoid general asset-platform ambitions until a real production experiment justifies them.

## Upstream and standards

PixelFX: [repository](https://github.com/patch-gg/pixelfx), [AI skill](https://github.com/patch-gg/pixelfx/blob/main/skills/pixelfx/SKILL.md), [authoring guide](https://github.com/patch-gg/pixelfx/blob/main/docs/AUTHORING.md), [notices](https://github.com/patch-gg/pixelfx/blob/main/NOTICE.md).

Governance: [AI Collaboration & Continuity Protocol (AICP)](https://github.com/jaychtw/game-development-standards/blob/main/AI-COLLABORATION-PROTOCOL.md), [UGDS](https://github.com/jaychtw/game-development-standards/blob/main/UGDS.md). Codex should pin the applicable revisions during implementation. The project-specific asset quality bar must remain compatible with the destination game's approved visual direction.

**Contribution policy:** develop on a working branch, preserve honest evidence, propose changes for review, and do not merge or publish without explicit authorization.
