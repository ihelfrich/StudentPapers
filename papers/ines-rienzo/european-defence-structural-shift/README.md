# Did Russia's Invasion of Ukraine in February 2022 Create a Structural or Cyclical Shift in European Defence Companies?

**Author:** Inès Rienzo (IE University, Bachelor in Economics)
**Supervisor:** Prof. Patricia Gabaldón Quiñones
**Editor:** Dr. Elizaveta Gonchar
**Source of truth:** [Google Doc](https://docs.google.com/document/d/1fQtV1I4r3GJgnfDwWdCANBtkDuwVPNz1Tih-qAyWBb0/edit) — local Markdown port snapshot taken 2026-05-01.

## Files

| File | Purpose |
|------|---------|
| `paper.md` | Working draft (Markdown port of the Google Doc). All edits land here. |
| `summary.md` | One-page distillation. Refresh after substantive edits. |
| `notes.md` | Running critique punch list (JIE-grade referee concerns + Gonchar's themes). |
| `comments.md` | Mirror of all 56 inline comments from the Google Doc, with resolution status. |
| `CHANGELOG.md` | Every edit applied to `paper.md` — before, after, rationale, comment id, commit. |
| `figures/` | Image assets (currently empty; figures live in the Google Doc). |

## Editing workflow

1. **Locate** the passage with the `paper-locator` subagent (Haiku — fast, cheap, read-only).
2. **Edit** with the `paper-editor` subagent (Sonnet — applies the change, updates `CHANGELOG.md`, marks the comment resolved in `comments.md`, commits).
3. **Cohesion sweep** after each edit: editor agent re-scans related passages for knock-on inconsistencies.
4. **Sync back to the Google Doc** at checkpoints — paste edits in, reply to Gonchar's comment threads, mark them resolved there too.

## Conventions

- Keep edits **surgical** — fix the flagged paragraph(s); don't rewrite surrounding prose unless cohesion requires it.
- One commit per logical edit. Commit message format: `fix: <short> (Gonchar id N)` or `edit: <short> (referee: <topic>)`.
- Numbers and statistical claims must be reverified against the underlying tables before a fix is committed.
- When a fix changes a downstream claim, the cohesion sweep is mandatory and must be logged in the CHANGELOG entry.
