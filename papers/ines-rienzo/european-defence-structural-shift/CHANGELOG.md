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

### 2026-05-02 — Top-level heading rename: # Literature Review → # 3. Background (Tier 3 Step 1/12)
- **Resolves:** Gonchar id (none — multi-step; id 5 will be closed at end of Phase B/C) / referee: tier-3-structure-step-1-of-12
- **Section:** Top-level heading rename: # Literature Review → # 3. Background (Tier 3 Step 1/12)
- **Before:** "# **Literature Review**"
- **After:** "# **3. Background**"
- **Rationale:** Per Gonchar (id 5, restructure plan in `RESTRUCTURE_PLAN.md`), the current `# Literature Review` section actually reads as Background (history of European defence + history of Russia's invasion + the post-invasion response). It is being renamed to `# 3. Background`; a fresh `# 4. Literature Review` will be inserted later (Step 8) to position the question and methods against prior work. This is the first edit in a 12-step structural rewrite series and is intentionally minimal — only the heading text changes; the section's contents stay put for now.
- **Cohesion check:** Swept "Literature Review", "Background", and "Historical Baseline". One remaining "Literature Review" occurrence at line 81 (TOC entry: `[**Literature Review** **10**](…)`) — this is the TOC link, which will be rebuilt in Step 11 of this series; deliberately left untouched. "Background" now appears only at line 208 (the renamed heading itself); no conflict. "Historical Baseline" appears at line 83 (TOC entry) and line 212 (subsection heading `## **Historical Baseline**`); neither conflicts with the rename. No in-text cross-references found that use "Literature Review" as a broken pointer outside of the TOC. No follow-up edits triggered by this step.
- **Commit:** 2ba80be

### 2026-05-01 — Future Research sentence: 2014 full scope and 2022 as escalation (Gonchar 43)
- **Resolves:** Gonchar id 43 / referee: factual-2014-framing
- **Section:** Conclusion → Limitations and Future Research (line 777)
- **Before:** "One future study might compare the magnitude of the 2022 invasion with that of the 2014 occupation of Crimea in terms of impact on cyclical and structural inertia in companies."
- **After:** "One future study might decompose the cumulative impact of Russia's 2014 invasion of Ukraine — which seized Crimea and opened a sustained war in the Donbas — and the 2022 escalation, treating the eight intervening years of low-intensity conflict as a baseline against which the 2022 step-change in cyclical and structural inertia can be measured."
- **Rationale:** Per Gonchar (id 43), the prior wording ("the 2022 invasion vs the 2014 occupation of Crimea") was wrong on two counts: (i) the 2014 invasion was not only Crimea — it included the Donbas — and (ii) it did not end before 2022; the 2022 escalation was a major expansion of an ongoing war. The replacement reframes the proposed future study as a decomposition of one continuous war into its 2014 and 2022 phases, names the full 2014 scope, and characterises 2022 as a "step-change" / "escalation" rather than a separate event. Closes the last instance of the Crimea-only framing in the paper.
- **Cohesion check:** Swept all five targets. (1) "occupation of Crimea" — 0 occurrences remaining; fully eliminated from paper.md. (2) "the 2014 occupation" — 0 occurrences remaining; fully eliminated. (3) "the 2022 invasion" — 2 occurrences remain: line 177 (Executive Summary: "the 2022 invasion indicate a cyclical shift or a structural one?" — shorthand in a research question, no factual claim; no conflict) and line 463 (figure caption date-marker, no factual claim; no conflict). (4) "magnitude of the 2022" — 0 occurrences remaining; fully eliminated. (5) "cyclical and structural inertia" — 1 occurrence at line 777 (the edited sentence itself); no contradiction. No cohesion flags raised. This is the final edit in the 2014-framing series (Gonchar 1, 2, 11, 43).
- **Commit:** a5dd61c

### 2026-05-01 — "We can deduce" foil sentence: verb and 2014 scope corrected (Gonchar 11)
- **Resolves:** Gonchar id 11 / referee: factual-2014-framing
- **Section:** Literature Review → Evidence of a Cyclical Shift (foil paragraph, line 240)
- **Before:** "We can deduce here that if defence spending growth is stagnating and returning to a trend level of no growth (mean-reversion) even after the Russian invasion of Crimea in 2014, then perhaps the same scenario will occur with the 2022 invasion as well."
- **After:** "One inference is that if defence spending growth stagnated and returned to trend (mean-reversion) even after Russia's 2014 invasion of Ukraine — which seized Crimea and opened a sustained war in the Donbas — then a similar reversion may follow the 2022 escalation."
- **Rationale:** Two corrections in one surgical edit. (1) Gonchar 11 (word-choice): "deduce" replaced with "One inference is that … may follow," which is appropriately tentative for this foil paragraph presenting the cyclical hypothesis. (2) Referee-cohesion link to Gonchar 2 (resolved at commit 60e9506, line 200): this sentence contained a parallel "Crimea-only" characterisation of 2014; the new wording names both fronts (Crimea + Donbas) and characterises the eight-year continuity, consistent with the line-200 fix. The direction of the inference (mean-reversion expected as a foil the rest of the paper argues against) is deliberately preserved. "The 2022 invasion" is reframed as "the 2022 escalation," consistent with the series-wide framing.
- **Cohesion check:** Swept all six targets. (1) "We can deduce" — 0 occurrences remaining; fully eliminated. (2) "Russian invasion of Crimea" — 0 occurrences remaining; fully eliminated. (3) "invasion of Crimea in 2014" — 0 occurrences remaining; fully eliminated. (4) "mean-reversion" — 1 occurrence at line 240 (the edited sentence itself); no other occurrence; no conflict. (5) "the 2022 invasion" — 3 occurrences: line 177 (Executive Summary, already reads "full-scale invasion … escalation," consistent), line 463 (figure caption date-marker, no factual claim, no conflict), line 777 (Future Research paragraph: "the 2014 occupation of Crimea" — this is the Gonchar 43 / edit-4 target, already flagged; no new issue). (6) "the same scenario will occur" — 0 occurrences remaining; fully eliminated. One standing cohesion flag: line 777 "2014 occupation of Crimea" (Gonchar 43) remains the edit-4 target, unresolved.
- **Commit:** b291b70

### 2026-05-01 — Introduction opener recast: full 2014 scope named; 2022 as escalation (Gonchar 2)
- **Resolves:** Gonchar id 2 / referee: factual-2014-framing
- **Section:** Introduction (opening of main paragraph, line 200)
- **Before:** "Russia's invasion of Ukraine in 2022 broke a period of relative social and economic calm in Europe, which its previous occupation of Crimea in 2014 had not engendered. The new war alarmed people, as it was the first conventional invasion of a European sovereign state since World War II…"
- **After:** "Russia's full-scale invasion of Ukraine in 2022 broke a period of relative social and economic calm in Europe that its earlier 2014 invasion — the seizure of Crimea and the incursion into the Donbas, which simmered as an active conflict zone for the next eight years — had not. The 2022 escalation alarmed people, as it was the largest conventional war on European soil since World War II…"
- **Rationale:** Per Gonchar (id 2), framing 2014 only as an "occupation of Crimea" is incorrect — Russia also invaded eastern Ukraine, which remained an active conflict zone through 2022. The replacement (i) names the full 2014 scope (Crimea + Donbas), (ii) acknowledges the eight-year continuity of low-intensity war, (iii) reframes 2022 as an "escalation" rather than a separate event, and (iv) softens the historical-significance claim from "first conventional invasion of a European sovereign state since WWII" to "largest conventional war on European soil since WWII," which is more defensible given other post-WWII conflicts (Yugoslavia, Hungary 1956, Czechoslovakia 1968). Brings the passage into agreement with the corrected Executive Summary opener (commit e40464b, line 177).
- **Cohesion check:** Swept all six targets. (1) "previous occupation of Crimea" — 0 occurrences remaining; fully eliminated. (2) "occupation of Crimea" — 1 occurrence at line 777: "the 2014 occupation of Crimea" in the Future Research paragraph; this is the edit-4 target (Gonchar 43, pending). Not touched here. (3) "first conventional invasion" — 0 occurrences remaining; fully eliminated. (4) "since World War II" — 2 occurrences: line 177 (Executive Summary, already reads "first large-scale interstate conventional war in Europe in decades" — consistent) and line 200 (the edited sentence, now reads "largest conventional war on European soil since World War II" — correct). No conflict. (5) "in contrast to 2014" — 1 occurrence at line 200, third sentence of the same paragraph: "and in contrast to 2014, Ukraine would now need to enlist support and devote resources to maintain its sovereignty." This sentence contrasts the two episodes' international response, not their scope; it is coherent with the new opener and was deliberately left untouched per caller instruction. No conflict. (6) "Donbas" — 2 occurrences: line 177 (edit-1 result, consistent) and line 200 (the new text, correct). No conflict. The rest of the line-200 paragraph (sentences 3–7: NATO upheaval, economic impact, capital influx, committed security upgrade) is untouched and reads coherently after the new opener. One cohesion flag raised: line 777 "2014 occupation of Crimea" (Gonchar 43) — remains the edit-4 target, unresolved.
- **Commit:** 60e9506

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
