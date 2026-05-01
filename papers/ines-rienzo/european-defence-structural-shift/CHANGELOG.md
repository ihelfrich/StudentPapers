# Changelog — European Defence Structural Shift

Tracks every edit applied to `paper.md` after porting from the Google Doc.
One entry per edit. Entries are reverse-chronological under each section.

Format:
```
### YYYY-MM-DD — short title
- **Resolves:** Gonchar id(s) and/or referee-grade concern
- **Section:** where in the paper
- **Before:** exact prior text (≤2 lines)
- **After:** exact new text (≤2 lines)
- **Rationale:** why
- **Cohesion check:** what other passages were re-scanned for knock-on effects
- **Commit:** <git sha>
```

---

## Pending

These are queued. Each will be applied as its own commit.

### Q1 — Book-to-bill formula inverted (Gonchar id 37)
- **Section:** *Mixed Methods → Financial Analysis → Methodology* (metric definition list)
- **Before:** "Defence book-to-bill ratio: measures the proportion of recognised defence revenue to new defence orders."
- **After:** "Defence book-to-bill ratio: the ratio of new defence orders booked in the period to defence revenue recognised in the same period (orders ÷ revenue)…"
- **Rationale:** Standard finance definition is orders ÷ revenue, not the reverse. The numbers in the doc are correct; only the prose is inverted. Verified by cross-checking against the figure caption ("above 1.0 means order books are getting larger") and the signalling-theory paragraph, both of which describe the metric correctly.
- **Cohesion check needed:** confirm signalling-theory paragraph wording ("orders shipped" → "revenue recognised"), no recompute of Welch/Chow/Panel results.
- **Status:** ready to apply.

### Q2 — "eight of the ten companies" + "nearly 40%" + paragraph artifacts (Gonchar ids 40, 42)
- **Section:** *Contextualisation* paragraph beginning "In the semantic analysis, the mean score increases substantially…"
- **Three issues bundled:**
  1. "eight of the ten companies (3… and 3 additional5…)" — wrong unit (cells, not firms) and wrong arithmetic.
  2. "nearly 40%" — actual relative change is ≈35% ((10.5−7.8)/7.8 = 0.346).
  3. Stray edit artifacts: "scores areis", "compelling supports".
- **Blocking:** awaiting unique-firm count from Table 2 (how many of the 10 firms have ≥1 starred Chow cell?) before finalising new sentence.
- **Status:** queued; needs author/editor input.

---

## Applied

*(empty until first edit lands)*
