# Reproducible VFX asset package — draft contract

A package is the handoff from creative production (ChatGPT or another executing agent) to game integration (Codex). **Preserve editable recipes, not only exported pixels.**

## Proposed package layout

```text
<effect-id>/
  recipe.json            # purpose, specification, options, seed, provenance
  source/                # original editable effect code / clearly licensed dependencies
  preview.png            # sampled contact sheet; optional animated preview
  sheet.png              # transparent frames
  sheet.json             # frames, durations, pivot, fps, loop and provenance as available
  validation.json        # actual checks, environment, results, known gaps
  README.md              # usage, integration hints, aesthetic acceptance status
```

Upstream render commands may produce different names; the packager should map and document them rather than imply those files were automatically emitted. Full copies of dependency code are optional; pinned immutable upstream references plus an independently reproducible build are preferred when licenses permit.

## Required metadata

- Stable asset ID and revision; destination project or "generic".
- Original creative specification, authored parameters, seeds, palette and frame dimensions.
- Source revision (including pinned PixelFX Git commit/tag) and exact generation/export commands.
- License, credit and provenance of adapted code, assets, references and excluded components.
- Frame duration, pivot, sheet layout and transparent background evidence.
- Validation results: what was run, pass/fail, visual inspection, and what remains unverified.
- Human creative approval status separate from technical verification.
- Instructions for regenerating from clean inputs.

## Acceptance gates

1. **Structural:** expected files exist; JSON parses; frames and pivot are internally consistent.
2. **Animation:** first frame, key impact, decay, end frame and loop seam as applicable are reviewed.
3. **Visual:** readable at destination display scale and consistent with approved art direction; **requires owner review** if claimed as accepted.
4. **Integration:** Codex tests use in the actual game only after a separately authorized integration task.
5. **Continuity:** source and deterministic recipe can be reconstructed after workspace loss.

No automatic publication. Don't copy PixelFX's excluded Patch Pixel font. Preserve relevant MIT licenses and upstream notices for adapted code.
