# Notes — European Defence Structural Shift

Working punch list. Items marked `[x]` are done; pending items show what's blocking.
Cross-references: Gonchar comment ids → `comments.md`; applied edits → `CHANGELOG.md`.

## Tier 1 — corrections (factual / arithmetic / formula)

- [x] **Book-to-bill formula inverted** (Gonchar 37) — fix prose; numbers OK. *Applied; see CHANGELOG 2026-05-01.*
- [x] **"eight of the ten companies" + arithmetic + artifacts** (Gonchar 40, 42) — units wrong (cells, not firms); ≈35% not 40%; fix "areis", "compelling supports". *Applied; see CHANGELOG 2026-05-01.*
- [x] **Russia invaded in 2014** (Gonchar 1, 2, 11, 43) — recast every "first conventional warfare in Europe" / "occupation of Crimea" passage; 2022 is an *expansion* of an ongoing 2014 invasion. *Gonchar 1 applied (Executive Summary opener, edit 1 of 4 in "2014 framing" series, commit e40464b); Gonchar 2 applied (Introduction opener, line 200, edit 2 of 4, commit 60e9506); Gonchar 11 applied (foil sentence, line 240, edit 3 of 4, commit b291b70); Gonchar 43 applied (Future Research sentence, line 777, edit 4 of 4; see CHANGELOG 2026-05-01).*
- [x] **Mellace et al. miscited** (Gonchar 4) — that paper is on the 2025 US aid suspension, not 2022. Fix or drop. *Applied; see CHANGELOG 2026-05-01.*
- [x] **Conclusion contradicts Howorth (2025)** (Gonchar 45) — line "Europe is no longer simply purchasing most of its defence needs from the United States" must be hedged. *Applied; see CHANGELOG 2026-05-01.*

## Tier 2 — references and citations

- [ ] Add Derwall et al. (2011) to References (Gonchar 7).
- [x] Add Sandler & Hartley (1995) to References (Gonchar 8). *Applied; see CHANGELOG 2026-05-02.*
- [x] Remove duplicate Ivančík entry (Gonchar 47). *Applied; see CHANGELOG 2026-05-02.*
- [x] Verify each: Bruner (2024), English (2025), Strüwe (2024), Suchman (1995), Walker & Willer (2014) is actually cited; drop or cite (Gonchar 49–53). *Applied; all five dropped (zero body mentions confirmed); see CHANGELOG 2026-05-02.*
- [x] Add citations for "guns vs butter" (19). *Applied; Sacchi et al. (2026) cited for definition; Sacchi year corrected 2025→2026; fewerless typo removed; see CHANGELOG 2026-05-02.*
- [ ] Add citations for framing-theory origin (33, → Goffman 1974 / Entman 1993), structural-break theory (26), "band-aid policy fix" (13), defence sin-stock framing (41), "government policies… stimulated the market" (16).

## Tier 3 — structure (Gonchar's flow rewrite)

- [ ] Number sections; drop sub-subsections (Gonchar 0).
- [ ] Rename "Literature Review" → **Background**; subsections: *History of European Defence Spending* and *Russia's Invasion of Ukraine* (Gonchar 5).
- [ ] Then a real **Literature Review** that positions question + method against prior work.
- [ ] Move "Detecting Structural Change" into the *Structural Break Analysis* subsection (Gonchar 18).
- [ ] Move two history paragraphs into *History of European Defence Spending* (Gonchar 29, 34).
- [ ] Promote **Data Collection** to its own *Data* section between Theory and Empirical (Gonchar 35).
- [ ] Rename "Analytical and Theoretical Frameworks" → **Theoretical Framework** or **Methodology** (Gonchar 23).
- [ ] Expand **Conclusion** per Gonchar 44: restate question → semantic evidence → financial evidence → limits → hedged statement.

## Tier 4 — wording / over-claiming

- [ ] Simplify "fundamental strategic independence" (3).
- [ ] "band-aid" → "short-term" (14).
- [ ] "huge" → "considerable" (32).
- [ ] "admitting in the process its crucial nature" → reword (20).
- [ ] "this study designed its AI scans to 'read' the reports" — rephrase (36).
- [ ] "prompts a close look" → "applies / implements" (25).
- [ ] Cut or hedge the "Peace Dividend era is fading… ESG bygone" closing (46).
- [ ] Drop or audit the wedding-banquet/Zeitenwende joke (author-flagged 31).

## Tier 5 — referee-grade methodological holes (not flagged by Gonchar; needed for journal)

- [ ] **Identification:** parallel-trends figure for DiD; placebo test with fake invasion date (e.g. Q1 2020); decompose defence-revenue-share to control for COVID-suppressed commercial denominators.
- [ ] **Inference:** wild-cluster bootstrap SEs; Holm-Bonferroni correction across the six metrics.
- [ ] **Structural break:** add Quandt-Andrews supF / Bai-Perron unknown-break tests; report breaks per company.
- [ ] **LLM scoring:**
  - [ ] Disclose model versions, temperature, top_p, prompts in appendix (currently partial).
  - [ ] Run each report 5–10 times; report mean ± SD.
  - [ ] Human-code 20-report stratified subsample; compute κ vs LLMs as ground-truth check.
  - [ ] Add a third heterogeneous rater (open-source LLM or Loughran-McDonald dictionary) for triangulation.
  - [ ] Placebo prompt: rate "structural commitment to commercial aviation" — confirms scores measure commitment, not era.
  - [ ] Acknowledge training-data leakage of annual reports.
- [ ] **Theory ↔ evidence:** lead-lag panel of capex/FTE vs semantic score to test signalling prediction.
- [ ] **Sample justification:** explain why Hensoldt, Kongsberg, KNDS, Naval Group, MTU, Patria are excluded.
- [ ] **Causal language:** replace "Russia's invasion *created*" → "is *associated with*" / "*coincided with*" throughout.
- [ ] **Replication archive:** data CSVs, code, LLM prompt-and-response logs, README.

## Tier 6 — journal-style cleanup

- [ ] Remove Executive Summary, Declaration, AI-use ack from body — abstract only (AI-use → footnote/methods).
- [ ] State formal hypotheses (H1, H2, H3) at end of theory section; test numbered in Results.
- [ ] Summary-statistics table for the panel.
- [ ] Tables in journal style (coefficients, SEs in parens, stars, N, R²).
- [ ] Number all equations.
- [ ] If single-author, replace "we" → "I" or passive voice.

---

## Tracking convention

When an item lands:
1. Apply the edit via the `paper-editor` subagent.
2. Tick the box here.
3. Move the entry from `CHANGELOG.md` Pending → Applied with the commit sha.
4. Mark the corresponding row in `comments.md` as `resolved`.
