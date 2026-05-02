# Google Doc sync checklist — Tier 1 edits

For when you (or anyone) opens the Google Doc and pastes the corrections back in. Order is **top-to-bottom of the document** — easiest to step through linearly.

For each row:
1. In the Doc, search (Ctrl+F / Cmd+F) the **Find** snippet.
2. Replace the matching sentence(s) with the **Replace** text.
3. On the corresponding Gonchar comment thread, paste the **Reply** line and click *Resolve*.

Suggested reply tone is brief and concrete — Gonchar will see the diff in track-changes anyway.

---

## 1. Executive Summary opener (Gonchar 1) — commit `e40464b`

**Find:** *"February of 2022 saw Russia's invasion of Ukraine, marking the first conventional warfare between European countries"*

**Replace with:**
> February of 2022 saw Russia's full-scale invasion of Ukraine — a major escalation of the war Russia had launched in 2014 with the seizure of Crimea and the incursion into the Donbas — and the first large-scale interstate conventional war in Europe in decades.

**Reply to Gonchar 1:** "Fixed — recast as the 2022 full-scale invasion / escalation of the 2014 war (Crimea + Donbas), and softened 'first conventional warfare' to 'first large-scale interstate conventional war in Europe in decades.'"

---

## 2. Introduction main paragraph (Gonchar 2) — commit `60e9506`

**Find:** *"its previous occupation of Crimea in 2014"* (also fixes "first conventional invasion of a European sovereign state since World War II")

**Replace the two opening sentences with:**
> Russia's full-scale invasion of Ukraine in 2022 broke a period of relative social and economic calm in Europe that its earlier 2014 invasion — the seizure of Crimea and the incursion into the Donbas, which simmered as an active conflict zone for the next eight years — had not. The 2022 escalation alarmed people, as it was the largest conventional war on European soil since World War II, and shook the complacent belief that peace in the post-Cold War era would be sustainable indefinitely.

**Reply to Gonchar 2:** "Fixed — named the full 2014 scope (Crimea + Donbas), characterised the 8-year continuity, reframed 2022 as escalation, and softened 'first conventional invasion since WWII' to 'largest conventional war on European soil since WWII.'"

---

## 3. Mellace miscitation in Introduction (Gonchar 4) — commit `115ae4a`

**Find:** *"(Cepparulo & Pasimeni, 2024; Mellace et al., 2025)"* — the parenthetical attached to the early-2022-cyclical-reaction sentence (NOT the one near the 2025 funding-surge paragraph; that one is correct).

**Replace with:**
> (Cepparulo & Pasimeni, 2024)

**Reply to Gonchar 4:** "Fixed — dropped Mellace from the cyclical-2022 sentence; their paper is about the 2025 US aid suspension, not 2022. Mellace's other in-text use later in the doc is in the correct 2025-funding context and was kept."

---

## 4. Lit Review cyclical-foil paragraph (Gonchar 11) — commit `b291b70`

**Find:** *"We can deduce here that if defence spending growth is stagnating"*

**Replace the entire sentence with:**
> One inference is that if defence spending growth stagnated and returned to trend (mean-reversion) even after Russia's 2014 invasion of Ukraine — which seized Crimea and opened a sustained war in the Donbas — then a similar reversion may follow the 2022 escalation.

**Reply to Gonchar 11:** "Fixed — replaced 'deduce' with 'One inference is that … may follow' (more tentative, appropriate for the foil); also corrected the 2014 framing to name both Crimea and Donbas."

---

## 5. Signalling Theory book-to-bill phrasing — commit `b0bdd25` (no Gonchar id; cohesion fix)

**Find:** *"as a ratio of total orders shipped"*

**Replace the sentence containing it with:**
> For example, the book-to-bill ratio reveals how many new orders the companies are receiving relative to revenue recognised in the same period — a tangible signal to the market of a real shift in demand, not only political but, perhaps more importantly, monetary.

(No Gonchar reply needed — this was an internal cohesion fix to align with the corrected book-to-bill definition below.)

---

## 6. Book-to-bill formula bullet (Gonchar 37) — commit `3ba9bd0`

**Find:** *"measures the proportion of recognised defence revenue to new defence orders"* — in the metric definitions list under *Mixed Methods → Financial Analysis → Methodology*.

**Replace the entire bullet with:**
> Defence book-to-bill ratio: the ratio of new defence orders booked in the period to defence revenue recognised in the same period (orders ÷ revenue). A value of 1.0 indicates that incoming orders are matching what is being billed out, so the order backlog is stable; a value above 1.0 indicates the backlog is growing (orders exceed deliveries), and a value below 1.0 indicates it is shrinking. As a forward-looking measure, it is a leading indicator of future revenue.

