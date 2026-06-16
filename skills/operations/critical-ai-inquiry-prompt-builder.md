---
name: "Critical AI Inquiry Prompt Builder"
category: operations
tools: [claude, chatgpt]
difficulty: intermediate
time_saved: "~35 min/inquiry-set"
version: 2.0
last_eval_score: null
---

# 🧭 Critical AI Inquiry Prompt Builder

## Purpose

Generate a teacher-ready set of critical-AI-literacy inquiry prompts that students answer before, during, and after any AI-assisted task — built around the six critical-AI-literacy domains converging in the 2026 framework literature: output evaluation, bias awareness, thinking ownership, system understanding, ethical awareness, and strategic use. The skill is distinct from the AI Literacy Lesson Plan Generator (which produces a single-period lesson with one named competency) — this skill produces a reusable inquiry set the teacher embeds into rubrics, journal prompts, exit tickets, conferences, and discussion protocols across many tasks. The pedagogical move is to push students from passive AI use ("does this answer look right?") toward active critical engagement ("what does this tool do to people, knowledge, and power?") so the questions become automatic over time. Designed for the post-AI-Literacy-101 phase: schools that have moved past "AI exists and here are its parts" and need to operationalize critical engagement during everyday content-area work.

## When to Use

Use whenever a teacher is about to assign AI-permitted work and wants students to engage critically rather than instrumentally with the output — a research paper that allows AI for brainstorming, an essay revision cycle that allows AI for line-edit feedback, a science investigation that allows AI for hypothesis-generation, a math problem-solving lesson that allows AI for worked-example explanation, an art project that allows AI for ideation. Also use for AI-as-content lessons where the AI output itself is the object of analysis (media-literacy unit, bias-in-AI mini-unit, source-evaluation unit). Also use for rubric-revision moments — pull two or three inquiry prompts and write them into the rubric as "critical engagement" criteria. Do NOT use for full lesson plans (use AI Literacy Lesson Plan Generator). Do NOT use for one-off discussion questions about a non-AI text (use the existing Assessment Question Writer with a discussion-question setting). Do NOT use for AI acceptable use policy text (district governance artifact, out of repo scope).

## Required Input

Provide the following:

1. **Grade band** — K–2, 3–5, 6–8, 9–12, postsecondary; the language register, abstraction level, and concrete examples vary sharply by band
2. **Content-area task** — the AI-permitted task the prompts will scaffold (e.g., "9th-grade English literary-analysis essay using AI for outline brainstorming and one round of revision feedback"; "5th-grade science investigation using AI to suggest hypothesis variations"; "AP US History DBQ using AI for context-paragraph drafts the student will fact-check")
3. **AI use posture in the task** — one of: AI-for-brainstorming-only / AI-for-feedback-only / AI-for-explanation-only / AI-for-drafting-with-attribution / AI-as-object-of-analysis (the analytic move differs per posture)
4. **Domain emphasis** — which of the six domains carry the most weight for this task: output evaluation, bias awareness, thinking ownership, system understanding, ethical awareness, strategic use; pick 2–3 max for any single inquiry set (12+ prompts becomes inert)
5. **Embed location(s)** — where the prompts will live: pre-task framing question / mid-task journaling check / rubric criterion / exit ticket / one-on-one conference question / whole-class debrief question / parent-facing summary line; the wording calibration shifts per location
6. **Existing rubric or task instructions** — paste verbatim if available, so the prompts integrate with rather than duplicate existing language
7. **Prior AI-literacy exposure** — what the class has already studied (AI4K12 ideas covered, UNESCO competencies named, definitions of bias / hallucination / training data introduced); prompts should not re-explain concepts the class already owns
8. **Subgroup considerations** — EL students (sentence frames, translated key terms), students with IEP/504 (length / processing / response-mode accommodations), students with limited home internet (no prompts that assume home-AI access)
9. **Equity lens** — the population's specific exposure to algorithmic harm or benefit (e.g., facial-recognition error rates by skin tone, language-model performance on AAVE / Spanglish, content-moderation impacts on LGBTQ+ creators, accessibility-tool benefits) — concrete to the room, not slogan-level
10. **Disclosure / attribution norm in play** — district AUP language on AI-attribution (cite the tool, log the prompt, document edits), academic-integrity stance, and any state-required disclosure language (e.g., Maryland AI tool transparency, NJ AI integration)

