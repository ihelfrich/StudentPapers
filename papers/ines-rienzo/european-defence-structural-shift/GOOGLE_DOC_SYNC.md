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
> February of 2022 saw Russia's full-scale invasion of Ukraine, a major escalation of the war Russia had launched in 2014 with the seizure of Crimea and the incursion into the Donbas. The 2022 invasion was the first large-scale interstate conventional war in Europe in decades.

**Reply to Gonchar 1:** "Fixed — recast as the 2022 full-scale invasion / escalation of the 2014 war (Crimea + Donbas), and softened 'first conventional warfare' to 'first large-scale interstate conventional war in Europe in decades.'"

---

## 2. Introduction main paragraph (Gonchar 2) — commit `60e9506`

**Find:** *"its previous occupation of Crimea in 2014"* (also fixes "first conventional invasion of a European sovereign state since World War II")

**Replace the two opening sentences with:**
> Russia's full-scale invasion of Ukraine in 2022 broke a period of relative social and economic calm in Europe that its earlier 2014 invasion had not. The 2014 invasion seized Crimea and opened the Donbas conflict, which simmered as an active conflict zone for the next eight years. The 2022 escalation alarmed people, as it was the largest conventional war on European soil since World War II, and shook the complacent belief that peace in the post-Cold War era would be sustainable indefinitely.

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
> One inference is that if defence spending growth stagnated and returned to trend (mean-reversion) even after Russia's 2014 invasion of Ukraine, which seized Crimea and opened a sustained war in the Donbas, then a similar reversion may follow the 2022 escalation.

**Reply to Gonchar 11:** "Fixed — replaced 'deduce' with 'One inference is that … may follow' (more tentative, appropriate for the foil); also corrected the 2014 framing to name both Crimea and Donbas."

---

## 5. Signalling Theory book-to-bill phrasing — commit `b0bdd25` (no Gonchar id; cohesion fix)

**Find:** *"as a ratio of total orders shipped"*

**Replace the sentence containing it with:**
> For example, the book-to-bill ratio shows how many new orders companies are receiving relative to revenue recognised in the same period. This is a clear signal of a real shift in demand, not only political but, perhaps more importantly, monetary.

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
> The corollary to these semantic scores is best demonstrated by the book-to-bill ratio in the Welch test. As the most forward-looking financial metric, the book-to-bill ratio increased from 1.20 pre-invasion to 1.75 post-invasion and accelerated to 2.02 by 2025. The Chow test provides further compelling support for both findings. The results in Table 2 confirm a structural break (i.e., a shift in trend) between 2021 and 2022 in eight of the sixty company-metric cells: three at the 5% level and five marginally significant at the 10% level. These cover six of the ten firms (Airbus, BAE Systems, Dassault Aviation, Leonardo, Rolls-Royce, and Thales).

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
> One future study might decompose the cumulative impact of Russia's 2014 invasion of Ukraine, which seized Crimea and opened a sustained war in the Donbas, and the 2022 escalation. The eight intervening years of low-intensity conflict could serve as a baseline against which the 2022 step-change in cyclical and structural inertia can be measured.

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

---

# Tier 4 — wording / over-claiming (6 more edits)

These shipped on branch `tier-4-wording`. Same workflow: search, replace, reply, resolve.

## 11. "Fundamental strategic independence" (Gonchar 3) — commit `8397fac`

**Find:** *"drive a shift toward fundamental strategic independence"* (closing of the Introduction autonomy paragraph)

**Replace:**
> drive a shift toward greater strategic independence.

**Reply to Gonchar 3:** "Simplified — 'fundamental' was carrying no weight; the surrounding paragraph already establishes 'strategic autonomy and independence', so 'greater strategic independence' echoes cleanly."

---

## 12. "Band-aid" register (Gonchar 14) — commit `90fc1b7`

**Find:** *"a fast fix -to stop the bleeding, as it were-and the "band-aid" nature"* (closing of the line-246 cyclical-evidence paragraph)

**Replace the entire closing clause with:**
> short-term measures, and the limited durability of these arrangements implied that a more sustainable, coherent continental level of defence security needed to be developed.

**Reply to Gonchar 14:** "Fixed — replaced 'band-aid' / 'stop the bleeding' colloquialism with neutral academic register ('short-term measures', 'limited durability')."

*Heads-up:* Gonchar's id 13 ("What was this fast fix? Citation?") is still open — the colloquialism is gone but no citation has been added for the limited-durability characterisation. Tier 2 will pick that up.

