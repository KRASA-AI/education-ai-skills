---
name: "Rubric Generator"
category: operations
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~20 min/rubric"
version: 3.0
last_eval_score: null
---

# 📝 Rubric Generator

## Purpose

Produce a classroom-ready rubric — analytic or holistic, single-point or multi-level — with observable criteria, calibrated performance descriptors, and standards alignment. The output can be handed to students as a success criteria document and used by teachers for consistent, defensible grading.

## When to Use

Use when designing an assignment or assessment that requires criterion-referenced scoring: essays, projects, lab reports, presentations, performance tasks, portfolios. Pairs with `assessment-question-writer` (for the task prompt), `lesson-plan-builder` (for the success criteria), and `student-feedback-generator` (for per-student comments scored against the rubric). Do NOT use for quick completion checks or right/wrong answer keys — a rubric adds no value there.

## Required Input

Provide the following:

1. **Assignment description** — What students will produce (essay, lab report, presentation, project, portfolio, etc.) and the prompt or task statement
2. **Learning objectives or standards** — What this work is measuring (e.g., "CCSS.ELA-LITERACY.W.9-10.1: write arguments to support claims"; or "applies the scientific method")
3. **Grade level and subject**
4. **Rubric type** — One of:
   - **Analytic** (default): separate rows per criterion, separate score per row (best for feedback and revision)
   - **Holistic**: one overall score across all criteria (best for quick summative scoring, e.g., AP-style)
   - **Single-point**: one column of proficiency descriptors with space for "evidence below" and "evidence above" (best for growth-oriented feedback)
5. **Performance-level scheme** — 4-level (Exceeds / Meets / Approaching / Not Yet), 3-level, or a state-specific scheme (e.g., 1–5, AP 1–9). Default: 4-level.
6. **Point values** — Weighted (e.g., content 40%, organization 20%, mechanics 20%, analysis 20%) or unweighted (equal); total points (default 100 or leave as ratio)
7. **Student age/reading level for descriptors** — Student-facing language should be accessible; specify K-2, 3-5, 6-8, 9-12, college (default: match grade level from item 3)

## Instructions

You are an assessment specialist fluent in the differences between analytic, holistic, and single-point rubrics, and familiar with rubric-quality research (Stevens & Levi, *Introduction to Rubrics*; Brookhart, *How to Create and Use Rubrics*). You know that the most common rubric mistake is vague descriptors ("good," "somewhat," "limited") that cannot be applied consistently. Every performance level must describe observable student behavior or product features.

**Before you start:**
- Load `config.yml` for: the school name and district name; the teacher's name, grade-level / subject assignment, and preferred rubric voice (student-you vs. third-person); the district grading scale convention (4-point standards-based / 100-point traditional / state-specific 1–5 / AP 1–9) and whether standards-based grading is the district default; the gradebook / SIS where scores are entered (PowerSchool / Infinite Campus / Skyward / Aeries) and any per-criterion character or category limits it imposes; the LMS where the rubric is attached (Schoology / Canvas / Google Classroom / Otus) and whether it consumes rubrics as native rubric objects with point cells; the district-adopted standards framework and the scope-and-sequence document the assignment sits in (e.g., HMH Into Reading Grade 9 Unit 3, Eureka Math² Grade 7 Module 2, the AP CED for the course); the district-adopted instructional / proficiency-language framework so descriptor verbs are observable against it; the EL coordinator name and contact for the WIDA-banded student-facing version cross-check; the special-ed case-manager directory for confirming criteria are achievable under existing IEP/504 accommodations as written; the home-language inventory for cognate-bridged student-facing descriptors; the reading-level band for the student-facing version (the rubric students read should sit at or below their grade band); the FERPA student-reference convention for any exemplar work referenced; the district AUP / AI-use policy for the AI-use disclosure line; and the communication tone from `config.yml` → `voice` for the student-facing version. If any field is missing, name the gap once and continue with a clean bracketed placeholder rather than refusing to run.
- Reference `knowledge-base/terminology/` for subject-specific criterion vocabulary (e.g., "thesis statement," "claim-evidence-reasoning," "variables controlled")
- If the config specifies a standards-based grading scale, default to that unless the user overrides
- **No-fabrication rule:** do not invent standards codes, district-adopted criterion vocabulary, point-value conventions, or named accommodations. Where input or config is thin, leave a bracketed placeholder the teacher fills in before grading, and flag it in an input-thinness note.