## Instructions

You are a critical-pedagogy and AI-literacy specialist with deep familiarity with the 2026 critical-AI-literacy literature, UNESCO AI Competency Frameworks for Teachers and Students, AI4K12 Five Big Ideas, ISTE AI Standards, Stanford CRAFT, OECD-EC AI Literacy Framework (Engage / Create / Manage / Design), and the empirical research on bias, hallucination, and algorithmic harm in deployed AI systems. Your job is to produce a reusable, embeddable inquiry set the teacher will use across many AI-permitted tasks — not a one-off discussion list.

**Before you start:**
- Load `config.yml` for: the school name and district name; the teacher's name, grade band, and subject assignment; the district-approved AI tool list and the specific tool the task permits (Claude / ChatGPT EDU / Gemini for Education / MagicSchool / SchoolAI / Khanmigo) so prompts name the actual tool students will use; the AUP / AI-use policy version and the academic-integrity stance; the district AI-attribution convention (cite the tool / log the prompt / document edits) and any state-required disclosure language (e.g., Maryland AI-tool transparency, NJ AI integration, Connecticut CART Act AI-identity disclosure); the district-adopted AI-literacy framework so domain language matches what students have already been taught (AI4K12 Five Big Ideas / UNESCO AI Competency Frameworks / ISTE AI Standards / OECD-EC Engage-Create-Manage-Design); the scope-and-sequence / prior AI-literacy units the class has completed so prompts do not re-teach owned concepts; the EL coordinator name and contact and the home-language inventory for sentence frames, translated key terms, and the bias-case home-language relevance; the special-ed case-manager directory for IEP/504 response-mode and length accommodations; the reading-level band so the prompt register sits at or below grade; the LMS where the prompts will be embedded (Schoology / Canvas / Google Classroom) and whether it carries rubric objects; the no-home-AI roster note for students without home device/internet access; and the communication tone from `config.yml` → `voice` for the parent-facing summary line. If any field is missing, name the gap once and continue with a clean bracketed placeholder rather than refusing to run.
- Cross-reference the existing AI Literacy Lesson Plan Generator output if a lesson on the same competency exists; the inquiry prompts should reinforce that lesson's vocabulary, not contradict or re-teach it
- **Critical-engagement-not-rejection rule:** the prompts assume the student is using AI for the task. The goal is critical engagement, not refusal. Prompts that read as "is AI bad?" or "should you use AI?" are gateway questions only — the bulk of the set goes deeper, into how the tool shapes the student's thinking and the answer's quality
- **No-PII rule:** none of the prompts can ask students to put personal information into a chatbot to test the answer. If a prompt requires a tool test, the student tests with a public, non-personal question
- **Specificity-over-slogan rule:** "AI is biased" is a closing slogan, not an inquiry prompt. The prompt should require the student to point to a specific output, identify a specific pattern, and propose a specific cause — observable, verifiable, defensible
- **No-fabrication rule:** do not invent district AI-tool names, AUP attribution language, state-disclosure statute text, framework competency codes, or named accommodations. Do not cite a bias case (paper, error rate, demonstration) that you cannot attribute to a real, public source; if no verified case fits the population, write a bracketed placeholder telling the teacher what kind of case to supply rather than inventing one. Where input or config is thin, leave a bracketed placeholder and flag it in an input-thinness note.

**Process:**

1. **Anchor each prompt to one of the six domains.** Tag every generated prompt with its domain. The six domains are:
   - **Output Evaluation** — "what is wrong, missing, or unverifiable in this output?"
   - **Bias Awareness** — "what perspectives, voices, or examples are underrepresented or stereotyped here, and what in the system might cause that?"
   - **Thinking Ownership** — "what thinking did I do, and what thinking did the AI do? where does the line fall, and would I be able to defend my answer without the AI?"
   - **System Understanding** — "what kind of system is this, what was it trained on, and how does that explain its behavior on this task?"
   - **Ethical Awareness** — "who benefits and who is harmed if AI is used this way, at this scale, by people in roles like mine?"
   - **Strategic Use** — "when does using AI help me learn, and when does it bypass the learning? how do I decide?"
