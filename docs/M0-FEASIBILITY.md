# M0 — Skill-first feasibility (Codex Offer / bounded spike)

**Status:** proposed; not an authorization for full implementation or changes to game repositories.  
**Product goal:** ChatGPT should eventually be able to create, review and package original pixel VFX from a conversation, with Codex freed from repetitive visual production.  
**Scope:** prove the minimum practical workflow before building installers, MCP services, plugins, or replacement renderers.

## Sources to inspect

1. [PixelFX repository](https://github.com/patch-gg/pixelfx), including `skills/pixelfx/SKILL.md`, `docs/AUTHORING.md`, `tools/new.mjs`, `tools/render.mjs`, `tools/check.mjs`, `NOTICE.md`, and license.
2. [This skill](../skills/fx-creator/SKILL.md) and [asset contract](ASSET-PACKAGE.md).
3. [AICP](https://github.com/jaychtw/game-development-standards/blob/main/AI-COLLABORATION-PROTOCOL.md) and [UGDS](https://github.com/jaychtw/game-development-standards/blob/main/UGDS.md); pin immutable revisions and follow working-branch discipline.
4. Available installed asset-production tooling, if discoverable in the actual workspace. Don't assume a ChatGPT-only installation is accessible to Codex.

## Explore and Offer

Before implementing, report:
- How the upstream skill and tooling actually work; license obligations and what must not be copied.
- How Codex can run the CLI, and whether ChatGPT in the owner's chat environment can run the same engine (verified, unverified, or blocked—never inferred).
- Minimal adaptations needed to support our creative direction and project-agnostic reproducibility.
- Options and tradeoffs for an approved, **no-cost**, local-first POC; failure modes and test plan.
- Specific owner approval needed before moving from Offer into code execution, or a tightly bounded evidence spike already authorized by a subsequent brief.

## Candidate first POC (requires authorization after Offer)

An **original** heavy cannon impact for Armorheart as an isolated FX Creator artifact. No edits to Armorheart's repo and no deployment.

Expected evidence:
1. Three visual variants or a written, evidence-backed reason to reduce the number.
2. Demonstrated render + image inspection + bounded refinement.
3. `check.mjs` results, with actual commands and exit codes.
4. Reproducible source and one PNG sprite sheet + JSON metadata + preview.
5. A clean-checkout/reconstruction attempt at the pinned upstream revision where feasible.
6. An exact statement of whether ChatGPT could independently operate the tool (not merely generate a brief).

## Stop/escalate

Stop for paid services, unsupported ChatGPT plugin assumptions, license uncertainty, unsatisfied image-inspection access, or material change in creative direction. Do not claim cross-session availability without testing in a fresh session. Do not merge, deploy, change project assets, or build a new rendering engine by default.

## Proposed completion gate

M0 ends with a credible Offer and a reviewable experiment plan. A working sample alone does not prove integration into ChatGPT; this must be separately tested with the actual conversation/runtime tooling.
