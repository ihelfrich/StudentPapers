# StudentPapers

Shared workspace for students' research papers — drafted, reviewed, and distilled together.

## Layout

```
papers/<student>/<paper-slug>/
    paper.md      # the draft (Markdown)
    summary.md    # short distillation (≤1 page)
    notes.md      # optional: open questions, review notes
    refs.bib      # optional: citations
    figures/      # optional: images, diagrams
```

`templates/` holds starter files. Copy them into a new paper directory to begin.

## Workflow

1. **Start a paper.** Create `papers/<student>/<paper-slug>/` and copy the templates in.
2. **Draft in Markdown.** One sentence per line keeps diffs reviewable.
3. **Edit together.** Open a PR for substantive changes; small fixes can land directly on the working branch.
4. **Distill.** Keep `summary.md` in sync with the draft: problem, approach, key result, open questions.

## Conventions

- Use `kebab-case` for paper slugs (e.g. `attention-in-rnns`).
- Put figures in `figures/` and reference them with relative paths.
- Don't commit build artifacts (PDFs, `.aux`, etc.) — see `.gitignore`.