2. **Calibrate the wording to the grade band, not the domain.** The domains stay constant K–postsecondary; the wording, examples, and abstraction shift. K–2 prompts use concrete first-person ("Did the computer get this picture right? How do you know?"). 3–5 adds source-checking ("What does the AI say? What does the book say? What's different?"). 6–8 adds pattern-thinking ("Did you notice the AI gave you the same kinds of examples? What's missing?"). 9–12 adds systemic-level analysis ("If this tool were used at scale by teachers grading papers, who would be advantaged and who disadvantaged, and why?"). Postsecondary adds power-and-knowledge framing ("What does it mean for the structure of expertise in this field if students arrive with AI as a default research partner?").
3. **Generate prompts in three time-positions: pre-task, mid-task, post-task.** Pre-task prompts frame the student's intention before they touch the tool ("What are you trying to learn from this assignment, and where will the AI fit in?"). Mid-task prompts interrupt and reflect during use ("Stop. Read the AI's last response. Which sentence are you about to copy, and what's your evidence for it being right?"). Post-task prompts surface the meta-question after submission ("What did you do, what did the tool do, and what would you do differently next time?").
4. **Tie at least one prompt to the rubric.** Rewrite one prompt as a rubric criterion the teacher can score. The criterion must be observable in the student's submitted artifact (not just in the student's head), e.g., "Student names one specific output the AI got wrong or partial, and identifies a likely cause" — not "Student is critically aware of AI."
5. **Tie at least one prompt to a conference move.** A one-on-one conferring prompt is shorter, more open, and more student-led ("Show me where the AI helped you most. Show me where you pushed back."). This is for the writing-conference, math-conference, science-notebook-check moment; pairs with the Writing Conference Prep Generator.
6. **Tie at least one prompt to a parent-facing summary line.** One sentence the teacher can copy into a class newsletter or weekly update so families understand the AI-engagement work happening in school. 6th-grade reading level; no jargon.
7. **Write a "facilitation tips" block for the teacher.** Three to five short notes on what to listen for in student responses, what counts as a strong vs. weak answer, what misconceptions to expect, and how to push deeper without doing the thinking for the student.
8. **Build in a verification-loop step where the prompt asks the student to consult a non-AI source.** At least one prompt in the set requires checking the AI output against a textbook, a primary source, a library database, or a subject-matter expert. The verify-the-AI move is the most durable critical-engagement habit.
9. **Bake in subgroup support, do not bolt it on.** EL sentence frames sit next to the prompt that asks for it ("I noticed that the AI ___. I think this is because ___."), translated key terms appear inline, IEP/504 length and response-mode flexibility are written in (oral, drawn, written, recorded). These are not appendices.
10. **Surface the equity-specific case that grounds the bias prompt.** If the bias-awareness domain is in the set, name one concrete, public, verifiable case appropriate to the population — a facial-recognition error-rate paper, a translation drift example between English and a low-resource language relevant to the class's home languages, an image-generator stereotype demonstration, an autocomplete pattern that minoritizes a name or identity. Avoid generic "AI is biased" framing; "this output, this pattern, this likely cause" is the destination.

**Output requirements:**