**Reply to Gonchar 37:** "Fixed — definition was inverted in prose (orders ÷ revenue, not the reverse). Numerical results in the paper are correct; only the prose was wrong."

---

## 7. "Eight of the ten companies" paragraph (Gonchar 40) — commit `2f05faf`

**Find:** *"areis best demonstrated"* (or *"3 additional5 companies"*) — both inside the *Contextualisation → Key Signalling Links* paragraph.

**Replace the whole sentence cluster from "The corollary…" through "(3 companies at the 5% level and 3 additional5 companies at the 10% level)" with:**
> The corollary to these semantic scores is best demonstrated by the book-to-bill ratio in the Welch test. As the most forward-looking financial metric, the book-to-bill ratio increased from 1.20 pre-invasion to 1.75 post-invasion and accelerated to 2.02 by 2025. The Chow test provides further compelling support for both findings. The results in Table 2 confirm a structural break (i.e., a shift in trend) between 2021 and 2022 in eight of the sixty company-metric cells — three at the 5% level and five marginally significant at the 10% level — covering six of the ten firms (Airbus, BAE Systems, Dassault Aviation, Leonardo, Rolls-Royce, and Thales).

**Reply to Gonchar 40:** "Fixed — corrected unit (cells, not firms): 8 of 60 firm-metric cells covering 6 of the 10 firms. Also fixed two stuck Track-Changes artifacts ('areis', 'compelling supports')."

---

## 8. "Nearly 40%" arithmetic (Gonchar 42) — commit `31af338`

**Find:** *"nearly 40%, from 7.8% pre-invasion to 10.5%"* — in the *Pre- and Post-Invasion Framing* paragraph.

**Replace the sentence with:**
> Adjusted EBIT margins rose substantially, by 2.7 percentage points (a relative increase of ≈35%), from 7.8% pre-invasion to 10.5% post-invasion.

**Reply to Gonchar 42:** "Fixed — recomputed as 2.7 percentage points / ≈35% relative ((10.5 − 7.8)/7.8 = 0.346). Standardised on percentage-points; same convention as the corresponding line earlier in Test 1."

---

## 9. Future Research sentence (Gonchar 43) — commit `a5dd61c`

**Find:** *"the magnitude of the 2022 invasion with that of the 2014 occupation of Crimea"* — in the limitations / future-work paragraph.

**Replace the sentence with:**
> One future study might decompose the cumulative impact of Russia's 2014 invasion of Ukraine — which seized Crimea and opened a sustained war in the Donbas — and the 2022 escalation, treating the eight intervening years of low-intensity conflict as a baseline against which the 2022 step-change in cyclical and structural inertia can be measured.

**Reply to Gonchar 43:** "Fixed — recast the proposed future study as a decomposition of the continuous 2014–2022 war into its two phases, naming the full 2014 scope (Crimea + Donbas) and treating 2022 as a step-change."

---

## 10. Conclusion line vs Howorth (Gonchar 45) — commit `064e4b3`

**Find:** *"Europe is no longer simply purchasing most of its defence needs from the United States"*

**Replace the surrounding sentences (the 2nd and 3rd sentences of the forecast paragraph) with:**
> While Europe remains dependent on the United States for a substantial share of new equipment procurement in the near term (Howorth, 2025), the financials of the top ten European defence contractors demonstrate a clear strategic shift toward greater defence self-reliance.

**Reply to Gonchar 45:** "Fixed — hedged the conclusion to acknowledge continued near-term US dependence, citing Howorth (2025) directly. Resolves the contradiction with the Literature Contradictions section."

---

## Quick reality check before submitting any of this back

- **No statistical results changed.** Every numerical claim in the paper is unchanged. Only prose, citations, and framing.
- **Eight Gonchar comment threads** can be flipped to *Resolved* once the above are pasted in: 1, 2, 4, 11, 37, 40, 42, 43, 45.
- **One internal cohesion edit** (item 5 above) has no Gonchar comment to resolve.
- **All other Gonchar comments remain open** — see `comments.md` for the full status, and `notes.md` for the prioritised punch list of what's queued next.

## What's NOT in this checklist (still to be done)

Tier 2 references, Tier 3 structural rewrite (12 steps in `RESTRUCTURE_PLAN.md`), Tier 4 wording fixes, Tier 5 referee-grade methodology work, Tier 6 journal-style cleanup. These will produce their own sync sheets when each batch lands.
