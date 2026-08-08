# Kopano Labs Identity Recovery Plan

## Purpose

The 07 August production cutover repaired routing and deployment topology, but it also stripped too much of the existing Kopano Labs identity and Cars4Mars campaign asset system. This plan makes identity continuity a production invariant instead of a styling preference.

## Source lineage

### Kopano Labs institutional identity

Canonical brand sources remain in `Kopano-Labs/Introduction-to-MCP`:

- `Schematics/02-Strategy/Kopano Brand Identity.md`
- `Schematics/02-Strategy/Kopano Rebrand Plan.md`
- `public/index.html` — interactive canvas/cursor identity lineage
- `public/manifest-main.json` — later dark green/cyan PWA identity lineage

The exact institutional logo used on this branch was recovered from the Cars4Mars campaign strategy pack and is stored at:

- `assets/kopano-logo.webp`
- `assets/kopano-mark.svg`

### Cars4Mars foundation

The first mission-control implementation remains part of the product history:

- repository: `RobynAwesome/cars4mars-landingpage`
- foundation merge: `e4217d365133385fdeea0effb4234d7d5991b06a`
- PR #1 established the mission state tracker, campaign-media split, DFR-01 architecture, support allocation and technical front door.

That repository is retired as a production dependency, **not erased as source lineage**.

### Cars4Mars owned visual pack

Recovered from `Kopano_Labs_Cars4Mars_Public_Campaign_Strategy_2026-08-03.pdf`:

1. `assets/cars4mars/founder-kholofelo.webp` — real team-leader / founder portrait.
2. `assets/kopano-logo.webp` — Kopano Labs institutional identity.
3. `assets/cars4mars/founder-animated.webp` — supporting animated identity.
4. `assets/cars4mars/concept-art.webp` — cinematic concept artwork; never physical rover evidence.
5. `assets/cars4mars/campaign-hero.webp` — primary animated campaign identity.
6. `assets/cars4mars/official-logo.webp` — official Cars4Mars organiser identity, kept separate from Kopano Labs.

## Invariants

1. **Kopano Labs is the parent identity.** Campaign palettes may change; the parent studio logo and institutional identity do not disappear with them.
2. **Campaign colour does not recolour the institution.** Cars4Mars can be Mars orange while Kopano remains Kopano.
3. **Do not regenerate or retouch the real founder portrait as a substitute for the real asset.**
4. **Do not redraw the official Cars4Mars organiser logo into a Kopano asset.**
5. **Concept art is labelled as concept art.** It is not physical rover evidence.
6. **The public page is a campaign experience, not an audit argument.** Technical truth, evidence gates and state declarations live in Mission Control.
7. **Source lineage is additive.** Rebuilds inherit useful source code, assets and logic before introducing replacements.
8. **Interactivity must be functional.** A visual claiming to be interactive needs working controls, responsive behaviour and an explicit reduced-motion fallback.
9. **Identity regression is a CI failure.** The production gate checks for institutional logo assets, owned campaign media and identity tokens.
10. **No blind production overwrite.** Identity or major visual changes go through branch review and validation before production promotion.

## Current information architecture

- `/` — Kopano Labs institutional home.
- `/Cars4Mars/` — cinematic mission/campaign surface with interactive rover.
- `/Cars4Mars/Media/` — owned campaign media and identity roles.
- `/Cars4Mars/Mission-Control/` — technical baseline, state tracker, ledger and source lineage.
- `/reports/KOPANO_LABS.pdf` — public DFR-01 web copy.

## Review gate

Before merge:

- verify the exact Kopano institutional logo is visible on `/`, `/Cars4Mars/`, Media and Mission Control;
- verify all recovered Cars4Mars assets are non-zero and render locally;
- verify the Cars4Mars organiser logo remains distinct;
- verify Three.js rover orbit/zoom, assembled/exploded modes, system selection and camera views;
- verify mobile layout and `prefers-reduced-motion` behaviour;
- verify Mission Control retains the required truth-state strings and source lineage;
- verify `robots.txt`, sitemap and DFR-01 remain valid.
