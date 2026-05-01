# Tier 3 Restructure Plan — Rienzo Thesis

Working document for the `paper-editor` subagent. Each step is a single surgical edit. Read top-to-bottom; execute in the recommended order at the bottom.

Target file: `/home/user/StudentPapers/papers/ines-rienzo/european-defence-structural-shift/paper.md` (1,416 lines).

---

## 1. Current structure map

### 1a. Body headings (actual)

Extracted via `grep -nE '^#{1,4} '`. Heading text is reproduced verbatim (including bolds, trailing spaces, typos):

| Line | Level | Heading |
|---:|:--|:--|
| 1   | `#`    | `Onglet 1` (port-from-Doc artifact, not a real heading) |
| 175 | `#`    | `**Executive Summary**` |
| 196 | `#`    | `**Introduction**` |
| 208 | `#`    | `**Literature Review**` |
| 212 | `##`   | `**Historical Baseline**` |
| 226 | `##`   | `**Evidence of a Cyclical Shift**` |
| 250 | `##`   | `**Evidence of Structural Shift**` |
| 276 | `##`   | `**Textual Analysis of Corporate Disclosures**` |
| 280 | `##`   | `**Detecting Structural Change**` |
| 286 | `##`   | `**Literature Contradictions**` |
| 298 | `##`   | `**Current Literature Gaps and Our Contributions**` |
| 304 | `#`    | `**Analytical and Theoretical Frameworks**` |
| 312 | `##`   | `**Structural Break Analysis**` |
| 320 | `##`   | `**Signalling Theory**` |
| 330 | `##`   | `**Framing Theory**` |
| 340 | `#`    | `**Mixed Methods**` |
| 344 | `##`   | `**Data Collection**` |
| 350 | `##`   | `**Semantic Analysis**` |
| 352 | `###`  | `***Methodology***` |
| 360 | `###`  | `***Large Language Model Framework***` |
| 379 | `###`  | `***Results***` |
| 381 | `####` | `*The Overall Picture*` |
| 399 | `####` | `*Classification*` |
| 425 | `####` | `*Company-level Assessment*` |
| 447 | `####` | `*The Outliers*` |
| 455 | `####` | `*Investment Commitment Language*` |
| 475 | `###`  | `***Inter-Rater Reliability Using a Second AI Model***` |
| 502 | `###`  | `***Difference-in-Difference (DiD) Analysis***` |
| 620 | `##`   | `**Financial Analysis**` |
| 622 | `###`  | `***Methodology***` |
| 637 | `###`  | `**Tests**` (note: `###` but with `##` bolding — ported anomaly) |
| 641 | `####` | `*Test 1 - Comparing Metric Averages Before and After the Invasion (Welch)*` |
| 660 | `####` | `*Test 2 - Confirming the Break Point, Per-Company and Pooled Chow Tests*` |
| 709 | `####` | `*Test 3 - Panel Fixed-Effects Regression*` |
| 725 | `#`    | `**Contextualisation of Mixed-Methods vis-a-vis the Theoretical Framework and Results**` |
| 734 | `###`  | `**Key Signalling Links Between Analyses**` (anomaly: jumps `##` → `###`) |
| 742 | `###`  | `**Pre- and Post-Invasion Framing**` |
| 754 | `###`  | `**Theoretical Support through Company Heterogeneity**` |
| 762 | `###`  | `**Summary of Key Limitations and Potential Avenues for Future Study**` |
| 781 | `#`    | `**Conclusion**` |
| 804 | `#`    | (blank `#`) |
| 806 | `#`    | `**References**` |
| 960 | `#`    | (blank `#`) |
| 962 | `#`    | `**Appendix**` |
| 1250 | `#`   | `**Appendix C: Semantic**` |

