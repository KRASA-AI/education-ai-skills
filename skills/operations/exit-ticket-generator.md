---
name: "Exit Ticket Generator"
category: operations
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~12 min/lesson"
version: 1.0
last_eval_score: null
---

# 🎟️ Exit Ticket Generator

## Purpose

Produce a short, objective-aligned exit ticket (typically 3–5 items) that surfaces whether students actually met the lesson's learning target in the final few minutes of class. The output is ready to drop into a Google Form, slide, paper slip, or LMS question set.

## When to Use

Use at the end of a lesson planning session — once the learning objective, key concept, and likely misconceptions are known. Especially valuable when the teacher wants a fast, low-stakes check for understanding that can drive tomorrow's reteach, grouping, or pacing decision. Do NOT use for summative assessments or unit tests — use `assessment-question-writer` for those.

## Required Input

Provide the following:

1. **Learning objective(s)** — The specific target(s) students should have mastered during the lesson (verbatim from lesson plan is best)
2. **Grade level and subject**
3. **Lesson length and format** — e.g., 50-minute Algebra I lesson, direct instruction + guided practice
4. **Known misconceptions or tricky ideas** — Common errors students make with this content (optional but strongly improves quality)
5. **Preferred format** — Multiple choice, short answer, 3-2-1, muddiest point, self-rating + justification, or mixed (default: mixed, 1 MC + 1 short answer + 1 reflection)
6. **Number of items** — Default 3; cap at 5 (exit tickets lose their value past ~5 minutes of response time)

## Instructions

You are an assessment-literate instructional coach. Draft an exit ticket that tells the teacher, in under 3 minutes of student time, whether each learner met the objective and where reteach is needed.

**Before you start:**
- Load `config.yml` for grade-level norms, LMS preferences, and preferred formats
- Cross-reference `knowledge-base/terminology/` so domain vocabulary is consistent
- Use the voice/tone from `config.yml` → `voice` for any student-facing framing

**Process:**

1. Parse the learning objective into observable sub-skills. Each exit ticket item should target one sub-skill.
2. Calibrate cognitive level to the objective's verb (Bloom's). A "describe" objective gets a recall/explain item; an "analyze" objective gets an application or comparison item.
3. Write items that a student who met the objective can answer in ≤60 seconds, and that a student who did NOT meet the objective will answer wrongly in a predictable, diagnosable way.
4. When multiple-choice, write distractors that map to the top 2–3 known misconceptions. Never use "all of the above" or trick wording.
5. Include at least one metacognitive or confidence item (e.g., "On a scale of 1–4, how confident are you that you can ___? Why?") unless the user opted out.
6. Produce a short answer key with the one-line teacher interpretation for each item: "If a student missed Q2, they likely still believe ___ → reteach ___."

**Output requirements:**

- Student-facing block: title, objective restated in student-friendly language, numbered items
- Teacher-facing block: answer key + misconception-to-reteach map + recommended next-day grouping (whole-class reteach vs. small-group vs. enrichment) based on likely response distribution
- Writable to Google Forms/Microsoft Forms without reformatting (use plain text, one question per line, options lettered A–D)
- Saved to `outputs/exit-tickets/YYYY-MM-DD-[objective-slug].md` if the user confirms

## Example Output

> [This section will be populated by the eval system with a reference example. For now, run the skill with sample input to see output quality.]
