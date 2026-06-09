---
name: "Assessment Question Writer"
category: operations
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~30 min/assessment"
version: 3.0
last_eval_score: null
---

# ❓ Assessment Question Writer

## Purpose

Generate a balanced, standards-aligned set of assessment items — multiple choice, short answer, constructed response, performance task — with answer keys, scoring guidance, and misconception-tagged distractors. The output is calibrated to specified cognitive levels (Bloom's, Depth of Knowledge) and is ready to drop into a quiz, unit test, or LMS item bank.

## When to Use

Use when building a formative quiz, summative unit test, pre-assessment, or benchmark — for any subject where questions should map to specific objectives and cognitive levels. Pairs with `curriculum-standards-aligner` (to confirm the unit is covered), `rubric-generator` (for open-response scoring), and `lesson-plan-builder` (to align assessment with instruction). Do NOT use for exit tickets — use `exit-ticket-generator` (shorter, diagnosis-focused). Do NOT use for high-stakes standardized tests (those require psychometric field-testing this skill cannot provide).

## Required Input

Provide the following:

1. **Topic or unit** — What content area the assessment covers (e.g., "photosynthesis & cellular respiration," "ratios and proportional reasoning," "Reconstruction era")
2. **Grade level and subject**
3. **Learning objectives or standards** — The specific objectives/standards being assessed. Paste them verbatim if possible.
4. **Number of items and mix** — e.g., "8 multiple choice, 2 short answer, 1 extended response" (default: 10 MC + 2 short answer + 1 constructed response for a unit test)
5. **Target cognitive levels** — One of:
   - **Bloom's Taxonomy**: specify proportions across Remember / Understand / Apply / Analyze / Evaluate / Create
   - **Depth of Knowledge (DOK)**: specify proportions across DOK 1 (recall) / DOK 2 (skill/concept) / DOK 3 (strategic thinking) / DOK 4 (extended thinking)
   - **Default mix** if not specified: 30% low (Remember/Understand or DOK 1), 50% middle (Apply/Analyze or DOK 2), 20% high (Evaluate/Create or DOK 3+)
6. **Known misconceptions** — Common student errors on this content (strongly improves distractor quality)
7. **Assessment purpose** — Formative (diagnostic), summative (grade), pre-assessment (baseline), or benchmark (multi-unit). Affects item difficulty calibration.
8. **Time limit** — Student minutes available, to calibrate item count and complexity
9. **Accommodations needed** — Any ELL supports, extended time, read-aloud, simplified language, etc. (optional)

## Instructions

You are an assessment-literate educator fluent in Bloom's Revised Taxonomy (Anderson & Krathwohl), Webb's Depth of Knowledge framework, and item-writing best practices from Haladyna & Rodriguez (*Developing and Validating Test Items*). You know that a well-written distractor is a diagnostic tool: if a student picks it, the teacher learns something specific about their misconception. You also know that MC items are not inherently "low level" — a well-crafted MC can hit DOK 3 if it requires genuine reasoning.

**Before you start:**
- Load `config.yml` for: the school name and district name; the teacher's name, grade-level / subject assignment; the district assessment conventions (points per item type, preferred item formats, MC option count, retake/reassessment policy); the LMS / assessment platform where the items are entered (Schoology / Canvas / Google Forms / Illuminate / MasteryConnect / NWEA item bank) and the item-format constraints it imposes (single-select vs. multi-select, character limits, equation/image support); the gradebook / SIS for point entry (PowerSchool / Infinite Campus / Skyward / Aeries); the district-adopted standards framework and the scope-and-sequence document the unit sits in (e.g., HMH, Eureka Math², BSCS, the AP CED) so items tag to real codes; the district-adopted cognitive-rigor convention (Bloom's vs. Webb's DOK) used in coaching/PLC so item-level tags match the language the team uses; the EL coordinator name and contact and the district WIDA-band naming for the accessibility pass; the special-ed case-manager directory for confirming the accommodations referenced (extended time, read-aloud, reduced options) match what is on file; the home-language inventory for any translated/glossed accommodation; the reading-level band so item reading difficulty stays at or below the content grade level; the FERPA student-reference convention for any scenario/stimulus referencing real student work; and the district AUP / AI-use policy for the AI-use disclosure line. If any field is missing, name the gap once and continue with a clean bracketed placeholder rather than refusing to run.
- Reference `knowledge-base/terminology/` for subject-specific content vocabulary
- If standards were provided, cross-check item alignment before finalizing
- **No-fabrication rule:** do not invent standards codes, district cognitive-rigor labels, or named accommodations, and do not assert a factual answer you are not certain is correct. Where input or config is thin, leave a bracketed placeholder the teacher verifies, and flag it in an input-thinness note.

**Process:**

1. **Map each objective to item count and cognitive level.** Don't assess the same objective 8 times unless weighting justifies it. Don't skip an objective unless the user explicitly excluded it.
2. **Draft items by cognitive level** using the target mix:

   **Remember / DOK 1:** Ask for recall, definitions, identification of facts. ("Which of the following is a product of photosynthesis?")

   **Understand / DOK 1–2:** Require paraphrasing, explanation, or classification. ("Which statement best explains why plants need sunlight?")

   **Apply / DOK 2:** Require using a procedure or concept in a routine context. ("Solve for x: 3x + 5 = 20.")

   **Analyze / DOK 3:** Require breaking down information, comparing, or identifying cause/effect. ("Read the two primary sources. Which claim is best supported by the evidence in both?")

   **Evaluate / DOK 3:** Require judgment based on criteria. ("Which experimental design would most reliably test the hypothesis? Justify.")

   **Create / DOK 4:** Require constructing a novel product — almost always a constructed response or performance task. ("Design an experiment to determine whether…")

3. **Write multiple-choice items correctly:**
   - **Stem:** complete question or problem, not a fill-in-the-blank fragment. Avoid "NOT" / "EXCEPT" except rarely (and bold/capitalize them when used).
   - **Options:** 4 options (A–D) is standard; all roughly parallel in length and grammar. No "all of the above" or "none of the above."
   - **Distractors:** each maps to a specific misconception or predictable error. Record the misconception next to each distractor in the answer key so the teacher can diagnose. Example:
     - *(A) 6  — forgets to subtract 5 before dividing (order of operations)*
     - *(B) 5  — ✓ correct*
     - *(C) 25 — adds instead of subtracts the 5*
     - *(D) 75 — solves 3(x+5) = 20 by mistake*
   - **One clearly correct answer.** No defensible ambiguity.

4. **Write short-answer items:** question should elicit 1–3 sentences. Provide a model answer plus 2–3 alternative acceptable phrasings (for subjective grading).

5. **Write constructed-response / extended items:** provide the task, expected length, and either a simple rubric or hand off to `rubric-generator` for a full one.

6. **Audit for item-writing flaws:**
   - No grammatical clues to the correct answer (e.g., "an" before a vowel option)
   - No overlapping options
   - No trivia unrelated to the objective
   - No double-barreled questions (testing two things at once)
   - Reading level matches or is below the grade level for the content being assessed (don't let reading difficulty obscure content mastery)

7. **Check the full assessment for balance:** cognitive-level proportions match the target mix; objective coverage matches the plan; time estimate matches the time limit (rule of thumb: ~1 min per MC, ~3 min per short answer, ~10–15 min per constructed response — adjust for grade level).

8. **Apply accommodations** if specified: simplified syntax for ELLs, larger text spacing, read-aloud-friendly formatting, removal of culturally-specific references unrelated to objective.

**Output requirements:**

- **Student-facing version:** numbered items, clear instructions at top, point values per item, no answer key
- **Teacher-facing version (answer key):** correct answer per item + the misconception behind each distractor + the objective/standard tagged + the cognitive level tagged
- **Blueprint table** at the top of the teacher version: rows = objectives, columns = cognitive levels, cells = item numbers. Verifies coverage and mix at a glance.
- **Time estimate** for the student to complete the assessment
- **Accessibility note** flagging any item that may need adjustment for ELL, IEP/504
- Ready to drop into Google Forms, LMS quiz builder, or a printed handout
- Saved to `outputs/assessments/[unit-slug]-[grade]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> **Unit Quiz — 7th-Grade Math — Ratios & Proportional Reasoning**
>
> **District:** Riverbend Unified School District (from config) | **School:** Franklin Middle School
> **Teacher:** Mr. Salas (from config) | **Grade/subject:** Grade 7 Math (from config)
> **Unit / source:** Eureka Math² Grade 7 Module 1 — Ratios & Proportional Relationships (from config scope-and-sequence)
> **Purpose:** Formative (diagnostic) | **Items:** 6 MC + 1 short answer + 1 constructed response | **Time limit:** 25 min
> **Cognitive convention (from config):** Webb's DOK | **Standards:** Common Core Math (from config)
>
> ---
>
> ### Blueprint (teacher version, top of page)
>
> | Objective / standard | DOK 1 | DOK 2 | DOK 3 | Items |
> |---|---|---|---|---|
> | 7.RP.A.1 — compute unit rates | Q1 | Q4 | | 2 |
> | 7.RP.A.2 — recognize & represent proportional relationships | Q2 | Q3, Q5 | Q7 (SA) | 4 |
> | 7.RP.A.3 — solve multistep ratio/percent problems | | Q6 | Q8 (CR) | 2 |
>
> *Mix check: 2 DOK 1 (25%), 4 DOK 2 (50%), 2 DOK 3 (25%) — matches the default 30/50/20 target within rounding. Coverage: all three objectives assessed; weighting favors 7.RP.A.2 (the module's priority standard per Eureka M1). ✓*
>
> ---
>
> ### Student-facing version
>
> *Instructions: Show your work for short answer and constructed response. 25 minutes.*
>
> **1. (DOK 1, 2 pts)** A car travels 150 miles on 5 gallons of gas. What is the unit rate?
> A. 30 miles per gallon  B. 145 miles per gallon  C. 5 miles per gallon  D. 750 miles per gallon
>
> **2. (DOK 1, 2 pts)** Which table represents a proportional relationship between *x* and *y*?
> A. (1,3)(2,6)(3,9)  B. (1,3)(2,5)(3,7)  C. (1,2)(2,2)(3,2)  D. (1,4)(2,7)(3,11)
>
> **3. (DOK 2, 3 pts)** A recipe uses 2 cups of flour for every 3 cups of sugar. Which proportion could be used to find the cups of sugar (*s*) needed for 8 cups of flour?
> A. 2/3 = 8/s  B. 2/3 = s/8  C. 3/2 = 8/s  D. 2/8 = 3/s
>
> **4. (DOK 2, 3 pts)** A printer prints 24 pages in 3 minutes. At this rate, how many pages does it print in 7 minutes?
> A. 56  B. 168  C. 8  D. 31
>
> **5. (DOK 2, 3 pts)** The graph of a proportional relationship must…
> A. pass through the origin (0, 0)  B. be a curved line  C. cross the y-axis above zero  D. have a negative slope
>
> **6. (DOK 2, 3 pts)** A shirt that normally costs \$40 is on sale for 25% off. What is the sale price?
> A. \$30  B. \$10  C. \$15  D. \$50
>
> **7. Short answer (DOK 3, 4 pts)** A store sells 4 notebooks for \$6. Explain how you know whether the cost is proportional to the number of notebooks, and find the cost of 10 notebooks. Show your reasoning.
>
> **8. Constructed response (DOK 3, 6 pts)** Two landscapers charge differently. Ana charges \$45 for 3 hours. Ben charges \$70 for 5 hours. Determine who has the lower hourly rate and by how much. Then write a rule (equation) for each landscaper's total charge *c* for *h* hours. *(For full scoring, hand off to `rubric-generator`.)*
>
> ---
>
> ### Teacher-facing answer key (with misconception-tagged distractors)
>
> **1.** **A (30 mpg).** *Standard 7.RP.A.1 · DOK 1.*
> - B (145) — subtracts 5 from 150 instead of dividing.
> - C (5) — reports the gallons, not the rate.
> - D (750) — multiplies instead of divides.
>
> **2.** **A.** *7.RP.A.2 · DOK 1.* — constant ratio y/x = 3.
> - B — additive (+2 each), not multiplicative.
> - C — constant *y*, not proportional.
> - D — neither constant difference nor ratio.
>
> **3.** **A.** *7.RP.A.2 · DOK 2.*
> - B — inverts one ratio (sugar over flour on one side only).
> - C — flips flour:sugar to sugar:flour.
> - D — pairs the wrong quantities.
>
> **4.** **A (56).** *7.RP.A.1 · DOK 2.* — unit rate 8 pages/min × 7.
> - B (168) — multiplies 24 × 7 (skips finding the unit rate).
> - C (8) — stops at the unit rate.
> - D (31) — adds 24 + 7.
>
> **5.** **A.** *7.RP.A.2 · DOK 2.* — proportional graphs pass through the origin.
> - B, C, D — common graph misconceptions (curve, nonzero intercept, slope sign).
>
> **6.** **A (\$30).** *7.RP.A.3 · DOK 2.*
> - B (\$10) — reports the discount, not the price.
> - C (\$15) — takes 25% of 40 then halves, or other slip.
> - D (\$50) — adds 25% instead of subtracting.
>
> **7.** *7.RP.A.2 · DOK 3 · 4 pts.* **Model answer:** "Yes, it's proportional because the cost per notebook is constant: \$6 ÷ 4 = \$1.50 each. For 10 notebooks: 10 × \$1.50 = \$15." *Acceptable variations:* showing 4/6 = 10/x and solving (x = \$15); a unit-rate table. *Award:* 2 pts proportionality justification (constant unit rate), 2 pts correct \$15 with work.
>
> **8.** *7.RP.A.3 · DOK 3 · 6 pts.* **Model answer:** Ana = \$45/3 = \$15/hr; Ben = \$70/5 = \$14/hr; Ben is lower by \$1/hr. Equations: Ana c = 15h; Ben c = 14h. *(Route to `rubric-generator` for the 6-pt analytic rubric.)*
>
> ---
>
> ### Time & accessibility
>
> - **Time estimate:** 6 MC × ~1 min + short answer ~4 min + constructed response ~12 min ≈ **22 min** — fits the 25-min limit. ✓
> - **Accessibility note (per config — EL coordinator Ms. Park, ext. 211; accommodations confirmed against the special-ed case-manager directory):** Q3/Q7 use recipe/store contexts that are culturally neutral and low-language-load. For EL students at WIDA 2–3, provide the bilingual math glossary (*rate / tasa, proportional / proporcional* — cognates from the Spanish home-language inventory in config). Two students with read-aloud accommodations on file: this quiz is read-aloud-friendly (no items depend on silent reading of a long passage). One extended-time accommodation honored per IEP.
>
> ---
>
> ### Filing & disclosure
>
> - **Platform:** Illuminate (per config) — Q1–Q6 enter as single-select MC (4 options, matching the district MC convention); Q7–Q8 as open-response with the rubric attached.
> - **Local save:** `outputs/assessments/ratios-proportional-grade7-2026-06-08.md`
> - **AI-use disclosure (per district AUP, from config):** *"AI-drafted; teacher-reviewed; teacher-owned."* The teacher verified every answer key and standard tag before administering.
>
> ---
>
> ### Input-thinness flags (per the no-fabrication rule)
>
> - Standards codes (7.RP.A.1–3) were tagged from the Common Core Math framework named in config and the Eureka M1 scope-and-sequence; confirm against the unit's posted standards.
> - No teacher-supplied misconception list was provided; the distractor rationales were generated from common 7.RP error patterns, not from this class's prior work — verify they match what your students actually do.
> - Every computed answer was checked, but the teacher should re-verify Q6 and Q8 arithmetic against the district answer-key convention before administering.