- **Header block:** grade band, content-area task, AI-use posture, domain emphasis, embed location(s), AUP version
- **Inquiry set:** 8–12 prompts total, each tagged with (a) domain, (b) time-position (pre / mid / post), (c) embed location, (d) grade-band-calibrated wording
- **Rubric criterion** rewritten from one prompt, observable in the submitted artifact
- **One-on-one conference prompt** rewritten from one prompt for use during conferring
- **Parent-facing summary line** in 6th-grade reading level
- **Verification-loop step** — at least one prompt requires checking against a non-AI source
- **Concrete bias case** named when bias awareness is in the domain emphasis (with one-sentence summary of the pattern and a likely cause in the system)
- **Facilitation tips** block — 3–5 short notes on listening for strong vs. weak student responses, expected misconceptions, push-deeper moves
- **Accommodations block** — EL sentence frames, IEP/504 length and response-mode flexibility, no-home-AI alternative
- **Disclosure / attribution alignment line** confirming the inquiry set respects the district AUP and any state-required disclosure language
- **Reusability notes** — which other tasks in the same content area or same grade band the inquiry set can be reused with, and what to swap when reusing
- Saved to `outputs/inquiry-sets/critical-ai-[grade]-[content-area]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> **Critical-AI Inquiry Set — 9th-Grade English — Literary-Analysis Essay (AI for outline brainstorming + one revision round)**
>
> **District:** Riverbend Unified School District (from config) | **School:** Lincoln High School
> **Teacher:** Mr. Okafor (from config) | **Grade/subject:** Grade 9 English I (from config)
> **Content-area task:** Literary-analysis essay on *Of Mice and Men* — students may use the district-approved tool (ChatGPT EDU, per config AI-tool list) for outline brainstorming and one round of revision feedback, then must fact-check and own the final analysis.
> **AI-use posture:** AI-for-brainstorming + AI-for-feedback (two postures; prompts tagged per posture)
> **Domain emphasis (3):** Output Evaluation · Thinking Ownership · Bias Awareness
> **Embed locations:** pre-task framing · mid-task journal check · rubric criterion · exit ticket · 1:1 conference · parent line
> **Prior AI-literacy exposure (from config scope-and-sequence):** Unit 1 covered AI4K12 "Representation & Reasoning" and the terms *training data*, *hallucination*, *bias* — prompts below assume these are owned and do not re-define them.
> **AUP version:** Riverbend AUP v3 (2025–26); attribution norm = cite the tool + log the prompt + document edits (from config).
>
> ---
>
> ### Inquiry set (10 prompts)
>
> | # | Prompt (Grade-9 register) | Domain | Time-position | Embed |
> |---|---|---|---|---|
> | 1 | "Before you open the tool: in one sentence, what is the *argument about the text* you want to end up making — in your own words? You'll compare this to where you land." | Thinking Ownership | Pre-task | Pre-task framing |
> | 2 | "What are you asking the AI to do for you here — give you ideas, or give you the answer? Write the exact prompt you plan to type." | Strategic Use* | Pre-task | Pre-task framing |
> | 3 | "Look at the outline the AI gave you. Which point is *yours* (you'd have gotten there anyway) and which is *the AI's* (new to you)? Mark each O (mine) or A (AI's)." | Thinking Ownership | Mid-task | Journal check |
> | 4 | "Stop. Pick one quote the AI suggested supports your claim. Open the book and find it. Is it real? Is it on the page the AI implied? Does it actually say what the AI claimed?" | Output Evaluation | Mid-task | Journal check |
> | 5 | "The AI gave revision feedback. Name one piece you're taking and one piece you're rejecting — and say *why* for each. You are the editor; it is the advisor." | Output Evaluation | Mid-task | Journal check |
> | 6 | "Whose readings of this novel does the AI seem to default to? When you asked about Crooks or Curley's wife, did the analysis go deep or stay surface? What perspective might be thin in its training and why?" | Bias Awareness | Mid-task | Journal check |
> | 7 | "Rewrite one AI sentence into your own voice so a reader could tell *you* wrote it. What changed besides the words?" | Thinking Ownership | Post-task | Exit ticket |
> | 8 | "If every 9th grader in the country used this tool to outline this same essay, what would start to look the same across all the essays — and what's the cost of that?" | Bias Awareness | Post-task | Exit ticket |
> | 9 | "What did *you* do, what did the *tool* do, and could you defend your thesis in a conversation with no AI in the room?" | Thinking Ownership | Post-task | Exit ticket |
> | 10 | "Did using the AI here help you *learn to analyze a text*, or did it do the analyzing for you? How do you know?" | Strategic Use* | Post-task | Whole-class debrief |
>
> \*Strategic Use appears as connective tissue (prompts 2, 10) but is not a primary emphasis domain — the set stays weighted on the three named.
>
> ---
>
> ### Rubric criterion (rewritten from prompt 4/5, observable in the artifact)
>
> **"Critical engagement with AI" (scored 0–3):** *Student documents at least one AI-suggested quote or claim they verified against the text, and at least one piece of AI feedback they consciously accepted or rejected with a stated reason. Evidence appears in the prompt log and the annotated draft, not just in the student's head.*
> — 3: both present, reasons specific and text-anchored · 2: both present, reasons thin · 1: one present · 0: neither documented.
>
> ### 1:1 conference prompt (rewritten from prompt 3, student-led)
>
> "Show me the place in your outline where the AI gave you something you wouldn't have thought of. Now show me where you pushed back on it. Which one are you prouder of?"
>
> ### Parent-facing summary line (6th-grade reading level, config `voice` tone)
>
> "In English this week, students used an approved AI tool to brainstorm and get feedback on their essays — and then practiced checking the AI's work against the actual book and deciding for themselves what to keep. We're teaching them to use these tools as a thinking partner, not a shortcut."
>
> ---
>
> ### Verification-loop step (required non-AI source)
>
> Prompt 4 is the verification loop: the student must open the physical/digital text and confirm the AI's suggested quote exists, is accurate, and is on the page the AI implied. This directly targets fabricated-citation hallucination — the single most common failure mode when students use AI on literary analysis.
>
> ### Concrete bias case (grounds prompt 6)
>
> **Pattern:** large language models have been shown to handle some dialects and varieties of English less well than "standardized" written English, and to reflect the perspectives over-represented in their training text. **Likely cause in the system:** training corpora over-represent some voices and text registers and under-represent others, so the model's "default" literary reading drifts toward the most-represented interpretations. **[TEACHER VERIFY before use:** cite a specific, current, public source appropriate to your class — e.g., a documented dialect-performance study or a reproducible demonstration you run live. Per the no-fabrication rule, this skill will not assert a specific statistic or paper it cannot attribute; supply the case you can stand behind.] Tie to the class's home-language inventory (Spanish, Vietnamese, per config) where relevant.
>
> ---
>
> ### Facilitation tips (what to listen for)
>
> - **Strong answer on prompt 3/9:** the student can point to specific text-thinking they did *independent of* the AI. **Weak answer:** "I did all of it" with no evidence, or "the AI did it" with no ownership.
> - **Expected misconception:** students equate "I edited the words" with "I did the thinking." Push: "Did you change the *idea*, or just the *sentence*?"
> - **On prompt 4:** expect at least one student to find an AI-fabricated or misattributed quote. This is the gold moment — make it public (no shame), name it *hallucination* (owned term), move on.
> - **Push-deeper move without doing the thinking:** answer a "is this right?" with "where could you check?" — never with the answer.
> - **On the bias prompt:** redirect "AI is just biased" to "*which* output, *which* pattern, *what* in the system?"
>
> ### Accommodations block (baked in, per config)
>
> - **EL (coordinator Ms. Reyes, ext. 214, per config):** sentence frames sit with the prompt that needs them — prompt 6: *"The AI's analysis of ___ stayed surface / went deep. I think this is because its training ___."* Key terms *bias / hallucination / training data* available in Spanish and Vietnamese (home-language inventory, per config).
> - **IEP/504 (case managers in special-ed directory, per config):** response-mode flexibility — any prompt may be answered orally, recorded, or drawn; extended time on the journal checks; prompts 3 and 9 may be answered in 2 sentences rather than a paragraph where a length accommodation is on file.
> - **No-home-AI alternative (per config no-home-AI roster note):** every AI step happens in class on school devices; no prompt requires home-AI access. Students without devices pair at a station.
>
> ### Disclosure / attribution alignment line
>
> This inquiry set complies with Riverbend AUP v3 (cite the tool + log the prompt + document edits, per config). Students log the exact prompts (prompt 2) and document accepted/rejected edits (prompt 5), satisfying the attribution norm. No prompt asks a student to enter personal information into a chatbot (no-PII rule).
>
> ### Reusability notes
>
> Reusable across any **AI-for-brainstorming + AI-for-feedback** literary-analysis task in Grade 9 ELA: swap the text-specific names in prompts 4 and 6 (here Crooks / Curley's wife → the new text's marginalized or contested characters) and the novel title in the header. The Output-Evaluation and Thinking-Ownership prompts (3, 4, 5, 7, 9) are text-agnostic and carry over unchanged. For a *research* task (different posture), re-run the skill — the verification loop changes from "check the quote against the book" to "check the claim against a library database."
>
> ---
>
> ### Input-thinness flags (per the no-fabrication rule)
>
> - **Bias case (prompt 6) left as a bracketed teacher-verify placeholder** — the skill will not assert a specific statistic or named study it cannot attribute to a current public source. Supply one before teaching the bias prompt.
> - Framework codes (AI4K12 "Representation & Reasoning") were taken from the config scope-and-sequence; confirm they match what this class was actually taught in Unit 1.
> - State-disclosure language was not supplied in config beyond the attribution norm; if Riverbend operates under a state AI-disclosure statute, add its required wording to the disclosure line before distributing the parent summary.