Anomalies the editor should be aware of:
- Line 1 `# Onglet 1` is Google-Docs porting noise. Out of Tier-3 scope (it's not a content heading). Flag for Tier 4/cleanup.
- Lines 637, 734 use `###` where the parent is `##`/`#`; the depth is one off. Live with it through Tier 3; revisit only if it interacts with renumbering.
- Lines 804 and 960 are stub `#` lines (probably intentional pagebreaks from the Doc). Leave alone.
- Section 725 ("Contextualisation…") has `###` subsections but no `##`s — that section is essentially flat under a `#`.

### 1b. TOC block at top of paper (lines 75–157)

The TOC is a Google-Docs export with heading-anchor URLs and printed page numbers. Its sequence:

`Executive Summary 7 → Introduction 8 → Literature Review 10 [Historical Baseline 10, Evidence of a Cyclical Shift 11, Evidence of Structural Shift 12, Textual Analysis of Corporate Disclosures 13, Detecting Structural Change 14, Literature Contradictions 14, Current Literature Gaps and Our Contributions 16] → Analytical and Theoretical Frameworks 16 [Structural Break Analysis 16, Signaling Theory 17, Framing Theory 18] → Mixed Methods 19 [Data Collection 19, Semantic Analysis 20 [Methodology 20, LLM Framework 20, Results 21 [The Overall Picture 21, Classification 22, Company-level Assessment 24, The Outliers 25, Investment Commitment Language 27], Inter-Rater Reliability 28, DiD 29], Financial Analysis 33 [Methodology 33, Tests 34 [Test 1 34, Test 2 35, Test 3 37]]] → Contextualisation 39 [Key Signalling Links 39, Pre- and Post-Invasion Framing 40, Theoretical Support through Company Heterogeneity 41, Summary of Key Limitations and Potential Avenues for Future Study 41] → Conclusion 43 → References 44 → Appendix 47.`

### 1c. TOC vs. body drift

- TOC says "Signaling Theory" (one `l`); body line 320 says "Signalling Theory" (UK spelling). Mismatch is cosmetic but visible in the TOC.
- TOC heading-link URLs all point to the Google Doc (`https://docs.google.com/document/d/...`). These are useless in the Markdown port and will be wholly invalidated by any heading rename. They should be regenerated, but that is a Tier-4 concern unless we choose to scrub during Tier-3 (recommended; cheaper to do once).
- Page numbers ("7, 8, 10, 11…") are meaningless in Markdown. Leaving them in is harmless; rebuilding them is impossible without a fixed page geometry.
- TOC does not list "Test 1/2/3" sub-bullets identically to body — close enough; no drift worth fixing in Tier 3.

### 1d. Cross-references and in-text section pointers

A full sweep of the body and table/figure mentions found these load-bearing references:

| Line | Reference | What it points to | Will it break? |
|---:|:--|:--|:--|
| 230 | "Figure 1The graph below" | Figure 1 (caption line 234) | No — figure stays put |
| 316 | "the aforementioned 'peace dividend'" | Background → Peace Dividend (currently Lit Review → Historical Baseline) | **Yes** — once Peace Dividend moves under Background, the word "aforementioned" still works because Background precedes Theoretical Framework. Verify ordering. |
| 334 | "the previously-noted peace dividends and demilitarisation" | Same as above | Same |
| 362 | "The full prompts are included in Appendix C" | Appendix C (line 1250) | No — appendix unchanged |
| 668 | "All detailed results can be found in Appendix A" | Appendix A (line 964) | No |
| 738 | "The results in Table 2 confirm a structural break …" | Appendix A → Table 2 (line 982) | No — table numbering unchanged |
| 348 | "The same reports were used to drive the quantitative analysis" | Forward ref to Financial Analysis | No |
| 504, 519, 548, 555, 571, 588, 604, 610 | DiD intra-section refs | Internal to DiD subsection | No |
| 721, 740, 750, 758 | "earlier tests", "as noted above", "above" | Intra-Contextualisation refs | No |
| 282 | "across both halves of the analysis in this thesis: financial metrics … LLM-generated narrative scores …" | Forward ref to both Mixed Methods halves | No (paragraph itself moves; refs internal to that paragraph) |
| 727 | "the following four tests of the overarching research" | Forward into Contextualisation list | No |
| 775 | "as noted above" | Conclusion limitations sentence — refs back to limitations subsection | No |
| 738 | "approximately 51 percent" / "8.1 by 2025" | Results numbers | No |

Two reference-style risks not covered above:
- The TOC block (lines 75–157) is itself a giant cross-reference. Every renamed heading must update the TOC entry. (See Step 11.)
- The body uses "Theoretical Framework" / "framework" / "frameworks" inconsistently in prose. After renaming the section, sweep paragraph text where "Analytical and Theoretical Frameworks" appears as a noun phrase. (None found in body prose, but verify on each step.)

---

## 2. Target structure (post-Tier-3)

Numbered headings. Format: `N. Title` for `#`, `N.M Title` for `##`, `N.M.K Title` for `###`. Sub-subsections (`####`) eliminated per Gonchar 0.

```
1. Executive Summary
2. Introduction
3. Background
   3.1 History of European Defence Spending
   3.2 Russia's Invasion of Ukraine
4. Literature Review
   4.1 Textual Analysis of Corporate Disclosures
   4.2 Literature Contradictions
   4.3 Current Literature Gaps and Our Contributions
5. Theoretical Framework
   5.1 Structural Break Analysis
   5.2 Signalling Theory
   5.3 Framing Theory
6. Data
7. Mixed Methods
   7.1 Semantic Analysis
       7.1.1 Methodology
       7.1.2 Large Language Model Framework
       7.1.3 Results
       7.1.4 Inter-Rater Reliability Using a Second AI Model
       7.1.5 Difference-in-Difference (DiD) Analysis
   7.2 Financial Analysis
       7.2.1 Methodology
       7.2.2 Tests
8. Contextualisation of Mixed Methods vis-à-vis the Theoretical Framework and Results
   8.1 Key Signalling Links Between Analyses
   8.2 Pre- and Post-Invasion Framing
   8.3 Theoretical Support through Company Heterogeneity
   8.4 Summary of Key Limitations and Potential Avenues for Future Study
9. Conclusion
References
Appendix
```

### 2a. Mapping current → target

| Current section/paragraph | Target |
|:--|:--|
| `# Executive Summary` (line 175) | `1. Executive Summary` |
| `# Introduction` (line 196) | `2. Introduction` |
| `# Literature Review` (line 208) — **header reused** | becomes `3. Background` |
| `## Historical Baseline` (212) → contains "Defence Companies as Sin Stocks" + "Peace Dividend" | absorbed into `3.1 History of European Defence Spending` |
| `## Evidence of a Cyclical Shift` (226) — "Temporary Spike" + "An Improvised Solution" | the "Temporary Spike" / PESCO paragraph + Figure 1 → `3.1`; the "Improvised Solution" U.S./EU funding paragraph → `3.2 Russia's Invasion of Ukraine` |
| `## Evidence of Structural Shift` (250) — "Underlying Political Change" / "Economic Legitimacy" / "Microeconomic Transition" | political-change + EDIS + economic legitimacy → `3.2`; microeconomic transition (firm-level cyclical-vs-structural literature) → stays in **`4. Literature Review`** as part of new Lit Review opener |
| **(currently inside Sig Theory at line 324)** "Prior to 2022, European defence companies had no reason…" | move to `3.1` (Gonchar 29) |
| **(currently inside Framing Theory at line 334)** "For many years after the Cold War, the European defence industry was framed predominantly…" | move to `3.1` (Gonchar 34). Note: keep one or two sentences of the Framing example in 5.3 to ground the theory; only the historical-narrative content moves. |
| `## Textual Analysis of Corporate Disclosures` (276) | `4.1` (now under the **new** Literature Review) |
| `## Detecting Structural Change` (280) | move into `5.1 Structural Break Analysis` (Gonchar 18) — appended as second paragraph or merged |
| `## Literature Contradictions` (286) | `4.2` |
| `## Current Literature Gaps and Our Contributions` (298) | `4.3` |
| `# Analytical and Theoretical Frameworks` (304) — opener paragraphs (lines 306, 308) | rename to `5. Theoretical Framework`; opener paragraphs retained as-is (they already introduce the three theories + tie each to its analytical role per Gonchar 23) |
| `## Structural Break Analysis` (312) | `5.1` (now contains the moved Detecting Structural Change paragraph) |
| `## Signalling Theory` (320) | `5.2` |
| `## Framing Theory` (330) | `5.3` |
| `# Mixed Methods` (340) | `7. Mixed Methods` (after `Data` insertion) |
| `## Data Collection` (344) | promoted to `# 6. Data` (Gonchar 35) |
| `## Semantic Analysis` (350) | `7.1 Semantic Analysis` |
| `### Methodology` / `### Large Language Model Framework` / `### Results` etc. | `7.1.1 / 7.1.2 / 7.1.3 / 7.1.4 / 7.1.5` |
| `#### The Overall Picture` etc. (the four `####`s) | **flatten**: drop the heading line entirely, rely on figure captions and prose for navigation (Gonchar 0). The content stays. |
| `## Financial Analysis` (620) | `7.2` |
| `### Methodology` / `### Tests` | `7.2.1 / 7.2.2` |
| `#### Test 1/2/3` | **flatten** to bold paragraph leads (Gonchar 0). |
| `# Contextualisation…` (725) | `8. Contextualisation of Mixed Methods vis-à-vis the Theoretical Framework and Results` |
| `### Key Signalling Links` etc. | `8.1 / 8.2 / 8.3 / 8.4` (level-fix while we're there) |
| `# Conclusion` (781) | `9. Conclusion` — content **expanded** (Step 12) |
| `# References` / `# Appendix` / `# Appendix C` | unnumbered — back-matter convention; or label "References" / "Appendix" without numbers |

The target-structure decision tree on a few items:
- **`Sin Stocks` paragraph (216):** Gonchar 6 wants the relevance to the research question made explicit, but that is a Tier-4 prose change. In Tier 3 it stays in Background under `3.1` (alongside Peace Dividend) with no rewrite. Status quo on placement; we are not the editor for content change here.
- **`Microeconomic Transition` paragraph (270–274):** this discusses how Rheinmetall/Saab pivot to dual-use; it is closer to *literature* than *background*. Recommendation: keep in the new `4. Literature Review` opener, framed as "prior empirical work on firm-level adaptation". Alternative: include in `3.2`. Decision: **`4. Literature Review` opener.** This is a judgement call; if the editor disagrees, it can be moved in a follow-up edit at zero risk.
- **`Underlying Political Change` (256–260) and `Economic Legitimacy` (264–266):** these describe the EU/US response and macroeconomic implications post-invasion. Place under `3.2 Russia's Invasion of Ukraine`. Gonchar 5 explicitly invites this ("History of European Defence Spending" + "Russia's Invasion of Ukraine including Europe/US response").

---

## 3. Ordered execution plan

Each step is a single surgical edit applied by the `paper-editor` subagent. `before` and `after` are exact strings; the subagent matches them as-is. I have kept rename steps minimal and atomic. Paragraph moves are described as cut-paste with a `before-paragraph` (matched exactly), a delete from the source location, and an insertion at the destination with surrounding anchors (preceding-line + following-line) to disambiguate.

Numbering convention used in `after` strings: bold + leading numeral, no period after the number, matching what the editor (Gonchar id 0) implied. If the journal house style requires a period, this is a one-line global tweak in Tier 4.

---

### Step 1: Rename `Literature Review` heading to `Background`

- **Files:** `paper.md`
- **Operation:** rename
- **Before:** `# **Literature Review**` (line 208)
- **After:** `# **3. Background**`
- **Cross-references:** TOC block line 81 — handle in Step 11. Body uses "the literature" (not "the Literature Review section") so no in-text break.
- **Gonchar resolved:** 5 (partial — establishes the rename).
- **Cohesion sweep:** grep `Literature Review` post-edit — there must remain *one* hit at the new Lit Review heading inserted in Step 8. Until then the document is temporarily without a Lit Review section; this is fine because Steps 1–8 are sequential.
- **Risk:** low.

### Step 2: Insert `3.1 History of European Defence Spending` heading and consolidate the historical-baseline material under it

- **Files:** `paper.md`
- **Operation:** rename + insert-subsection-header
- **Before:** `## **Historical Baseline**` (line 212)
- **After:** `## **3.1 History of European Defence Spending**`
- **Sub-action (in same edit):** the two `*Defence Companies as "Sin Stocks"*` and `*Peace Dividend*` italicised pseudo-headings (lines 214 and 220) become bold paragraph leads or are simply absorbed; per Gonchar 0 ("drop sub-subsections"), prefer to **delete** them since the paragraphs are short. **Recommendation:** keep them as italicised lead phrases (they're not headings, they're emphasis) — do not change in this step. Tier 4 can revisit.
- **Cross-references:** "the aforementioned peace dividend" at line 316 still works because Background still precedes Theoretical Framework. Check after Step 6.
- **Gonchar resolved:** 5 (partial).
- **Risk:** low.

### Step 3: Move `*Temporary Spike*` paragraph + Figure 1 + cyclical-evidence material into `3.1`

This is a delete-and-reinsert of the entire `## **Evidence of a Cyclical Shift**` section (lines 226–248) into `3.1`, with the parent `##` header dropped (we are flattening). This includes:

- The intro sentence + PESCO paragraph (line 230)
- Figure 1 caption block (lines 234–236)
- The "One inference is that…" foil paragraph (line 240)

It *excludes* the "An Improvised Solution" sub-block (lines 244–246), which goes to `3.2` in Step 4.

- **Files:** `paper.md`
- **Operation:** move-paragraph
- **Before-block (exact, lines 226–242):** the `## **Evidence of a Cyclical Shift**` header through end of the "One inference" paragraph and the trailing blank-line-paragraph break before "*An Improvised Solution*"
- **After-block:** delete from current location; reinsert at end of `3.1` (immediately before the `## **Evidence of Structural Shift**` line in its current position, OR equivalently immediately after the existing Peace-Dividend paragraph). The cleanest insertion point is **right after line 222 (end of Peace Dividend paragraph)**, with one blank line separator and **without** the `##` Evidence-of-a-Cyclical-Shift header (drop the header).
- **Replacement opener for the moved block:** since we're dropping the parent `##`, the moved content needs a smooth handoff. Recommend prefixing with the existing italic *Temporary Spike* line which becomes the lead.
- **Cross-references:** the body of the foil paragraph references "the 2014 invasion" which is already factually corrected per CHANGELOG. No further fixes here.
- **Gonchar resolved:** 5 (partial).
- **Risk:** medium — large block, must verify Figure 1 caption and the table of figures (none — figures are inline) move atomically. Confirm by greppping `Figure 1` after the move; should still appear exactly once.

### Step 4: Insert `3.2 Russia's Invasion of Ukraine` heading and migrate post-invasion-response material into it

Material to assemble under `3.2`:
- "An Improvised Solution" (currently 244–246; the `*An Improvised Solution*` lead and the paragraph that follows)
- "Underlying Political Change" + EDIS paragraph (256–260)
- "Economic Legitimacy" paragraph (264–266)
- The `## **Evidence of Structural Shift**` opener paragraph at 252 ("Given its nature and organisation, the EU had no choice…") — this is the natural lead for `3.2`.

The `## **Evidence of Structural Shift**` *header* itself should be **replaced** by `## **3.2 Russia's Invasion of Ukraine**`. The "Microeconomic Transition" sub-block (270–274) **does not move**; it is repurposed as the opener of the new Lit Review (Step 8).

- **Files:** `paper.md`
- **Operation:** rename + reorganize within section
- **Before:** `## **Evidence of Structural Shift**` (line 250)
- **After:** `## **3.2 Russia's Invasion of Ukraine**`
- **Sub-action:** within `3.2`, prepend the relocated "An Improvised Solution" paragraph from Step 3's exclusion (so the order becomes: opener "Given its nature and organisation…" → An Improvised Solution → Underlying Political Change → Economic Legitimacy).
- **Cross-references:** none broken.
- **Gonchar resolved:** 5 (substantial).
- **Risk:** medium. This step is the highest-content-density move. The editor must keep paragraph order coherent. Recommend the editor pause and re-read `3.2` end-to-end after applying.

### Step 5: Move "Prior to 2022, European defence companies had no reason…" paragraph to `3.1`

- **Files:** `paper.md`
- **Operation:** move-paragraph
- **Before (paragraph, line 324):** `Prior to 2022, European defence companies had no reason to anticipate a dramatic surge in demand, and the incentive to invest large amounts of capital did not exist. The invasion dramatically changed this. Still, as governments anticipated longer-term defence needs, it was necessary for them to send consistent –and costly–signals to defence companies to make credible that they were intent upon developing and expanding their militaries (Ribera Payá & Barredo González, 2025).`
- **After:** delete from line 324; insert into `3.1 History of European Defence Spending` immediately after the "Peace Dividend" paragraph (or after the relocated foil paragraph from Step 3 — editor choice; recommend the latter since "Prior to 2022 there was no incentive" is a transitional bridge to the 2022 escalation in `3.2`).
- **Cross-references:** Signalling Theory (line 320) loses its second paragraph. Verify that line 326 ("Germany's *Zeitenwende*…") still flows from line 322. It does — `Zeitenwende` is introduced as a fresh example, but the paragraph break is now larger. The editor should consider adding a one-line bridge in Tier 4.
- **Gonchar resolved:** 29.
- **Cohesion target:** sweep `Signalling Theory` body to confirm Zeitenwende paragraph is the natural successor; flag for Tier 4 if a bridge sentence is wanted.
- **Risk:** low.

### Step 6: Move "For many years after the Cold War…" paragraph to `3.1`

- **Files:** `paper.md`
- **Operation:** move-paragraph
- **Before (paragraph, line 334):** `For many years after the Cold War, the European defence industry was framed predominantly through a lens of ethical liability and restraint. The key political narrative placed emphasis on the previously -noted peace dividends and demilitarisation. The defence sector was often framed as an unfortunate, heavily regulated necessity rather than a public good. In financial markets, this framing resulted in the exclusion of most defence companies from many Environmental, Social, and Governance ESG (ESGEnvironmental, Social, and Governance) portfolios, creating the moral opinion that weapons manufacturing was inherently risky or anti-sustainable (Drempetic et al., 2020).`
- **After:** delete from line 334; insert into `3.1` (after the Step 5 paragraph). The "previously-noted peace dividends" cross-reference still works since Peace Dividend is in the same subsection.
- **Cross-references:** Framing Theory (line 332) loses its concrete example. The next paragraph (line 336, "The abrupt and emphatic change…") starts with "The abrupt change…" — currently this *contrasts* with the Cold-War paragraph being moved out. After the move, line 336 reads abruptly. **Flag for Tier 4:** add a one-line bridge in Framing Theory restating the pre-2022 baseline before launching into the post-2022 reframing.
- **Gonchar resolved:** 34.
- **Cohesion target:** sweep `Framing Theory` body; flag the abrupt-transition issue.
- **Risk:** medium (orphaned transition).

### Step 7: Move `## Detecting Structural Change` content into `5.1 Structural Break Analysis`

- **Files:** `paper.md`
- **Operation:** move-paragraph + delete-heading
- **Before (heading + paragraph, lines 280–282):** `## **Detecting Structural Change**` + the single paragraph "Distinguishing temporary shocks from permanent regime changes is, of course, necessary here…"
- **After:** delete heading line 280; move paragraph into `## **5.1 Structural Break Analysis**` (currently line 312). Insert as a new paragraph after the existing line-316 paragraph ("The Chow test, originally designed by Gregory Chow in 1960…"). Rationale: that placement reads "[problem of distinguishing breaks] → [Chow as the tool] → [combined with panel/DiD] → [applied here]," which is the editor's intended flow.
- **Cross-references:** the moved paragraph references "this thesis" / "in this thesis" multiple times — those still work. It also references "commercial aerospace firms serve as a control group" — forward ref, still works.
- **Gonchar resolved:** 18.
- **Risk:** low.

### Step 8: Insert new `4. Literature Review` section between Background and Theoretical Framework

This is the only step in this batch that adds a heading without an existing parent. It uses the `Textual Analysis of Corporate Disclosures` + `Literature Contradictions` + `Current Literature Gaps and Our Contributions` blocks (currently lines 276–302) as the section body, plus the orphaned "Microeconomic Transition" paragraphs (currently 270–274) as a new opener, and adds a one-paragraph framing lead from Gonchar's note about positioning the question against prior work.

- **Files:** `paper.md`
- **Operation:** insert-section-header + reorganize
- **Action sequence within this step:**
  1. **Delete heading** `## **Textual Analysis of Corporate Disclosures**` at line 276 (it becomes a `##` under the new `#` Lit Review).
  2. **Insert new `# **4. Literature Review**` header** immediately before the (deleted-line-280)-now-relocated text. Concretely: where the old `## Textual Analysis of Corporate Disclosures` stood (after the relocated `*Microeconomic Transition*` paragraph), insert:
     - `# **4. Literature Review**` (level-1)
     - one paragraph of new framing prose (≤4 sentences) positioning this paper against prior work — see template below.
     - then re-insert `## **4.1 Textual Analysis of Corporate Disclosures**` and the existing paragraph.
  3. **Move** `*Microeconomic Transition*` paragraph cluster (lines 270–274 currently) into `4. Literature Review` as opener content (under the new framing paragraph, before `4.1`).
  4. **Rename** `## **Literature Contradictions**` → `## **4.2 Literature Contradictions**` (line 286).
  5. **Rename** `## **Current Literature Gaps and Our Contributions**` → `## **4.3 Current Literature Gaps and Our Contributions**` (line 298).
- **Suggested framing-paragraph template** (to be drafted by the editor — this is the only place outside Step 12 where new prose is needed; keep ≤80 words, in Rienzo's voice):

  > "The empirical literature on the post-2022 European defence shift falls into three groups: studies of macro-level spending and procurement (Cepparulo & Pasimeni 2024; Genini 2025; Lane 2024), studies of firm-level reorientation toward dual-use production (Börjeson Kennedy et al. 2025; Freedman 2023), and methodological work on detecting regime change in time series and corporate disclosures (Chow 1960; Loughran & McDonald 2011). This thesis combines the second and third strands by applying narrative-text methods and structural-break tests jointly to the same ten-firm panel."

  Mark this as the editor's-discretion text; the sentence above is a placeholder.

- **Cross-references:** TOC handled in Step 11.
- **Gonchar resolved:** 5 (completes the rename + new-section requirement).
- **Cohesion target:** sweep "literature review" / "the literature" mentions in body to make sure none claim something the new Lit Review doesn't cover.
- **Risk:** medium-high — most complex step. The editor should apply this as one commit but may want to split if matchers fail.

### Step 9: Rename `# Analytical and Theoretical Frameworks` to `# 5. Theoretical Framework`; renumber subsections

- **Files:** `paper.md`
- **Operation:** rename × 4
- **Before (line 304):** `# **Analytical and Theoretical Frameworks**`
- **After:** `# **5. Theoretical Framework**`
- **Before (line 312):** `## **Structural Break Analysis**`
- **After:** `## **5.1 Structural Break Analysis**`
- **Before (line 320):** `## **Signalling Theory** ` (note trailing space)
- **After:** `## **5.2 Signalling Theory**`
- **Before (line 330):** `## **Framing Theory**`
- **After:** `## **5.3 Framing Theory**`
- **Cross-references:** TOC.
- **Gonchar resolved:** 23. Gonchar specifically asked for "introduce the three theoretical frameworks where they tie to their analytical role" — the existing opener paragraphs at lines 306–308 already do this, so no prose move is required. (The editor explicitly said the rename + reorder is sufficient; the opener paragraphs already preview each theory.)
- **Risk:** low.

### Step 10: Promote `Data Collection` to `# 6. Data`; renumber Mixed Methods and downstream

- **Files:** `paper.md`
- **Operation:** rename + level-promotion + renumber cascade
- **Sub-actions:**
  1. **Before (line 344):** `## **Data Collection**`
     **After:** `# **6. Data**` (level 1; promoted from `##` to `#`)
     This pulls the two Data-Collection paragraphs (346, 348) out from under "Mixed Methods" into a top-level section.
  2. **Before (line 340):** `# **Mixed Methods**`
     **After:** `# **7. Mixed Methods**`
     Note that with Step 10.1 the Data section is *between* Theoretical Framework and Mixed Methods, so the Mixed Methods header at line 340 needs to be kept — but it is currently *above* Data Collection (line 344). After Step 10.1 promotes Data to `#`, the `# Mixed Methods` header at 340 is now followed immediately by `# Data` and then Semantic Analysis. **This breaks the structure.** Fix: in the same edit, **delete** the `# Mixed Methods` heading at 340 and **insert** a new `# **7. Mixed Methods**` heading immediately *after* the Data section (i.e., immediately before the current `## **Semantic Analysis**` at line 350).
  3. **Renumber subsections:**
     - Line 350 `## **Semantic Analysis**` → `## **7.1 Semantic Analysis**`
     - Line 620 `## **Financial Analysis**` → `## **7.2 Financial Analysis**`
- **Cross-references:** "the same reports were used to drive the quantitative analysis" (line 348, end of Data) is a forward ref into 7.2 — still works.
- **Gonchar resolved:** 35.
- **Risk:** medium — the heading-level swap is the trickiest atomic operation. Two-pass approach is fine: commit the promotion as one edit, the Mixed Methods relocation as a second.

### Step 11: TOC rebuild + sub-subsection (`####`) flattening + remaining `###` renumbering

This step bundles the cleanup operations that touch a lot of lines but are mechanical.

- **Files:** `paper.md`
- **Operation:** rebuild + flatten
- **Sub-actions:**
  1. **Replace TOC block** (lines 75–157) with a new TOC matching the target structure in §2. Drop Google-Doc URLs; use plain numbered list. Drop page numbers (or keep them as `??` placeholders for typesetting).
  2. **Flatten `####` headings.** All five Semantic-Results `####` headings (lines 381, 399, 425, 447, 455) and the three Financial-Tests `####` headings (641, 660, 709) are removed. The titles become bold paragraph leads — e.g., `**Test 1 — Comparing Metric Averages Before and After the Invasion (Welch).**` at the start of the paragraph that currently follows the `####`. This satisfies Gonchar 0 ("drop sub-subsections") without losing navigability.
  3. **Renumber `###` headings under `7.1` and `7.2`:**
     - `### Methodology` (line 352) → `### 7.1.1 Methodology`
     - `### Large Language Model Framework` (360) → `### 7.1.2 Large Language Model Framework`
     - `### Results` (379) → `### 7.1.3 Results`
     - `### Inter-Rater Reliability Using a Second AI Model` (475) → `### 7.1.4 Inter-Rater Reliability Using a Second AI Model`
     - `### Difference-in-Difference (DiD) Analysis` (502) → `### 7.1.5 Difference-in-Difference (DiD) Analysis`
     - `### Methodology` (622, under Financial Analysis) → `### 7.2.1 Methodology`
     - `### Tests` (637) → `### 7.2.2 Tests` (also fix the bold-marker mismatch from `**Tests**` to consistent style)
  4. **Renumber Contextualisation subsections** (currently `###` under `# Contextualisation…`):
     - `# Contextualisation…` (line 725) → `# **8. Contextualisation of Mixed Methods vis-à-vis the Theoretical Framework and Results**`
     - `### Key Signalling Links Between Analyses` (734) → `## **8.1 Key Signalling Links Between Analyses**` (level promotion `###` → `##` to fix the existing depth anomaly)
     - similarly 742 → `## 8.2 Pre- and Post-Invasion Framing`
     - 754 → `## 8.3 Theoretical Support through Company Heterogeneity`
     - 762 → `## 8.4 Summary of Key Limitations and Potential Avenues for Future Study`
  5. **Renumber Conclusion / References / Appendix:**
     - Line 781: `# **Conclusion**` → `# **9. Conclusion**`
     - Line 806: `# **References**` → `# **References**` (unchanged — back-matter convention)
     - Line 962: `# **Appendix**` → `# **Appendix**` (unchanged)
     - Line 1250: `# **Appendix C: Semantic**` → `# **Appendix C: Semantic**` (unchanged)
  6. **Renumber Executive Summary / Introduction:**
     - Line 175: `# **Executive Summary**` → `# **1. Executive Summary**`
     - Line 196: `# **Introduction**` → `# **2. Introduction**`
- **Cross-references:** none break — Table 2 / Figure 1 / Appendix A,C all retain their existing labels.
- **Gonchar resolved:** 0 (numbering + sub-sub flattening), and finalises TOC consistency.
- **Risk:** medium. Many small edits. Recommend executing as 3–4 commits within this step ("TOC rebuild", "flatten Semantic Results sub-subsections", "flatten Financial Tests sub-subsections", "Contextualisation renumber"). The `paper-editor` subagent can decide commit boundaries.

### Step 12: Expand the Conclusion (Gonchar 44; closes 064e4b3 cohesion follow-up on line 294 over-claim)

This is the only step that *generates new prose*. The expanded Conclusion replaces the current two paragraphs at lines 783–785. The draft below uses only numbers and findings present in the paper; nothing is invented.

- **Files:** `paper.md`
- **Operation:** expand-conclusion
- **Before (lines 783–785):**

  > `The overall trend forecasts that this fundamental shift will be sustained. While Europe remains dependent on the United States for a substantial share of new equipment procurement in the near term (Howorth, 2025), the financials of the top ten European defence contractors demonstrate a clear strategic shift toward greater defence self-reliance.`
  >
  > `The 2022 war on Ukraine awakened the entire continent and the world. We can confidently say that the Peace Dividend era is fading and that the exclusion of defence companies from policy frameworks such as ESG is a bygone narrative. The defence industry today is no longer unanimously seen as a war-waging mechanism, but rather as an essential pillar of nations and the security of European society.`

- **After (draft, ~390 words; *NEW PROSE — generated by the planner, to be reviewed before commit*):**

  > **Research question.** This thesis asked whether Russia's February 2022 escalation of its war against Ukraine produced a *structural* shift — a permanent change in the parameters governing European defence companies — or merely a *cyclical* surge that will revert as the conflict winds down. The two hypotheses imply very different futures for capital allocation, industrial policy, and the post-Cold-War "peace dividend" frame, so the question is consequential beyond the academic.
  >
  > **Semantic evidence.** The narrative analysis of 79 annual reports (2018–2025) from ten listed European primes shows a sharp and sustained shift in management language. The mean structural-language score rose from 4.7 pre-invasion to 7.1 post-invasion and reached 8.1 by 2025; business-as-usual framings dropped from 22 of 40 reports to 4 of 39, while transformational framings rose from 1 to 23. Inter-rater agreement between two independent LLM scorers (Claude, Gemini) was Cohen's κ = 0.88 across the corpus and 0.94 post-invasion. A difference-in-differences design using commercial-aerospace firms as a control group isolates a treatment effect of +2.03 score points (p = 0.024), with parallel-trends holding at the 10 percent threshold (p = 0.086).
  >
  > **Financial evidence.** Three quantitative tests converge on the same direction. The Welch t-test finds the mean book-to-bill ratio rises from 1.20 to 1.75 (p = 0.0013) and the group EBIT margin rises by 2.7 percentage points, from 7.8 to 10.5 percent (p = 0.0041). The Chow test detects breaks in 8 of 60 firm-metric cells covering six of the ten firms. The panel fixed-effects regression, controlling for firm fixed effects and a pre-invasion trend, confirms the EBIT-margin shift at +2.69 pp (p = 0.037). Order-book signals are directionally consistent in the panel but not yet significant given the short post-event window.
  >
  > **Limitations and future work.** Four limitations qualify the inference. The sample is ten publicly listed primes; private and smaller contractors are excluded. The post-event window is three to four years, which limits the panel's power on volatile metrics. Annual reports reflect a management-eye view that is not free of advocacy. And by definition, a structural claim is forward-looking: a near-term geopolitical resolution, persistent US procurement dependence (Howorth 2025), or "war fatigue" could yet alter the trajectory. Future work should expand the firm sample, extend the post-2022 window as new years of data arrive, and decompose the cumulative effect of the 2014 and 2022 phases of the war.
  >
  > **A hedged close.** Subject to those caveats, the joint semantic and financial evidence assembled here is more consistent with a structural shift than a cyclical one. The most credible single number — a +2.69 pp EBIT-margin lift that survives firm fixed effects and a pre-trend control — supports a re-rating of European defence primes that is unlikely to unwind on the timescales studied. Whether the shift hardens into a new equilibrium or erodes will depend on European political will, the durability of EU-level procurement instruments, and the unresolved tension between strategic autonomy ambitions and continued near-term US dependence.

- **Cohesion targets to sweep:**
  - Line 294 ("the European defence industry has crossed a point of no return … a well-funded, united force ready for long-term global security"). The new Conclusion explicitly hedges, so the line-294 framing is partially in tension. Per CHANGELOG 064e4b3, line 294 carries its claim via attribution ("the research overwhelmingly agrees…"), which makes it a literature-summary statement rather than the paper's own claim — so retention is defensible. **Recommendation:** leave 294 alone; the new Conclusion's hedged close balances it. If the editor wants belt-and-braces, add "Subject to the caveats below" at the start of line 294 — but that is Tier 4.
  - "Peace Dividend era is fading" (line 785, deleted in this step) — confirm no surviving body sentence makes the same dramatic claim.
  - Line 783 phrasing "fundamental shift will be sustained" — gone after this edit.
- **Gonchar resolved:** 44 (i, ii, iii, iv, v all addressed). Implicitly closes the 064e4b3 follow-up on over-claim.
- **Risk:** medium. New prose is the highest-stakes change in the batch. Editor should review numbers against the body one more time before commit. All numbers in the draft above were extracted from: line 189 (4.7→7.1→8.1; book-to-bill 1.20→1.75; EBIT 7.8→10.5; firm list), line 481 (κ=0.88 / 0.94), line 583 (DiD +2.03), line 565 (parallel-trends p=0.086), line 604 (DiD p=0.024), line 645 (Welch p=0.0013, p=0.0041), line 717 (panel β=2.69, p=0.037), line 738 (8 of 60 cells, six of ten firms).

---

## 4. Risk register

| Risk | What goes wrong | Pre-commit check |
|:--|:--|:--|
| **TOC drift** | The TOC block (lines 75–157) keeps Google-Doc URLs and stale page numbers; readers of the rebuilt paper see a TOC that doesn't match the body. | After Step 11.1, grep TOC entries against actual `#`/`##` headings; ensure 1:1 match by title. |
| **Broken cross-refs to "aforementioned peace dividend"** | If `3. Background` ends up *after* `5. Theoretical Framework`, the "aforementioned" at line 316 is forward-pointing and reads wrong. | After Steps 1–10, confirm Background still precedes Theoretical Framework in body order. |
| **Orphaned transitional sentence in Framing Theory** | Step 6 removes the Cold-War paragraph. Line 336 ("The abrupt and emphatic change…") starts mid-contrast. | After Step 6, read 5.3 end-to-end. Flag bridge-sentence need for Tier 4. |
| **Orphaned transitional sentence in Signalling Theory** | Step 5 removes the "Prior to 2022 → no incentive" paragraph. Zeitenwende paragraph may now lead too abruptly. | After Step 5, read 5.2 end-to-end. Flag bridge-sentence need for Tier 4. |
| **Table/figure renumbering pressure** | None of the moves alter figure or table positions. Confirm Table 2 reference at line 738 still resolves. | grep `Table 2` post-Step-11; should resolve to Appendix A line 982. |
| **Heading-level depth violation in Step 11.4** | Promoting Contextualisation subsections from `###` to `##` is a real depth fix but if the editor forgets one, the renderer breaks. | grep `^###` after Step 11; expected only under 7.1 and 7.2. |
| **Step 8 framing-paragraph voice mismatch** | The new Lit Review opener I drafted is a placeholder. If pasted as-is, voice may not match Rienzo's. | Editor must rewrite the placeholder before commit; mark explicitly. |
| **Step 12 Conclusion numbers off by a digit** | The draft cites several numbers; a transcription error would be a referee-grade fact issue. | Cross-check every number in the Conclusion draft against the body lines listed above. |
| **`### Tests` bold-vs-level anomaly at line 637** | Currently rendered with both `###` and `**`; renaming to `### 7.2.2 Tests` may double-bold. | Verify rendered output in markdown preview after Step 11.3. |
| **`# Onglet 1` (line 1) port artifact** | Cosmetic; not in scope but shows up in any rendered TOC. | Out of scope. Tag for Tier 4. |
| **Gonchar 6 ("sin stocks relevance") and Gonchar 13/14/15/16/19/20/26/27/30/32/33** are content prose changes that are NOT in this Tier-3 batch. | Editor may be tempted to address them while in the same area; resist — they are Tier 4. | When a Tier-3 step touches a paragraph carrying an open Tier-4 Gonchar id, do not co-edit. Add a comment in the commit message noting "Tier 4 candidate retained: Gonchar id N". |

---

## 5. Recommended order of execution

The edits cluster into four phases. Within a phase, ordering is suggested; across phases, ordering is required.

**Phase A — Backbone renames (sequential, low risk):**
1. Step 1 (rename Lit Review → Background)
2. Step 9 (rename Theoretical Framework + numerals)

These two are pure renames and unblock everything else. Doing them first means subsequent moves land into the new headings cleanly.

**Phase B — Background assembly (sequential, content-heavy):**
3. Step 2 (insert `3.1` heading)
4. Step 3 (move cyclical-evidence material into `3.1`)
5. Step 4 (insert `3.2` heading + relocate post-invasion-response material)
6. Step 5 (move "Prior to 2022 …" paragraph into `3.1`)
7. Step 6 (move "For many years after the Cold War …" paragraph into `3.1`)

These must run sequentially because each step's `before-string` matchability depends on the previous step's outcome.

**Phase C — Methodology / Data / Lit-Review insertion (mixed):**
8. Step 7 (move Detecting Structural Change into `5.1`) — independent of Phase B; could run in parallel after Phase A
9. Step 8 (insert new `4. Literature Review`) — depends on Phase B (the Microeconomic-Transition opener is freed up by Step 4)
10. Step 10 (promote Data, renumber Mixed Methods) — independent; could run after Phase A

Phase C steps 8 and 10 do not depend on each other; 9 depends on Step 4. Order: 7, 10, 8 (preferred) or 10, 7, 8.

**Phase D — Cleanup and Conclusion (sequential):**
11. Step 11 (TOC rebuild + flatten `####` + Contextualisation renumber + Exec/Intro/Conclusion numerals)
12. Step 12 (Conclusion expansion)

Step 11 must run after all of Phase A–C so that the rebuilt TOC reflects the final structure. Step 12 runs last because (a) the Conclusion expansion is the largest single prose insertion and reviewing it in isolation is easier when the rest of the paper has stabilised, and (b) the "research question" recap should reference final section numbering.

**Parallelisable pairs:** Step 7 ↔ Step 10. Otherwise sequential.

**Total commits expected:** 12 conceptual steps; the editor may break Step 11 into 3–4 small commits, so realistic commit count is 14–16.
