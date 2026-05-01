# European Defence: Structural Shift Post-2022 — Summary

**Author:** Inès Rienzo
**Paper:** [`paper.md`](./paper.md)
**Last refreshed:** 2026-05-01 (port snapshot)

## Problem
Did Russia's February 2022 invasion of Ukraine produce a **structural** (lasting parameter shift) or **cyclical** (temporary level shift) change in European defence companies? The empirical answer matters for capital allocation, EU industrial policy, and the future of the post-Cold-War "peace dividend" frame.

## Approach
Mixed methods on 79 annual reports (2018–2025) from ten listed European primes (Airbus, BAE, Dassault, Indra, Leonardo, Rheinmetall, Rolls-Royce, Saab, Safran, Thales). Two LLMs (Claude Opus 4.5, Gemini 2.5) score each report 1–10 on cyclical-vs-structural language. Three financial tests on six metrics: Welch t-test (pre/post means), Chow break test (per-firm and pooled), and panel fixed-effects regression. A DiD against commercial-aerospace exposure isolates the defence-specific effect. Inter-rater reliability checked with Cohen's κ.

## Key result
Mean structural score rises **4.7 → 7.1 → 8.1** (pre / post / 2025). Pooled book-to-bill rises **1.20 → 1.75** (Welch p = 0.0013). Group EBIT margin rises **+2.7 pp** (~35% relative; panel p = 0.037). Chow detects breaks in **8 of 60 firm-metric cells** at ≤10% (3 at 5%). κ between LLM raters = 0.88.

## Why it matters
The paper argues the post-2022 trajectory is structural, not cyclical — implying multi-decade reallocation of European industrial capacity, ESG re-framing of defence stocks, and weaker US dependence. If true, it overturns the "peace dividend" prior; if not, today's order books unwind.

## Open questions / weaknesses (referee-grade)
- N=10 firms; standard errors fragile — wild-cluster bootstrap not yet reported.
- DiD parallel-trends not shown; commercial-aerospace control is contaminated by post-COVID rebound.
- LLM scoring lacks human-coded validation; stochasticity not characterised; potential training-data leakage of the annual reports.
- Multiple-testing correction across six metrics not applied (the panel p = 0.037 likely fails Holm).
- Causal language overstates what the design supports.

See `notes.md` for the full punch list and `CHANGELOG.md` for in-flight fixes.
