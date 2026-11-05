# Sources and notices

FX Creator's original orchestration instructions are informed by:

- [patch-gg/pixelfx](https://github.com/patch-gg/pixelfx), its [MIT-licensed skill](https://github.com/patch-gg/pixelfx/blob/main/skills/pixelfx/SKILL.md), and [authoring guide](https://github.com/patch-gg/pixelfx/blob/main/docs/AUTHORING.md).
- The procedural pixel VFX approach discussed by [Hugo Duprez / Sprite Fusion](https://www.spritefusion.com/pixel-art-vfx).

**No PixelFX generator source, pre-rendered VFX, or third-party fonts are vendored in this M0 documentation-only branch.** This file is a provenance pointer, not a claim that all upstream components are relicensable without conditions.

If later adapting or vendoring upstream code, copy the applicable MIT license and attribution, inspect the exact file headers and [upstream NOTICE](https://github.com/patch-gg/pixelfx/blob/main/NOTICE.md). The upstream NOTICE identifies:
- Hugo Duprez adaptations in `src/core/sim.js` and some effects.
- Hollow Crown adaptations in `src/core/act.js`.
- Patch Pixel font in `gallery/fonts`, excluded from upstream's general MIT grant; **do not copy by default**.

Record every actually imported component and source revision in the package. Our repository's MIT license applies to our original contributions and properly licensed portions only.
