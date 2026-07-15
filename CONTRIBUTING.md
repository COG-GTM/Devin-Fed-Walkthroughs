# Contributing to Devin Federal Walkthroughs

These are living walkthroughs for working with Devin on real codebases. All contributions are welcome — from a typo fix to a whole new walkthrough.

## Ways to contribute

- 🛠️ **Fix or improve an existing walkthrough** — clarify a step, update a command, or correct an outdated link.
- ➕ **Add a new walkthrough** — use the [`_template/`](./_template/) scaffold and share a concrete, end-to-end task.
- 🐛 **Report an issue** — tell us which walkthrough and step failed, what you expected, and what happened.
- 💡 **Share an idea** — suggest a codebase, Devin surface, or workflow that would make a useful walkthrough.

## Repository layout

Each walkthrough is a self-contained folder with its own `README.md` plus the guide and any assets it needs:

```text
<walkthrough-name>/
├── README.md
├── walkthrough.html
└── ...                  # assets, sample files, or other guide material
```

The [`_template/`](./_template/) folder is a starter scaffold for new walkthroughs. It is not itself a walkthrough and does not appear in the root index table.

## Adding a new walkthrough

1. Copy `_template/` to a new folder using a lowercase-kebab-case name:
   ```bash
   cp -R _template/ your-walkthrough-name/
   ```
2. Fill in `your-walkthrough-name/README.md` and `your-walkthrough-name/walkthrough.html`.
3. Add a row for the walkthrough to the [Walkthroughs table](./README.md#walkthroughs) in the root README.
4. Open a pull request from your fork.

Use lowercase-kebab-case folder names such as `openmct-favorites-tray` or `cobol-ledger-modernization`.

## What makes a good walkthrough

Use this checklist before opening a PR:

- [ ] It is self-contained and tells the reader what to do without relying on hidden context.
- [ ] It uses a real codebase, with a link to the source repository.
- [ ] It produces a concrete end result the reader can inspect.
- [ ] It follows the **understand → plan → build → verify** throughline.
- [ ] It shows specific Devin surfaces, as relevant: DeepWiki, Codemaps, Tab, Cascade Ask/Plan/Build, `AGENTS.md`, Skills, and CLI + MCP.
- [ ] It lists prerequisites and includes a quick start.
- [ ] It includes a verification step that checks the result.

## Submitting a PR

Fork the repository, create a branch, make the change, and push it from your fork:

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

Before opening the PR:

- [ ] A walkthrough README is included or updated.
- [ ] A new walkthrough has a row in the root README table.
- [ ] Relative links work.
- [ ] The new walkthrough follows the template.

## Local review before you open a PR

Preview Markdown in your editor or with a local Markdown viewer. For a quick browser review, use a Markdown CLI such as `grip`:

```bash
grip README.md
```

Then open the local URL it prints. Open an HTML guide directly in a browser:

```bash
python3 -m http.server 8000
```

Visit `http://localhost:8000/` and open the walkthrough's `walkthrough.html`. Check headings, tables, code blocks, and every relative link before you push.

## Related links

- **Devin docs** — <https://docs.devin.ai>
- **Devin Desktop docs** — <https://docs.devin.ai/desktop>

---

_Built by [Cognition](https://cognition.ai). Devin is Cognition's autonomous AI software engineer._