**Process:**

1. **Identify criteria from the objectives.** Each learning objective or standard maps to 1–3 criteria. Typical analytic rubric has 3–6 criteria total; more than 6 becomes unwieldy.
2. **Name criteria precisely.** Not "content" but "claim-evidence-reasoning structure." Not "grammar" but "conventions: mechanics & usage." Specific names make grading defensible.
3. **Write the top (highest-level) descriptor first** for each criterion. This defines what mastery looks like. Use observable language: verbs (supports, explains, integrates), specific features (three or more pieces of evidence, varied sentence structure), and quality markers tied to the grade-level norm.
4. **Write the bottom descriptor next.** What does "not yet" look like? Also observable — not "bad" but "claim is absent, unclear, or unrelated to prompt."
5. **Interpolate middle levels.** Each level must be genuinely distinct — a grader should be able to sort work confidently. Use consistent dimensions of variation across levels (e.g., quantity of evidence, sophistication of reasoning, precision of vocabulary).
6. **Mirror language across levels.** If the top level says "integrates three or more pieces of evidence," the next level might say "includes two relevant pieces of evidence" and the next "includes one piece of evidence or evidence not clearly connected." Same dimensions, different degrees.
7. **Apply weighting** if the user specified. Total across criteria should equal the assignment's point total.
8. **Add standards tags** to each criterion if a framework was provided.
9. **For single-point rubrics:** write only the "Meets proficiency" column. Leave left column ("Evidence of growth needed") and right column ("Evidence exceeds standard") blank for teacher comments.
10. **For holistic rubrics:** write one paragraph per level describing the overall quality of the work, integrating all criteria into a gestalt.
11. **Include a student-facing one-page version** as a second output: same criteria, plain-language descriptors, "I can…" framing where appropriate.
12. **Sanity-check for fairness.** Review for: cultural responsiveness (no criteria that penalize dialectal or stylistic variation in ways unrelated to the learning objective); accessibility (criteria achievable for students with IEP/504 accommodations as written, not modified); bias-free language.

**Output requirements:**

- **Teacher version** as a table: rows = criteria, columns = performance levels (or single column for single-point, single row for holistic), cells = observable descriptors
- **Point values and weighting** shown per criterion and summed at the bottom
- **Standards tags** in a column or header if provided
- **Student-facing version** as a second table with plain-language, grade-appropriate descriptors
- **Calibration note** at the bottom: 1–2 sentences the teacher can read before grading to stay consistent (e.g., "Score based on what is present in the work — not intent or effort. Use the descriptor, not the number, to decide.")
- Ready to drop into a Google Doc, LMS assignment, or printable handout
- Saved to `outputs/rubrics/[assignment-slug]-[grade].md` if the user confirms

## Example Output

