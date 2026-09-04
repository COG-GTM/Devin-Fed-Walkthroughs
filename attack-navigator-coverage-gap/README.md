# MITRE ATT&CK Navigator × Devin — Desktop + CLI Walkthrough

A hands-on walkthrough for engineers evaluating **[Devin](https://docs.devin.ai) Desktop + CLI** in the FedRAMP boundary: ship a **Coverage Gap report** in [MITRE ATT&CK Navigator](https://github.com/mitre-attack/attack-navigator), the open-source tool SOCs, red teams and threat-intel analysts use to annotate ATT&CK matrices, from a bare machine to a working, on-screen feature.

The full, self-contained walkthrough lives in **[`navigator-walkthrough.html`](./navigator-walkthrough.html)**. Open it in any browser. This README is the map.

> Part of [**Devin Federal Walkthroughs**](../README.md). See the repo index for other walkthroughs.

---

## What you'll build

A **Coverage Gap report** sidebar panel in Navigator:

- Per-tactic counts of annotated vs. total techniques, with progress bars, for the layer you're working on
- An expandable list of the techniques you have *not* covered in each tactic
- A CSV export (`<layer>_coverage.csv`) with one row per tactic and a TOTAL row
- A parent technique counts as covered when any of its sub-techniques is annotated, matching how analysts read the matrix

The change runs through the whole stack: a calculation on the view model, a standalone Angular component, sidebar and toolbar wiring, a feature flag in `config.json`, and Karma/Jasmine specs.

Every part of the walkthrough serves that one result: **understand → plan → build → verify.**

## The throughline

| Part | Surface | Capability | What you do |
|------|---------|------------|-------------|
| 0 — Set up | Desktop (Plan mode) | Environment audit, clone, `npm ci` | Get Navigator running from a machine with only Devin installed |
| 1 — Understand | Desktop | DeepWiki, Codemaps, Tab, adding context | Map the toolbar → view model → sidebar chain the feature will follow |
| 2 — Plan | Desktop | Ask mode, Plan mode, model selection | Scope the feature and review the plan before any code is written |
| 3 — Build | Desktop | `AGENTS.md`, permission modes, images, mid-task redirects | Implement the feature to the repo's conventions |
| 4 — Extend | Desktop | Skills (`.devin/skills/`) | Create a pre-PR quality gate, modify it, add a layer-format review skill |
| 5 — Verify | Live browser | Click-path verification, terminal context | Confirm counts, gaps, the sub-technique rule and the CSV on screen; fix a compile error from terminal output |
| 6 — CLI | Terminal | Devin CLI, `/plan`, `/context`, `/compact`, MCP | Plan and build a layer-comparison stretch feature from the terminal with the same Skills |

The prompts in the guide are more explicit than you'd write day to day so a group lands on the same result; each major prompt also shows a looser version.

## Who it's for

Engineers who have completed the Devin Desktop 101 / 201 and Devin CLI 101 sessions and want to practise on a real codebase. Angular/TypeScript familiarity helps but is not required; the guide teaches Navigator's structure as you go. The cyber-defense domain makes the feature immediately relevant to detection-engineering and purple-team work.

## Prerequisites

- **Devin Desktop and/or the Devin CLI (FedRAMP builds)**: <https://windsurf.fedstart.com/install> and <https://windsurf.fedstart.com/install/cli>. Part 0 covers sign-in.
- **Node.js 22** and **Git**, installed through your organisation's approved software channel (the guide assumes package managers such as Homebrew are not available). Part 0 has the agent audit and install them.
- Nothing else: no Docker, database, account or API key. Navigator is a client-side app that reads ATT&CK data over HTTPS.

## Quick start

```bash
# 1. Clone Navigator
git clone https://github.com/mitre-attack/attack-navigator.git
cd attack-navigator
git checkout -b feature/coverage-gap-report

# 2. Install and run (from the Angular app directory)
cd nav-app
npm ci
npx ng serve --host 0.0.0.0 --port 4200    # http://localhost:4200
```

Then open **[`navigator-walkthrough.html`](./navigator-walkthrough.html)** from this folder and follow along from Part 0.

## Repository contents

| File | Purpose |
|------|---------|
| [`README.md`](./README.md) | Map of the walkthrough, prerequisites, and quick start |
| [`navigator-walkthrough.html`](./navigator-walkthrough.html) | The complete walkthrough: all seven parts, prompts, reference code, screenshots, quick reference and FAQ |

## Known limitation

Navigator's `ng lint` target references a removed TSLint builder upstream, so the guide's quality gate is Prettier plus the Karma test suite. This is disclosed in the FAQ.

## Contributing

See **[CONTRIBUTING.md](../CONTRIBUTING.md)** for how to fix this walkthrough or add another one.

## Related links

- **Codebase** — [MITRE ATT&CK Navigator](https://github.com/mitre-attack/attack-navigator)
- **ATT&CK** — <https://attack.mitre.org/>
- **Devin docs** — <https://docs.devin.ai>
- **Devin Desktop docs** — <https://docs.devin.ai/desktop>
- **Devin Federal** — <https://docs.devin.ai/federal/introduction>

---

_Built by [Cognition](https://cognition.ai). Devin is Cognition's autonomous AI software engineer. ATT&CK® and ATT&CK Navigator are © The MITRE Corporation._
