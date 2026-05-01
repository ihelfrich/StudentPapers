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

### 2026-05-01 — Book-to-bill formula corrected (Gonchar 37)
- **Resolves:** Gonchar id 37 / referee: (none — author/editor-flagged)
- **Section:** Mixed Methods → Financial Analysis → Methodology (metric definitions list)
- **Before:** "Defence book-to-bill ratio: measures the proportion of recognised defence revenue to new defence orders. A ratio of 1.0 indicates stability, while a ratio above 1.0 indicates growth."
- **After:** "Defence book-to-bill ratio: the ratio of new defence orders booked in the period to defence revenue recognised in the same period (orders ÷ revenue). A value of 1.0 indicates that incoming orders are matching what is being billed out, so the order backlog is stable; a value above 1.0 indicates the backlog is growing (orders exceed deliveries), and a value below 1.0 indicates it is shrinking. As a forward-looking measure, it is a leading indicator of future revenue."
- **Rationale:** The previous prose inverted the standard book-to-bill formula (it should be orders ÷ revenue, not revenue ÷ orders) and was internally contradictory: as written, "above 1.0" would actually have meant the backlog is shrinking. The numerical results in the paper (1.20 → 1.75 → 2.02) are consistent with the correct definition, so this is a prose-only fix; no statistical results need to be recomputed.
- **Cohesion check:** Swept "book-to-bill" (9 occurrences), "orders shipped" (1), "new orders" (2), "recognised defence revenue" (0 remaining). All other book-to-bill mentions (lines 183, 189, 645, 668, 690, 719, 738, 748, 773) are consistent with the corrected definition. One follow-up candidate flagged: line 322 (signalling-theory paragraph) reads "as a ratio of total orders shipped" — correct in spirit but imprecise; "shipped" should be "revenue recognised". This should be addressed as a separate edit.
- **Commit:** <fill in after committing>