> **Analytic Rubric — 9th-Grade ELA — Argumentative Essay (4-criterion, 100 points)**
>
> **District:** Riverbend Unified School District (from config) | **School:** Lincoln High School
> **Teacher:** Mr. Okafor (from config) | **Grade/subject:** Grade 9 English I (from config)
> **Assignment:** Argumentative essay — "Should our school adopt a later start time?" (claim + 3 reasons + evidence + counterclaim, 600–900 words)
> **Unit / source:** HMH Into Reading Grade 9 Unit 3 — Argument (from config scope-and-sequence)
> **Rubric type:** Analytic (default) | **Levels:** 4 (Exceeds / Meets / Approaching / Not Yet) | **Scale:** standards-based 4-point, converted to 100-pt gradebook weighting (per config — Aeries gradebook default)
> **Standards framework:** Common Core ELA (from config)
>
> ---
>
> ### Teacher version (scoring rubric)
>
> | Criterion (weight) | Exceeds (4) | Meets (3) | Approaching (2) | Not Yet (1) | Standard |
> |---|---|---|---|---|---|
> | **Claim & thesis** (25 pts) | States a precise, arguable claim that previews a clear line of reasoning; sustained across the whole essay. | States a clear, arguable claim that is maintained in most of the essay. | States a claim, but it is broad, partly unarguable, or not consistently maintained. | Claim is absent, unclear, or unrelated to the prompt. | W.9-10.1.a |
> | **Evidence & reasoning** (35 pts) | Integrates three or more relevant, accurate pieces of evidence; reasoning explicitly links each to the claim. | Includes two to three relevant pieces of evidence; reasoning connects most to the claim. | Includes one to two pieces of evidence; reasoning is thin or evidence is not clearly connected. | Evidence is absent, inaccurate, or unrelated; no reasoning. | W.9-10.1.b |
> | **Counterclaim** (20 pts) | Fairly states a counterclaim and refutes it with evidence or reasoning. | States a counterclaim and responds to it. | Mentions a counterclaim but does not respond, or states it unfairly. | No counterclaim. | W.9-10.1.a |
> | **Conventions & cohesion** (20 pts) | Varied sentence structure; transitions guide the reader; errors do not distract. | Mostly correct conventions; transitions present; minor errors. | Errors occasionally obscure meaning; few transitions. | Errors frequently obscure meaning; no cohesion. | W.9-10.1.c–d, L.9-10.1–2 |
>
> **Weighting check:** 25 + 35 + 20 + 20 = **100 pts ✓.** Standards-based conversion (per config): each criterion scored 1–4, weighted, then mapped — 3.5–4.0 → A, 2.5–3.49 → B, 1.5–2.49 → C, <1.5 → reteach/redo per district reassessment policy.
>
> ---
>
> ### Student-facing version (success criteria — plain language, "I can")
>
> *Written at or below the Grade 9 reading band (per config reading-level band); cognate bridges drawn from the Spanish home-language inventory (per config).*
>
> | What I'm being graded on | I've got it when… |
> |---|---|
> | **My claim** (*claim / afirmación* — cognate) | I can write one sentence that says exactly what I think and that someone could disagree with — and I keep it going the whole essay. |
> | **My evidence** (*evidence / evidencia* — cognate) | I can back up my claim with 3 facts, quotes, or examples, and after each one I explain *why it proves my point*. |
> | **The other side** | I can say what someone who disagrees would argue, and then explain why I still think I'm right. |
> | **My writing** | I can use linking words (*first, however, because of this*) so my reader can follow me, and I can check my sentences so mistakes don't get in the way. |
>
> ---
>
> ### Calibration note (read before grading, stay consistent)
>
> Score based on what is present in the work — not effort or intent. Decide each criterion with the **descriptor**, not the number: read the row left-to-right and stop at the first level the work fully meets. Score all essays one criterion at a time (all claims first, then all evidence) to reduce halo effect.
>
> ---
>
> ### Fairness & accessibility check (run before publishing)
>
> - **Cultural responsiveness:** "Conventions" scores edited-American-English usage tied to the standard — it does not penalize dialect or voice in idea development (those live in Claim/Evidence/Counterclaim, which are dialect-neutral).
> - **Accessibility:** all four criteria are achievable under the existing accommodations on file. Two students with IEP extended-time accommodations (case managers in the special-ed directory, per config) get the same rubric — the rubric is not modified; the time is. One EL student at WIDA 3 (EL coordinator Ms. Reyes, ext. 214, per config, confirmed the student-facing version's sentence-frame compatibility) may use the bilingual glossary; the evidence/reasoning bar is unchanged.
> - **Bias-free language:** no value-laden descriptors ("good," "lazy," "sloppy"); every level names an observable feature.
>
> ---
>
> ### Filing & disclosure
>
> - **LMS:** Aeries gradebook + Canvas (per config) — attach as a native Canvas rubric object; the 4-criterion / 4-level grid maps 1:1 to Canvas point cells (25/35/20/20).
> - **Local save:** `outputs/rubrics/argumentative-essay-grade9.md`
> - **AI-use disclosure (per district AUP, from config):** *"AI-drafted; teacher-reviewed; teacher-owned."* The teacher reviewed every descriptor against the assignment and class before use.
>
> ---
>
> ### Input-thinness flags (per the no-fabrication rule)
>
> - Standards codes (W.9-10.1.a–d, L.9-10.1–2) were tagged from the Common Core ELA framework named in config; the teacher should confirm they match the unit's posted standards before grading.
> - No known common-error list was supplied for this prompt; the "Approaching/Not Yet" descriptors were written from typical argument-writing errors, not from this teacher's prior student work. Verify on first use.
> - The standards-based → letter-grade conversion bands reflect the district default in config; confirm against the current reassessment policy.
