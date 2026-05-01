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

### 2026-05-01 — Executive Summary opener recast: 2022 as escalation of 2014 war (Gonchar 1)
- **Resolves:** Gonchar id 1 / referee: factual-2014-framing
- **Section:** Executive Summary (opening)
- **Before:** " February of 2022 saw Russia's invasion of Ukraine, marking the first conventional warfare between European countries, and the continent suddenly awoke to a seismic shift from the status quo."
- **After:** " February of 2022 saw Russia's full-scale invasion of Ukraine — a major escalation of the war Russia had launched in 2014 with the seizure of Crimea and the incursion into the Donbas — and the first large-scale interstate conventional war in Europe in decades. The continent suddenly awoke to a seismic shift from the status quo."
- **Rationale:** Per Gonchar (id 1), the previous opening misstated two facts: (a) Russia first invaded Ukraine in 2014, not 2022, and (b) "first conventional warfare between European countries" is incorrect without a temporal qualifier. The replacement (i) frames 2022 as a "full-scale invasion" / "escalation" rather than the start of the conflict, (ii) explicitly names both the 2014 seizure of Crimea and the incursion into the Donbas, and (iii) hedges the historical-significance claim to "first large-scale interstate conventional war in Europe in decades."
- **Cohesion check:** Swept all six targets. (1) "first conventional warfare" / "first conventional invasion" — line 200 retains "first conventional invasion of a European sovereign state since World War II"; this is the edit-2 target in this series, to be addressed separately. (2) "Russia's invasion of Ukraine" — line 177 now correct; line 200 opens "Russia's invasion of Ukraine in 2022 broke a period of relative social and economic calm… which its previous occupation of Crimea in 2014 had not engendered" — this frames the two events as related but still implies the calm-breaking force was uniquely 2022; edit-2 target. Line 202 reads "did Russia's invasion of Ukraine in February 2022 create a structural or cyclical shift" — this is the research-question sentence and is acceptable as shorthand; no contradiction. Lines 306 and 1258 similarly use "Russia's invasion" as research-question shorthand; no conflict. (3) "since World War II" — line 200 reads "first conventional invasion of a European sovereign state since World War II"; this needs the same temporal hedge as line 177 received (edit-2 target). (4) "occupation of Crimea" — line 200 uses "previous occupation of Crimea in 2014 had not engendered [calm-breaking]"; this partially contradicts the 2014-as-war framing (edit-2 target). Line 777 reads "compare the magnitude of the 2022 invasion with that of the 2014 occupation of Crimea" — this also omits the Donbas; edit-4 target (Gonchar 43, per notes.md). (5) "since 2014" — no free-standing occurrences found; no conflict. Three cohesion flags raised for follow-up edits 2, 3, and 4 of the "2014 framing" series.
- **Commit:** e40464b

### 2026-05-01 — Conclusion overclaim hedged with Howorth (2025) near-term dependence caveat (Gonchar 45)
- **Resolves:** Gonchar id 45 / referee: causal-language-and-overclaim
- **Section:** Conclusion (closing paragraph of forecast)
- **Before:** "…Europe is no longer simply purchasing most of its defence needs from the United States. A clear and strategic plan for defence self-reliance is being demonstrated through the financials of the top ten European defence contractors."
- **After:** "While Europe remains dependent on the United States for a substantial share of new equipment procurement in the near term (Howorth, 2025), the financials of the top ten European defence contractors demonstrate a clear strategic shift toward greater defence self-reliance."
- **Rationale:** The previous conclusion sentence overstated the degree of European autonomy and directly contradicted the paper's own Literature Contradictions paragraph (line 288), which cites Howorth (2025) for the claim that European forces purchased the vast majority of new equipment from US companies during the early Ukraine response. The hedged version preserves the structural-shift claim while explicitly acknowledging continued near-term US dependence and citing Howorth (2025) for that fact.
- **Cohesion check:** Swept "no longer simply purchasing" (0 remaining occurrences — eliminated), "Howorth" (lines 288 and 294 — both in Literature Contradictions, consistent with the caveat now added to the Conclusion; References line 884 — correct entry), "self-reliance" (line 177 — aspirational framing in Introduction, no contradiction; line 783 — the edited sentence, now hedged), "fundamental shift" (line 783 only — the edited sentence, retained), "United States" (line 288 — states EU "still heavily reliant on the United States from a military defence perspective", consistent with new Conclusion hedging; line 783 — edited sentence), "vast majority of their new equipment" (line 288 only — Literature Contradictions paragraph, still intact and now echoed by the Conclusion). No remaining passage contradicts the edit. One cohesion flag raised: line 294 closes with "the European defence industry has crossed a point of no return… a well-funded, united force ready for long-term global security" — this is in the Literature Review's synthesis paragraph and carries its own hedging via attribution ("the research overwhelmingly agrees"); it does not make an autonomous over-claim, but it sits close to the tension and should be reviewed in the Conclusion expansion (Gonchar 44).
- **Commit:** 064e4b3

### 2026-05-01 — Mellace et al. (2025) miscitation dropped from Introduction (Gonchar 4)
- **Resolves:** Gonchar id 4 / referee: (none — editor-flagged)
- **Section:** Introduction
- **Before:** "…to respond to a crisis situation (Cepparulo & Pasimeni, 2024; Mellace et al., 2025)."
- **After:** "…to respond to a crisis situation (Cepparulo & Pasimeni, 2024)."
- **Rationale:** Mellace et al. (2025) studies the suspension of US aid to Ukraine in early 2025 — it does not document the cyclical 2022 reaction the sentence is describing. Per Gonchar (id 4) the citation here is incorrect. Removing it; Cepparulo & Pasimeni (2024) remains as the supporting citation for the cyclical-reaction claim. Mellace's other in-text appearance at line 246 is in the correct 2025 funding-context paragraph and is left intact, as is the References entry.
- **Cohesion check:** Swept "Mellace" (1 remaining occurrence — line 246, correct context; References entry line 908 also correct), "Cepparulo & Pasimeni" (lines 204, 230, 236 — all consistent, no conflict), "early reaction" (line 204 only — the edited sentence), "cyclical" (17 occurrences across Introduction, Literature Review, Methodology, Results, Discussion — none are linked to the now-removed citation; no contradicting passage found). No follow-up edits required.
- **Commit:** 115ae4a

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
