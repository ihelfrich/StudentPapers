# Contributing

## Starting a new paper

```bash
mkdir -p papers/<student>/<paper-slug>/figures
cp templates/paper.md    papers/<student>/<paper-slug>/paper.md
cp templates/summary.md  papers/<student>/<paper-slug>/summary.md
cp templates/notes.md    papers/<student>/<paper-slug>/notes.md
```

## Editing together

- **Branch naming:** `<student>/<paper-slug>` for the working branch, `review/<paper-slug>` for review passes.
- **Commits:** keep them small and descriptive (e.g. `tighten methods section`, `add figure 2`).
- **PRs:** open one when a section is ready for review. Tag the author and any reviewers.
- **Diffs are easier to read** when each sentence is on its own line — Markdown renders the same either way.

## Distilling

After meaningful edits to `paper.md`, refresh `summary.md`:
- Problem (1–2 sentences)
- Approach (3–5 sentences)
- Key result (1 sentence + the number/claim)
- Why it matters (1–2 sentences)
- Open questions (bullets)

Aim for ≤1 page. The summary is what we'll skim before group meetings.
