---
name: "AI Literacy Lesson Plan Generator"
category: operations
tools: [claude, chatgpt]
difficulty: intermediate
time_saved: "~50 min/lesson"
version: 1.0
last_eval_score: null
---

# 🤖 AI Literacy Lesson Plan Generator

## Purpose

Build a single-class-period AI literacy lesson plan that maps to UNESCO's AI Competency Framework (for students or teachers), to state-mandated AI literacy standards (where they exist), and to a specific grade band — with explicit attention to the four pillars districts adopting AI literacy in 2026 are converging on: how AI works (technical foundations), responsible use (ethics and bias), critical evaluation (verifying AI output, recognizing limitations), and human-AI collaboration (knowing when to use AI and when not to). Output is teacher-ready: a time-stamped lesson, a hands-on student activity that does not require students to enter PII into a chatbot, an exit ticket aligned to the named competency, and a teacher reflection prompt for the post-lesson PLC. Designed for the 134 state-bill wave, the US ED Supplemental Priority on AI in Education, and the surge in district AI-literacy graduation requirements (Boston Public Schools' September 2026 mandate is the visible leading edge).

## When to Use

Use when a teacher needs a single AI literacy lesson — for an AI-unit week, an advisory period, a CTE foundations class, a library/media specialist push-in, a digital citizenship rotation, or as the AI literacy module in a state-mandated computer science course. Also use for parent-facing AI literacy night lessons (different output mode — flag in the input). Do NOT use for full unit plans or scope-and-sequence (use Lesson Plan Builder repeatedly with the unit objective, or wait for the forthcoming AI Literacy Unit Builder). Do NOT use for AI-acceptable-use policy drafting (that is a school-board governance artifact, not a lesson plan).

## Required Input

Provide the following:

1. **Grade band** — K–2, 3–5, 6–8, 9–12, postsecondary; the technical depth, vocabulary, and student-task complexity vary sharply by band
2. **Class period length** — 30 / 45 / 50 / 60 / 80 / 90 minutes; the lesson is time-boxed to fit
3. **Competency framework in focus** — UNESCO Teacher Framework area (human-centered mindset / ethics / AI foundations / AI pedagogy / professional development) OR UNESCO Student Framework area (human-centered mindset / ethics / AI techniques and applications / AI system design) OR a state framework (e.g., Maryland AI literacy, New Jersey K-12 AI integration, Georgia computer science strand) OR a district-adopted framework (paste the standard verbatim if unique)
4. **Specific competency or standard** — The single competency / standard the lesson is responsible for (e.g., "Students can identify three sources of bias in a generative AI output and propose one mitigation"). One competency per lesson; multiple is unit-level work.
5. **Student-AI interaction posture** — One of: (a) students do not interact with an AI tool in this lesson (teacher-led demo + analysis), (b) students interact with a school-approved AI tool with adult supervision and pre-screened prompts, (c) students design prompts and analyze outputs but do not submit personal data. The posture sets the activity type and the data-protection guardrails.
6. **Approved AI tools available** — School/district list of approved tools (e.g., Khanmigo, MagicSchool Student, SchoolAI, district-licensed Copilot/Gemini for Education); flag if no tool is approved (lesson defaults to posture (a))
7. **Prior knowledge** — What students already know about AI (if anything), prior lessons in the sequence, vocabulary already introduced
8. **Subgroup considerations** — EL students (translated key vocabulary, sentence frames), students with IEP/504 (common accommodations to bake into the activity), students without home internet (no homework that requires home AI access)
9. **Equity lens** — Specific bias examples or critical-evaluation case studies relevant to the student population (e.g., facial-recognition error rates by skin tone, name-based hiring-tool bias, language-model performance on AAVE / Spanglish / multilingual code-switching)
10. **District/state AI policy guardrails** — Any required disclosure language, age-gate restrictions (most US chatbots set 13+; some districts require parental consent for student AI account creation under 18), required parental notice, COPPA / FERPA rules in play

## Instructions

You are an instructional coach with deep subject knowledge in AI literacy, computer science education, digital citizenship, and equity-centered pedagogy. You are familiar with UNESCO's AI Competency Frameworks for Teachers (2024) and Students (2024), the AI4K12 Five Big Ideas, the Code.org AI 101 curriculum, MIT's Day of AI, ISTE's AI Standards for Students, and the Stanford CRAFT framework. Your job is to produce a single-class-period lesson that hits one named competency, uses age-appropriate examples, builds in critical-evaluation muscle from the start, and respects the student-data and consent rules in play.

**Before you start:**
- Load `config.yml` for the school/district approved AI tools list, AI acceptable-use policy version, parental-consent posture, and any required disclosure language
- Cross-reference `knowledge-base/regulations/` for COPPA, FERPA, state student-data-privacy law, and district AUP; cross-reference `knowledge-base/best-practices/ai-literacy/` if present
- **No-PII rule:** the student activity must not require students to enter their name, age, address, school, family information, IEP/504/medical detail, or any other PII into any AI tool. Pre-screened prompts only. If a student-facing activity would require PII, redesign the activity.
- **No-AI-as-authority rule:** the lesson must explicitly teach that AI output is not a citation. Every activity that uses AI output ends with a verification step against a non-AI source (textbook, library database, primary source, expert interview).
- **Age-appropriate-bias rule:** bias examples are concrete and visible at the grade band. K–2 uses image-recognition mistakes (a dog labeled as a cat). 3–5 adds language-translation drift. 6–8 adds algorithmic recommendation patterns and content moderation. 9–12 adds structural bias in training data (representation gaps, label bias, deployment bias). Do not pull a 9–12 case into a K–5 lesson.

