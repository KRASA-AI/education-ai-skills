---
name: "Rubric Generator"
category: operations
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~20 min/rubric"
version: 2.0
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
- Load `config.yml` for school/org name, grading scale conventions (e.g., 4-point standards-based vs. 100-point traditional), and preferred rubric voice (student-you vs. third-person)
- Reference `knowledge-base/terminology/` for subject-specific criterion vocabulary (e.g., "thesis statement," "claim-evidence-reasoning," "variables controlled")
- If the config specifies a standards-based grading scale, default to that unless the user overrides

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

> [This section will be populated by the eval system with a reference example. For now, run the skill with sample input to see output quality.]
