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

---

## Applied

### 2026-05-01 — Signalling Theory book-to-bill denominator corrected (cohesion follow-up Q1)
- **Resolves:** Gonchar id (none) / referee: cohesion-followup-Q1
- **Section:** Theoretical Frameworks → Signalling Theory
- **Before:** "…as a ratio of total orders shipped, which would signal to the market that there is a tangible change, not only politically but perhaps more importantly, monetarily."
- **After:** "…relative to revenue recognised in the same period — a tangible signal to the market of a real shift in demand, not only political but, perhaps more importantly, monetary."
- **Rationale:** The previous wording said the denominator was "total orders shipped". For a defence prime, revenue is recognised on percentage-of-completion or delivery — not literal physical shipment — and the standard book-to-bill denominator is revenue recognised (billed), not orders shipped. Aligns this passage with the corrected formula in the Methodology section (Q1 fix, commit 3ba9bd0, line 631).
- **Cohesion check:** Swept "orders shipped" (0 remaining occurrences — fully eliminated), "ratio of total orders" (0 occurrences), "revenue recognised" (lines 322 and 631 — both now consistent), "book-to-bill" (10 occurrences across lines 183, 189, 322, 631, 645, 668, 690, 719, 738, 748, 773 — all consistent with corrected definition). No contradicting passage found. No further follow-up required.
- **Commit:** b0bdd25

### 2026-05-01 — "nearly 40%" arithmetic corrected to ≈35% / 2.7 pp (Gonchar 42)
- **Resolves:** Gonchar id 42 / referee: (none — editor-flagged arithmetic)
- **Section:** Contextualisation of Mixed-Methods (Pre- and Post-Invasion Framing)
- **Before:** "Adjusted EBIT margins rose substantially, nearly 40%, from 7.8% pre-invasion to 10.5% post-invasion."
- **After:** "Adjusted EBIT margins rose substantially, by 2.7 percentage points (a relative increase of ≈35%), from 7.8% pre-invasion to 10.5% post-invasion."
- **Rationale:** The relative change is (10.5 − 7.8) / 7.8 = 0.346 ≈ 35%, not 40% as previously claimed (Gonchar id 42). I have also standardised on percentage points as the primary unit — mixing relative percent change with values that are themselves percentages (margins) is a common source of referee confusion. The same number is already correctly described elsewhere in the paper (line 645: "an increase of 2.7 percentage points"); this aligns the two passages.
- **Cohesion check:** Swept "nearly 40%" (0 remaining occurrences), "2.7 percentage points" (lines 645, 717 — both consistent with the corrected framing; line 645 already states the pp figure without any relative-% claim; line 717 uses 2.69 pp from the fixed-effects regression, which is consistent), "7.8% pre-invasion" (line 748 only — the edited sentence), "10.5% post-invasion" (line 748 only), "EBIT margin" (lines 183, 189, 645, 717, 748 — all consistent), "0.346" (no occurrences). No contradicting passage found. Line 189 reads "EBIT margin, which increased from 7.8 to 10.5% in the panel regression" with no relative-% claim — no conflict.
- **Commit:** 31af338

### 2026-05-01 — "eight of the ten companies" cell-vs-firm fix and artifact cleanup (Gonchar 40)
- **Resolves:** Gonchar id 40 / referee: (none — editor-flagged)
- **Section:** Contextualisation of Mixed-Methods (Key Signalling Links Between Analyses)
- **Before:** "The corollary to these semantic scores areis best demonstrated by the book-to-bill ratio in the Welch test. … The Chow test is further compelling supports of both findings. The results presented in Table 2, confirming a structural break (i.e., shift in trend) between 2021 and 2022 for eight of the ten companies within the sample (3 companies at the 5% level and 3 additional5 companies at the 10% level)."
- **After:** "The corollary to these semantic scores is best demonstrated by the book-to-bill ratio in the Welch test. … The Chow test provides further compelling support for both findings. The results in Table 2 confirm a structural break (i.e., a shift in trend) between 2021 and 2022 in eight of the sixty company-metric cells — three at the 5% level and five marginally significant at the 10% level — covering six of the ten firms (Airbus, BAE Systems, Dassault Aviation, Leonardo, Rolls-Royce, and Thales)."
- **Rationale:** Three problems resolved together: (1) "areis" was a stuck Track-Changes artifact; singular subject "the corollary" takes "is". (2) "The Chow test is further compelling supports" was syntactically broken; replaced with "provides further compelling support for". (3) The original fragment conflated company-metric cells with firms; Table 2 has 60 cells (10 firms × 6 metrics) of which 8 break (3 at 5%, 5 at 10%), spanning 6 unique firms. Gonchar 42 ("nearly 40%") is NOT resolved here — that is a separate sentence handled in Q2b.
- **Cohesion check:** Swept all six cohesion targets ("eight of the ten", "three companies at the 5%", "additional5", "areis", "compelling supports", "company-metric cells", "sixty company-metric") across paper.md. All matched only at line 738 (the edited sentence cluster). No other passage contradicts the new cell/firm distinction.
- **Commit:** 2f05faf

### 2026-05-01 — Book-to-bill formula corrected (Gonchar 37)
- **Resolves:** Gonchar id 37 / referee: (none — author/editor-flagged)
- **Section:** Mixed Methods → Financial Analysis → Methodology (metric definitions list)
- **Before:** "Defence book-to-bill ratio: measures the proportion of recognised defence revenue to new defence orders. A ratio of 1.0 indicates stability, while a ratio above 1.0 indicates growth."
- **After:** "Defence book-to-bill ratio: the ratio of new defence orders booked in the period to defence revenue recognised in the same period (orders ÷ revenue). A value of 1.0 indicates that incoming orders are matching what is being billed out, so the order backlog is stable; a value above 1.0 indicates the backlog is growing (orders exceed deliveries), and a value below 1.0 indicates it is shrinking. As a forward-looking measure, it is a leading indicator of future revenue."
- **Rationale:** The previous prose inverted the standard book-to-bill formula (it should be orders ÷ revenue, not revenue ÷ orders) and was internally contradictory: as written, "above 1.0" would actually have meant the backlog is shrinking. The numerical results in the paper (1.20 → 1.75 → 2.02) are consistent with the correct definition, so this is a prose-only fix; no statistical results need to be recomputed.
- **Cohesion check:** Swept "book-to-bill" (9 occurrences), "orders shipped" (1), "new orders" (2), "recognised defence revenue" (0 remaining). All other book-to-bill mentions (lines 183, 189, 645, 668, 690, 719, 738, 748, 773) are consistent with the corrected definition. One follow-up candidate flagged: line 322 (signalling-theory paragraph) reads "as a ratio of total orders shipped" — correct in spirit but imprecise; "shipped" should be "revenue recognised". This should be addressed as a separate edit.
- **Commit:** 3ba9bd0
