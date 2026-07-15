# Devin Federal Walkthroughs

Hands-on, self-contained walkthroughs for engineers evaluating **[Devin](https://docs.devin.ai) Desktop + CLI** on real-world codebases. Each walkthrough takes a concrete feature or task from first clone to a working result, showing off the surfaces you'd actually use — DeepWiki, Codemaps, Tab, Cascade (Ask / Plan / Build), AGENTS.md, Skills, and the CLI + MCP.

## Walkthroughs

| Walkthrough | Codebase | Stack | What you build |
|-------------|----------|-------|----------------|
| [**Open MCT — Favorites tray**](./openmct-favorites-tray/) | [NASA Open MCT](https://github.com/nasa/openmct) | JavaScript / Vue 3 | A right-click "Add to Favorites" action + a header tray listing pinned objects, end to end |

_More walkthroughs coming — each lives in its own folder with a self-contained README and assets._

## How these are organized

Every walkthrough is a self-contained folder:

```
<walkthrough-name>/
├── README.md      ← the map: what you build, prerequisites, quick start
└── ...            ← the walkthrough itself (HTML guide, assets, sample files)
```

New walkthroughs can start from the [`_template/`](./_template/) scaffold, which includes a README and lightweight HTML guide skeleton. Start with a walkthrough's `README.md`, then open its guide and follow along.

## Contributing — PRs and forks welcome

See **[CONTRIBUTING.md](./CONTRIBUTING.md)** for the full guide.

**These are living walkthroughs, and they get better when you make them better.** Spotted a typo, hit a step that didn't match your environment, found a cleaner prompt, or want to add a whole new walkthrough? Please contribute.

- 🐛 **Found something off?** [Open an issue](https://github.com/COG-GTM/Devin-Fed-Walkthroughs/issues) describing what you expected vs. what happened.
- 🔧 **Have a fix or improvement?** [Open a pull request](https://github.com/COG-GTM/Devin-Fed-Walkthroughs/pulls) — no change is too small. Typos, clearer wording, better screenshots, and updated commands are all welcome.
- ➕ **Want to add a walkthrough?** Drop a new folder with its own `README.md` following the layout above, add a row to the table here, and open a PR.
- 🍴 **Want to adapt one?** Fork the repo and remix any walkthrough for your own codebase, team, or stack — that's exactly what they're designed for.
- 💡 **Ideas and feedback?** Start a discussion or issue. We'd love to hear how you're using Devin and what would make these more useful.

### How to submit a PR

```bash
# Fork this repo on GitHub, then:
git clone https://github.com/<your-username>/Devin-Fed-Walkthroughs.git
cd Devin-Fed-Walkthroughs
git checkout -b my-improvement
# ...make your changes...
git commit -m "Describe your change"
git push origin my-improvement
# Then open a pull request from your fork on GitHub.
```

Don't worry about getting it perfect — open the PR and we'll iterate together.

## Related links

- **Devin docs** — <https://docs.devin.ai>
- **Devin Desktop docs** — <https://docs.devin.ai/desktop>

---

_Built by [Cognition](https://cognition.ai). Devin is Cognition's autonomous AI software engineer._
