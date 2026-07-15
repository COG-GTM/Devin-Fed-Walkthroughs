# NASA Open MCT × Devin — Desktop + CLI Walkthrough

A hands-on walkthrough for engineers evaluating **[Devin](https://docs.devin.ai) Desktop + CLI**: ship a real **"Favorites" tray** feature to [NASA's Open MCT](https://github.com/nasa/openmct) — the open-source mission control framework used for spacecraft telemetry visualization — from first clone to a working, on-screen feature.

The full, self-contained walkthrough lives in **[`openmct-walkthrough (1).html`](./openmct-walkthrough%20(1).html)** — open it in any browser. This README is the map.

---

## What you'll build

A **Favorites** feature in Open MCT, end to end:

- A right-click **"Add to Favorites"** action on any object in the tree
- A new **header tray** that lists what you've pinned, with click-to-navigate
- **Persistence** across reloads

Every part of the walkthrough serves that one feature: **understand → plan → build → verify.**

## The throughline

| Part | Surface | Capability | What you do |
|------|---------|------------|-------------|
| 0 — Set up | Desktop | Clone, Devin CLI install, `npm install` | Get Open MCT open and running |
| 1 — Understand | Desktop | DeepWiki, Codemaps, Tab | Explain the plugin architecture; map how a plugin contributes UI |
| 2 — Plan | Desktop | Cascade: Ask + Plan modes | Scope the feature without touching code |
| 3 — Build | Desktop | AGENTS.md, permission modes | Implement the feature to the repo's conventions |
| 4 — Extend | Desktop | Skills (`.devin/skills/`) | Encode a reusable pre-PR quality gate |
| 5 — Verify | Live browser | Manual verification | Confirm the feature works on screen |
| 6 — CLI | Terminal | Devin CLI + MCP | Run the same workflow from the terminal |

## Who it's for

Engineers evaluating Devin Desktop + CLI — especially those working in JavaScript / Vue 3 codebases. No prior Open MCT knowledge required; the walkthrough teaches the plugin architecture as you go, and the same skills transfer to any repo you bring.

## Prerequisites

- **Node.js ≥ 24.14.1** — Open MCT pins the exact version in its `.nvmrc`, so `nvm install` picks it up automatically.
- **Devin Desktop and/or the Devin CLI** — install instructions are in Part 0 of the walkthrough.
  - FedRAMP users: <https://windsurf.fedstart.com/install/cli>
  - Everyone else: see the [CLI quickstart](https://docs.devin.ai).

## Quick start

```bash
# 1. Clone Open MCT (the app you'll be building in)
git clone https://github.com/nasa/openmct.git
cd openmct

# 2. Use the pinned Node version, install, and run
nvm install
npm install
npm start        # dev server at http://localhost:8080/
```

Then open **[`openmct-walkthrough (1).html`](./openmct-walkthrough%20(1).html)** from this repo and follow along from Part 0.

## Repository contents

| File | Purpose |
|------|---------|
| `openmct-walkthrough (1).html` | The complete walkthrough — all six parts, prompts, code snippets, quick reference, and FAQ |
| `README.md` | This overview |

---

## Contributing — PRs and forks welcome

**This is a living walkthrough, and it gets better when you make it better.** Whether you spotted a typo, hit a step that didn't match your environment, found a cleaner prompt, or want to add a whole new section — please contribute.

- 🐛 **Found something off?** [Open an issue](https://github.com/COG-GTM/nasa-openmtc-walkthrough/issues) describing what you expected vs. what happened.
- 🔧 **Have a fix or improvement?** [Open a pull request](https://github.com/COG-GTM/nasa-openmtc-walkthrough/pulls) — no change is too small. Typos, clearer wording, better screenshots, updated commands, and new steps are all welcome.
- 🍴 **Want to adapt it?** Fork the repo and remix the walkthrough for your own codebase, team, or stack. That's exactly what it's designed for — the workflow (understand → plan → build → verify) applies to any repo, not just Open MCT.
- 💡 **Ideas and feedback?** Start a discussion or issue. We'd love to hear how you're using Devin and what would make this walkthrough more useful.

### How to submit a PR

```bash
# Fork this repo on GitHub, then:
git clone https://github.com/<your-username>/nasa-openmtc-walkthrough.git
cd nasa-openmtc-walkthrough
git checkout -b my-improvement
# ...make your changes...
git commit -m "Describe your change"
git push origin my-improvement
# Then open a pull request from your fork on GitHub.
```

Don't worry about getting it perfect — open the PR and we'll iterate together. Every contribution, big or small, is appreciated.

---

## Related links

- **Open MCT** — <https://github.com/nasa/openmct>
- **Devin docs** — <https://docs.devin.ai>
- **Devin Desktop docs** — <https://docs.devin.ai/desktop>

---

_Built by [Cognition](https://cognition.ai). Devin is Cognition's autonomous AI software engineer._