---

## 13. "Admitting in the process its crucial nature" (Gonchar 20) — commit `72170dc`

**Find:** *"admitting in the process its crucial nature from a socioeconomic lens"* (in the Literature Contradictions paragraph at line 294)

**Replace the sentence with:**
> As the old perceptions regarding spending on weaponry begin to shift, capital is flowing into the industry at scale, reflecting a growing recognition of its socioeconomic importance (Shevchuk & Luchka, 2024).

**Reply to Gonchar 20:** "Reworded — replaced the awkward 'admitting … its crucial nature from a socioeconomic lens' with the more direct 'reflecting a growing recognition of its socioeconomic importance'."

---

## 14. "Prompts a close look" (Gonchar 25) — commit `eb26ead`

**Find:** *"This evolution has energised the defence sector and prompts a close look at three key theoretical frameworks"* (closing sentence of the Theoretical Framework opener at line 306)

**Replace the sentence with:**
> To analyse this evolution, the thesis applies three key theoretical frameworks: structural break theory, signalling theory, and framing theory.

**Reply to Gonchar 25:** "Made the agency explicit — the thesis applies these frameworks rather than just looks at them. Also dropped the 'energised' rhetorical clause."

---

## 15. Wedding-banquet metaphor + "huge" (Gonchar 31, 32) — commit `36b6f65`

**Find:** *"this might seem like a person renting a hall for his wedding banquet"* (in the Zeitenwende paragraph at line 326)

**Replace the entire paragraph with:**
> Germany's *Zeitenwende* ("watershed moment") was established in February of 2022 and earmarked 100 billion euros to be disbursed in binding, long-term contracts just for its military. *Zeitenwende 2.0* (500 billion euros over the next 12 years) extends this commitment further (KRPATA, 2025). Defence contractors read these commitments as a credible signal, and the German push for a more robust defence stimulated a considerable increase in corporate spending on new facilities, factories, and production lines (Zandee et al., 2024). This illustration of signalling theory then piggybacks into other spheres as well. Defence companies send their own signals to financial markets, which can then plan for expansion in banking, loans, and broader financial activity.

**Reply to Gonchar 31:** "Cut — the wedding banquet / brides / honeymoon / 'Like the marriage' metaphor was too informal for journal submission. All substantive claims (€100B 2022 commitment, €500B Zeitenwende 2.0, contractor response, signalling-theory framing, KRPATA and Zandee citations) preserved verbatim."

**Reply to Gonchar 32:** "'huge' → 'considerable' as suggested."

---

## 16. AI-scans-to-"read" rephrase (Gonchar 36) — commit `9208614`

**Find:** *"this study designed its AI scans to "read" the reports"* (Semantic Analysis methodology opener at line 354)

**Replace the entire opening cluster with:**
> Semantic analysis should aim to identify *meaning* rather than count words. AI tools can readily measure word frequency, but in this study the prompts ask the model to read each report as a financial analyst would, applying the vocabulary and reporting conventions specific to the defence sector. The prompts then ask the model to score tone, framing, and commitment levels as expressed through word choice and the language of strategic stance.

**Reply to Gonchar 36:** "Rephrased — replaced 'designed its AI scans to "read"' (anthropomorphic, vague) with 'the prompts in this study direct the model to interpret', which names the actual mechanism (prompt engineering) and drops the scare quotes."

---

## After Tier 4: 14 of 51 Gonchar comments resolved

Tier 1 (8) + Tier 4 (6) = **14 comment threads** can now be closed: 1, 2, 3, 4, 11, 14, 20, 25, 31, 32, 36, 37, 40, 42, 43, 45.

Still open (37): the references-and-citations cluster (Tier 2), the structural-rewrite cluster (Tier 3 — handled by `RESTRUCTURE_PLAN.md`), and methodological / journal-style work (Tiers 5–6).

Two cohesion follow-ups flagged but not yet edited:
- **Line 348** — "instructed the AI to focus" — mild personification; candidate for tightening as part of Tier 5 LLM-rigor pass.
- **Line 364** — "the AI model provided a structured assessment" — same flavour; same plan.

## What's NOT in this checklist (still to be done)

Tier 2 references, Tier 3 structural rewrite (12 steps in `RESTRUCTURE_PLAN.md`), Tier 5 referee-grade methodology work, Tier 6 journal-style cleanup. These will produce their own sync sheets when each batch lands.