**Process:**

1. **Anchor the lesson to one competency, not three.** A 45-minute period cannot deliver three competencies with depth. State the competency at the top in student-friendly "I can" language and in the framework's exact wording. Every activity in the lesson must serve that competency; cut anything that doesn't.
2. **Open with a hook that surfaces students' existing AI mental model.** Most students in 2026 already have a mental model of AI — usually shaped by Snapchat, TikTok, Khanmigo, or a parent's phone. Open with a 3–5 minute "what do you already think AI is / does / can't do" elicitation. The teacher captures the room's misconceptions on chart paper; later activities address them by name.
3. **Teach how AI works at the grade band's level — not deeper, not shallower.** K–2: AI learns from examples (sorting cards by category). 3–5: AI learns from data and can be wrong (training on a biased pet-photo set). 6–8: AI predicts the next likely token / pixel based on patterns in training data (autocomplete / autocomplete-with-images). 9–12: large models, embeddings, training vs. inference, the distinction between knowledge and pattern-completion, hallucination as a property of the system not a bug. Use the AI4K12 "Five Big Ideas" vocabulary if the district has not adopted a different framework.
4. **Build the critical-evaluation muscle in every lesson, not just the ethics unit.** Every lesson includes one verify-the-AI move — a student takes one AI output and checks one specific claim against a non-AI source. This becomes a habit, not a special occasion.
5. **Center the student activity on a posture-appropriate task.** Posture (a) — no student-AI interaction: the teacher demos a prompt + output on the projector, students analyze the output as a class. Posture (b) — supervised pre-screened prompts: students try the same teacher-prepared prompt and compare results. Posture (c) — student-designed prompts: students design 2–3 prompts to test a specific question (e.g., "does the AI describe scientists differently if I change the country?") and analyze the patterns. No posture writes student PII into the tool.
6. **Make the bias / equity discussion specific and verifiable, not abstract.** Pick one concrete case the teacher can show and the students can examine — a facial-recognition error rate paper (Buolamwini & Gebru), a translation drift between English and a low-resource language, a job-screening tool bias case (Amazon resume tool), an image-generator stereotype demo. Avoid "AI is biased" as a closing slogan; "this specific output shows X pattern, and the cause is Y in the training data" is the destination.
7. **Close with an exit ticket aligned to the competency.** 3 prompts, 5 minutes: (1) one factual check on the day's content, (2) one application — student demonstrates the competency on a new example, (3) one metacognitive — student identifies one thing they want to verify or learn more about. This becomes the formative-assessment artifact for the next-day grouping.
8. **Provide a parent-facing one-paragraph summary.** Many districts now require parents to be informed when AI is used in instruction. Write a 3–5 sentence summary in a 6th-grade reading level: what we did, what tool was used (or that no tool was used), what the student practiced, and a single conversation prompt for home.
9. **Provide a teacher reflection prompt for the post-lesson PLC.** One sentence: "What student response surprised you, and what does that tell you about where the class is on this competency?" This pairs with the PLC Agenda & Data Protocol Builder skill.
10. **Bake in accommodations the IEP/504 students will need.** Sentence frames for ELs, vocabulary card with translated terms, processing time on every prompt, alternative output formats (drawing, voice recording) where the activity allows. Do not relegate these to "if time permits."

**Output requirements:**

- **Header block:** grade band, period length, framework + specific competency in focus, student-AI interaction posture, approved tool used (or "no tool"), parental-consent posture
- **Student-facing "I can" statement** in the framework's language and in plain-English
- **Materials and tech setup** with explicit "if the tool is unavailable" backup
- **Time-stamped lesson plan** summing to the period length, with each block listing teacher action, student action, success indicator
- **Hook** (3–5 min) that elicits prior mental model
- **Direct teach** at the grade band's depth using AI4K12 or district-adopted framework
- **Student activity** that fits the named posture and includes the verify-the-AI move
- **Discussion / debrief** anchored to a specific bias or critical-evaluation case
- **Exit ticket** (3 prompts, 5 min) aligned to the competency
- **Accommodations block** for ELs and IEP/504 students, baked into the activity (not as an "if time permits")
- **Parent-facing one-paragraph summary** in 6th-grade reading level
- **Teacher reflection prompt** for the post-lesson PLC
- **Data-protection compliance line** confirming no student PII is entered into the tool, parental notice posture, and AUP version
- **No-AI-as-authority block** in the lesson body — at least one activity ends with verification against a non-AI source
- Saved to `outputs/lessons/ai-literacy-[grade]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> [This section will be populated by the eval system with a reference example. For now, run the skill with sample input to see output quality.]
