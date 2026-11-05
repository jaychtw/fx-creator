---
name: fx-creator
description: Use when producing or refining original code-driven pixel-art VFX for our game projects. Discover PixelFX recipes, render and inspect previews, iterate within a bounded brief, validate, and package reproducible assets for review and game integration. Do not claim tool availability without checking.
license: MIT
compatibility: Requires an execution environment with Node.js >=18 and an accessible PixelFX checkout for upstream commands; visual inspection capability is required for aesthetic review. Skill installation in ChatGPT is environment-dependent.
---

# FX Creator — AI asset production

## Purpose and responsibility

Produce **inspectable, regenerable visual effects**, not one-shot promises. Prefer original effects or clearly attributable adaptations. The creative director owns the intended look and final visual acceptance; AI collaborators select routine implementation techniques and report evidence. ChatGPT is the preferred creative producer **when it can actually run and inspect the tool**; Codex is responsible for engineering and integration unless explicitly assigned production work.

This is an original orchestration skill **informed by**, not a verbatim copy of, [patch-gg/pixelfx](https://github.com/patch-gg/pixelfx)'s [skill](https://github.com/patch-gg/pixelfx/blob/main/skills/pixelfx/SKILL.md) and [authoring contract](https://github.com/patch-gg/pixelfx/blob/main/docs/AUTHORING.md). Consult upstream for its precise APIs and limitations rather than assuming these instructions replace it.

## Capability preflight — mandatory

1. Identify the runtime (ChatGPT session, Codex workspace, or other), accessible repository, filesystem, execution tool, image/animation inspection, Node version, and any offline/network constraints.
2. Locate an approved PixelFX checkout. If missing and cloning is supported, first check permission and provenance; otherwise report the precise blocker. Avoid unpinned dependency drift when reproducibility matters.
3. From the PixelFX checkout, verify the documented command on a known sample: `node tools/render.mjs fire/torch`. Inspect `records/fire/torch/contact.png` if accessible. **Do not infer success from source availability.**
4. If ChatGPT cannot invoke a runtime command, it may prepare an actionable specification/brief and inspect returned artifacts; it **must not** claim it created files. Route execution to Codex or another genuinely accessible environment. A GitHub skill is not automatically installed in chat.

## Creative specification

Before generation record a compact intent contract:
- Project, intended visual context and approved art direction; original/reference assets and provenance.
- Effect behavior (trigger, silhouette, timing phases, direction, scale at game resolution, palette, animation duration, looping).
- Deliverables (editable source/recipe, PNG sprite sheet, JSON frames/pivots/durations, previews, validation).
- Exclusions (no game logic modification, no third-party font, no unauthorized deployment, spend $0 by default).
- Acceptance checks and human aesthetic decisions still required.

Avoid guessing missing creative approval from the upstream default style. For Armorheart, example POC is one heavy cannon impact: controlled force, readable at play scale, not an oversized decorative explosion. This is a candidate experiment, not approved production art.

## Execute — upstream workflow with bounded original production

1. **Discover:** inspect `docs/CATALOG.md` and use `node tools/list.mjs <words>` to find nearby techniques. Render relevant existing candidates. Do not silently reuse a library asset when original production is required.
2. **Construct:** inspect upstream `docs/AUTHORING.md`, choose pure `draw(p,t,o)` vs seeded simulated `create(o)`, and create an original effect via `node tools/new.mjs <category>/<name>` when available. Prefer parameters and reusable mechanisms over copied imagery.
3. **Preview:** run `node tools/render.mjs <id>`; inspect the contact sheet *and* time-sequenced frames or a playable preview for motion. Explicitly inspect first-frame onset, impact, decay, end state, and target in-game scale.
4. **Refine:** choose a small number of meaningfully different variants where creative direction warrants it; fix the highest-impact defect per iteration. Bound iterations by the brief (default max three revision rounds for M0); record any unresolved quality problems.
5. **Validate:** run `node tools/check.mjs <id>`; capture exit status and findings. Manually check legibility, alignment, sprite origin, timing, transparency, consistency with the destination game, and reduced-motion implications if relevant. Automated pass ≠ artistic acceptance.
6. **Export:** `node tools/render.mjs <id> --sheet` for PNG/JSON exports. Record effect ID, pinned upstream revision, command/options/seed, source recipe, licenses, rendered preview and check results. Consult [asset package contract](../../docs/ASSET-PACKAGE.md).
7. **Handoff:** present the strongest variants and known limitations to the owner. Integrate into another repo only after explicit authorization. Use an immutable release/commit reference for handoff; don't merge or deploy automatically.

## Evidence requirements

Report observed vs untested: execution environment, reproducible commands, source refs, image/animation inspection method, technical checks, visual judgment, licensing/provenance, generated file paths, and any integration tests. Preserve editable source and recipes; a sprite sheet alone is insufficient.

## Failure behavior

If Node, renderer, image inspection, permissions, licenses, or real ChatGPT execution are unavailable, **stop only the blocked operation**, report what is missing, and offer the next feasible evidence-gathering action. Never pretend another agent has executed a command or invent a successful result. Do not incur external costs.

## Upstream credit

The underlying PixelFX generator and its skill are MIT-licensed; its [NOTICE](https://github.com/patch-gg/pixelfx/blob/main/NOTICE.md) identifies adapted Hugo Duprez and Hollow Crown components and an excluded proprietary font. Maintain appropriate MIT notices for any code actually copied/adapted; do not import the excluded font. See [NOTICE.md](../../NOTICE.md).
