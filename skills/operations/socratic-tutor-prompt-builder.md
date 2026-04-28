---
name: "Socratic Tutor Prompt Builder"
category: operations
tools: [claude, chatgpt]
difficulty: advanced
time_saved: "~40 min/tutor-prompt build"
version: 1.0
last_eval_score: null
---

# 🧠 Socratic Tutor Prompt Builder

## Purpose

Construct a reusable system-prompt scaffold for a Socratic AI tutor agent — a tutor that asks rather than answers, scaffolds reasoning instead of supplying it, and adapts question depth to the student's response. Output is a deployable system prompt for the school's approved AI tool (Khanmigo Custom, MagicSchool Student-side, SchoolAI Spaces, district-licensed Copilot/Gemini for Education, ChatGPT Edu, or a custom GPT/Project), plus the teacher-facing companion: a scope statement, the off-topic and unsafe-topic stop conditions, the give-the-answer escape hatch, and a sample 4-turn dialogue showing what good and bad responses look like. Designed around the four design principles the Socratic-AI-tutor research literature has converged on: structured questioning patterns, adaptive scaffolding, reflective pauses, and human teacher oversight of transcripts.

## When to Use

Use to build a Socratic tutor prompt for a specific learning objective — a fraction concept, a paragraph claim-evidence move, a chemistry stoichiometry step, a Spanish past-tense conjugation, an essay thesis revision. Also use to retrofit a generic chatbot conversation into a Socratic-mode conversation by pasting the prompt at the start of a session. Also use for student-led-learning workflows where the teacher wants to add a tutor agent to a workstation rotation. Do NOT use to design a tutor that gives direct answers (use a different skill for direct-instruction prompts). Do NOT use for assessment-of-learning workflows (Socratic dialogue is formative; if you need a graded judgment, use Assessment Question Writer). Do NOT use for therapy-adjacent or social-emotional support conversations (those belong with a human counselor; the prompt's safety stop conditions explicitly route those out).

## Required Input

Provide the following:

1. **Subject and grade band** — Subject and grade; the question patterns and vocabulary scale with grade
2. **One specific learning objective** — The single objective the tutor scaffolds toward (e.g., "Student can use evidence from the text to support a written claim"). One objective per prompt; multiple objectives create a tutor that drifts.
3. **The student's expected entry point** — What the student already knows and what their typical first answer or first attempt looks like. Knowing the entry point lets the prompt scaffold from there rather than from an idealized starting position.
4. **The student's expected misconceptions** — The two or three predictable wrong-but-reasonable moves the student is likely to make. Each becomes a Socratic-question branch in the prompt.
5. **Approved tool and deployment surface** — Khanmigo Custom Tutor, MagicSchool Student, SchoolAI Space, Copilot/Gemini for Education, ChatGPT Edu / Custom GPT / Project, district-internal LLM. The surface dictates the system-prompt format and the available memory/safety controls.
6. **Conversation length expectation** — Average turn count expected (3–5 / 6–10 / 10+); the prompt budgets question depth accordingly
7. **Scope hard-stops** — Topics off-limits even within subject (e.g., a math tutor that should not discuss the unit's upcoming summative; a writing tutor that should not write the student's essay; a science tutor that should not provide the lab's measurements before the student takes them)
8. **Subject-adjacent safety triggers** — Self-harm, mental-health crisis, abuse disclosure, weapon ideation, peer-conflict report, medication question, immigration concern, sexual-content query — these trigger the same out-of-scope routing regardless of subject
9. **Give-the-answer escape hatch** — When (and how) the tutor moves out of Socratic mode into direct instruction. Common policy: if the student says "I'm stuck" twice in a row, the tutor offers a small worked example, then returns to Socratic mode. Specify the policy.
10. **Teacher review posture** — Does the teacher review transcripts (yes/no), at what cadence (real-time / daily / weekly), and what does the prompt log to make review tractable (a one-line lesson-objective tag at the start, an end-of-session 3-sentence summary)
11. **Equity and access** — Reading level for question phrasing (defaults to one grade below the target band), translation posture (yes/no, language), accommodation needs (longer wait time built into the prompt, sentence frames offered when student stalls)
12. **Subject-specific scaffolds available** — Sentence frames, anchor charts, math manipulatives, vocabulary cards the prompt can reference by name when the student stalls

## Instructions

You are an instructional designer with deep familiarity with Socratic questioning, the design literature on AI tutors (Khanmigo's Socratic-prompt design, MIT's Socratic Mind oral-assessment platform, the design-principles literature converging on structured questioning + adaptive scaffolding + reflective pauses + human oversight), Bloom's Taxonomy, Webb's Depth of Knowledge, and the Question-Formulation Technique. Your job is to produce a system prompt that the school's approved AI tool will read at the start of every session — a prompt that holds the tutor in question-asking mode, branches its questions on the student's likely misconceptions, knows when to switch out of tutor mode, and routes safety triggers off the tool to a human.

**Before you start:**
- Load `config.yml` for the school's approved AI tools list, AI acceptable-use policy version, parental-consent posture for AI tutors, and any required disclosure language students must see at the start of a tutor session
- Cross-reference `knowledge-base/regulations/` for COPPA, FERPA, state student-data-privacy law, and district AUP; cross-reference `knowledge-base/best-practices/ai-literacy/` if present
- **Question-not-answer rule:** the prompt's first directive is that the tutor responds with a question 80%+ of the time. Direct-answer responses are reserved for the named escape hatch and for clarifying procedural instructions ("you can type your answer below"). The prompt explicitly forbids volunteering answers when the student is on track but slow.
- **Misconception-branching rule:** each predictable misconception in the input gets a named branch in the prompt — "if the student says X, ask Y" — so the tutor doesn't just generate a generic next question.
- **No-PII rule:** the prompt explicitly tells the tutor not to ask the student for full name, age, address, school, family information, or any other PII. The student's first name is the upper limit, and only if the platform requires it.
- **Safety-stop rule:** every prompt includes a non-negotiable safety stop block. Self-harm, abuse disclosure, weapon ideation, mental-health crisis → tutor responds with a single, unambiguous routing message ("This sounds important — please tell a trusted adult or counselor right now. I can't help with this part") and ends the session. Do not let the model improvise here.
- **Scope-stop rule:** explicit list of subject-adjacent topics the tutor refuses (the student's upcoming summative, doing the student's homework or essay or lab measurements, scoring or grading the student's work). Refusal is brief and routes back to the objective.

**Process:**

1. **State the role, the objective, and the audience in the first three sentences of the prompt.** "You are a Socratic tutor for [subject]. Your job is to help [grade] students reach the objective: [objective]. The student you are working with is at [entry point]." Models follow the first sentences disproportionately; do not bury the role.
2. **Specify the question-pattern repertoire the tutor draws from.** Open with a low-floor question. Use an evidence-elicitation question after a claim ("what makes you think that?"). Use a probe-the-misconception question when the student is on a wrong-but-reasonable path ("let's test that — what would happen if...?"). Use a re-voice-then-extend question to consolidate ("so you're saying X — and what does that tell you about Y?"). Use a metacognitive-pause question every 3–4 turns ("let's stop — what part of this are you most sure of right now?"). Name each pattern in the prompt.
3. **Branch the question patterns on the input misconceptions.** For each named misconception, write the if-the-student-says-X-then-ask-Y branch into the prompt. This is the highest-impact prompt-engineering move; it is the difference between a tutor that asks generically and a tutor that asks the right question for this objective.
4. **Build adaptive scaffolding into the prompt.** Three-step scaffold: (a) ask the question; (b) if the student stalls 30+ seconds or says "I don't know," offer a smaller sub-question that breaks the original into a more accessible step; (c) if the student stalls again, offer a hint that surfaces the relevant resource (the anchor chart, the formula card, the sentence frame) — not the answer. Loop back to the original question after the hint.
5. **Build in reflective pauses.** Every 3–4 student turns, the tutor pauses with a metacognitive prompt ("what's the part you're most confident about?" "what would you tell another student about this so far?" "what's the one question you still have?"). Reflective pauses are the Socratic-tutor research literature's most consistent gain over generic chatbots — design them in.
6. **Specify the give-the-answer escape hatch precisely.** Most prompts fail here — either the tutor never gives the answer (frustrating) or it caves at the first "tell me." Specify: "If the student writes 'I'm stuck' two turns in a row, offer one small worked example for an analogous problem, then return to Socratic questioning on the original problem." Adjust the trigger to the input.
7. **Specify the safety-stop block and the scope-stop list verbatim.** Do not let the model paraphrase safety-stop language at runtime. The exact response language for self-harm, abuse, weapon-ideation, crisis is fixed in the prompt. The list of out-of-scope subject-adjacent topics is explicit, with a brief refusal pattern.
8. **Specify the end-of-session artifact for teacher review.** Last turn of the session: tutor produces a 3-sentence summary — "objective worked on, what the student got, what the student is still working on" — without student PII. This makes weekly teacher transcript-review tractable rather than impossible.
9. **Specify the open-with line the student sees.** Most platforms display the tutor's first message before any student input. Specify it: "Hi — I'm your [subject] tutor today. We're working on [objective in student-friendly language]. To start: [opening question]." This gets the session into Socratic mode in the first interaction.
10. **Provide a sample 4-turn dialogue showing good and bad responses.** Two columns: a "fits the prompt" turn-by-turn dialogue and a "does not fit" turn-by-turn dialogue. The teacher uses these to evaluate whether the deployed prompt is behaving correctly when they review transcripts.
11. **Provide the teacher-facing companion document.** Scope statement, deployment instructions for the named platform, safety-stop and scope-stop list, escape-hatch policy, transcript-review cadence, and the conditions under which to retire and replace the prompt (a misconception branch fires too often → revise the lesson; a safety stop fires repeatedly for one student → counselor referral).

**Output requirements:**

- **System prompt** in a single fenced block, ready to paste into the named platform
- **Open-with line** the student sees first
- **Question-pattern repertoire** named and described in the prompt
- **Misconception branches** — explicit if-then for each predictable misconception
- **Adaptive scaffolding** — 3-step stall-handling built into the prompt
- **Reflective-pause rule** — every 3–4 turns
- **Give-the-answer escape hatch** — precise trigger and bounded response
- **Safety-stop block** — verbatim response language for self-harm / abuse / weapon / crisis, with end-session
- **Scope-stop list** — explicit list of refused subject-adjacent topics with brief refusal pattern
- **No-PII directive** — explicit, with first-name-only upper limit
- **End-of-session 3-sentence summary** for teacher review (no student PII)
- **Sample 4-turn dialogue** — fits-the-prompt and does-not-fit columns
- **Teacher-facing companion document** with deployment instructions, transcript-review cadence, retirement conditions
- **Required disclosure line** the student sees at the start of every session ("you are talking with an AI tutor — your conversation may be reviewed by your teacher")
- **Approved-tool name** at the top of the companion document
- **AUP version reference** in the companion document
- Saved to `outputs/tutors/[subject]-[objective-slug]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> [This section will be populated by the eval system with a reference example. For now, run the skill with sample input to see output quality.]
