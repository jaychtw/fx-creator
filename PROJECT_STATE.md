# FX Creator — project state

**Date:** 2026-11-05  
**Phase:** M0 documentation / feasibility offer preparation  
**Acceptance:** not yet reviewed or approved for implementation  
**Repository:** https://github.com/jaychtw/fx-creator

## Confirmed baseline

- Initial repository contained only README and MIT license before this working-branch proposal.
- Product direction from owner: ChatGPT-first conversational production, reuse existing PixelFX methods via an adapted skill, Codex primarily for tool engineering/integration; minimize cost and human repetitive work.
- Scope for first bounded experiment: original pixel-art cannon impact, generated without changing an existing game.
- No FX Creator code, generated sprite sheets, live plugin, or verified end-to-end ChatGPT operation yet.

## Proposed architecture

One skill (`skills/fx-creator/SKILL.md`) orchestrating an external, pinned PixelFX checkout. A small reversible proof of execution precedes any custom installer, integration service, or replacement renderer.

## Authority and next action

This branch records the product concept, adapted skill instructions, provenance and candidate Codex Offer. Owner review of the PR is the next decision gate. Codex should first conduct a scoped feasibility assessment and return an Offer. Full POC implementation, game integration and deployment remain separate approvals.

## Standards and evidence

- [AICP](https://github.com/jaychtw/game-development-standards/blob/main/AI-COLLABORATION-PROTOCOL.md) and [UGDS](https://github.com/jaychtw/game-development-standards/blob/main/UGDS.md) read for current process guidance; exact immutable standard pins must be captured when implementation starts.
- No build, render, package, or runtime tests have been performed for FX Creator.
