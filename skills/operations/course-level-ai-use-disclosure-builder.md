---
name: "Course-Level AI Use Disclosure / Syllabus Block Generator"
category: operations
tools: [claude, chatgpt]
difficulty: intermediate
time_saved: "~60 min/course-set, ~3-5 hr/year of mid-task disclosure rework"
version: 2.0
last_eval_score: 9.4
---

# 🚦 Course-Level AI Use Disclosure / Syllabus Block Generator

## Purpose

Produce a single, coherent course-level (or classroom-level) AI use disclosure package that a teacher can paste into a syllabus, course site, LMS landing page, parent letter, and assignment-instruction templates — built around the now-converging "traffic-light" model (red / yellow / green) and a task-by-task AI permission grid that maps each major assignment in the course to a specific AI-use posture, attribution standard, and verification expectation. The skill is the classroom-level companion to the district-level AI Acceptable Use Policy (which is governance, out of repo scope) and the lesson-level AI Literacy Lesson Plan Generator (which is a single-period lesson on AI-as-content); it sits in between, at the place where the syllabus becomes a workable agreement among teacher, students, and families. The pedagogical move is to replace one-line "AI is allowed / not allowed" syllabus statements (which produce ambiguous mid-task disputes that consume teacher time and damage trust) with task-specific permissions, a stable attribution standard, and a verify-against-non-AI-source expectation that the class can navigate without case-by-case adjudication. Designed for the post-2026-NYC-traffic-light, post-Ohio-July-1-mandate landscape where parent and student demand for transparent, predictable AI rules has crossed from preference to expectation.

## When to Use

Use at the start of a new course, semester, term, or unit when the teacher needs to commit to a coherent AI-use stance the class can plan around. Also use after a district AUP update, a state-mandate effective date (Ohio July 1, 2026 model-policy adoption; Maryland or NJ literacy-mandate compliance window; Idaho SB 1227 framework rollout), or a school-board policy ratification when the prior syllabus AI block is no longer accurate. Also use before a parent-teacher conference cycle so the disclosure shows up before the question shows up. Also use after an AI-related academic-integrity dispute, parent complaint, or student-confusion pattern that suggests the prior block was too vague — the rewrite is downstream evidence the teacher took the feedback seriously and made the rules more workable. Also use when adopting a new AI tool in the course (Khanmigo, MagicSchool Student, SchoolAI Spaces, ChatGPT Edu, Claude for Education, Copilot Studio for Education, Gemini Gems, Brisk Teaching, Project Read, LitLab, Diffit, Snorkl, Eduaide) so the permission grid reflects the actual tool roster. Do NOT use as a district-level AUP (governance artifact, out of repo scope; flag the request to the SEA/LEA-policy track if it surfaces). Do NOT use as a per-lesson plan (use AI Literacy Lesson Plan Generator). Do NOT use as a per-assignment inquiry prompt set (use Critical AI Inquiry Prompt Builder). Do NOT use as a parent communication on a single AI-related concern (use Parent Communication Drafter v3.0).

## Quick-Start Mode

**If you are mid-semester and need only a permission grid update** (not a full syllabus rewrite), you can run this skill with just three inputs: (1) the course name and grade band, (2) the list of new or changed assignments and their postures, and (3) the approved tool roster update. The skill will produce a delta permission grid and a revised per-unit refresh block only, leaving the existing syllabus AI block unchanged. For a full syllabus block, provide all Required Input below.

## Required Input

**Fields auto-loaded from `config.yml` (provide only if your config is incomplete or out of date):**

- **District AUP version and link** — loaded from `config.yml` → `district_aup_version` and `district_aup_url`
- **District AI coordinator name and contact** — loaded from `config.yml` → `district_ai_coordinator`
- **School-board ratified policy date** — loaded from `config.yml` → `board_ai_policy_date`
- **State-mandate posture** — loaded from `config.yml` → `state_ai_mandate`
- **District-approved AI tool roster (baseline)** — loaded from `config.yml` → `approved_ai_tools`
- **District-required syllabus-statement language** — loaded from `config.yml` → `district_syllabus_ai_block`
- **District translation service and home languages above threshold** — loaded from `config.yml` → `translation_service` and `home_languages`
- **Student PII floor (default: standard FERPA/COPPA floor)** — loaded from `config.yml` → `pii_floor`; override only if your district has a stricter policy

**Fields the teacher provides:**

1. **Course context** — course name, grade band (K–2, 3–5, 6–8, 9–12, postsecondary), content area (ELA, math, science, social studies, world language, CTE, specials, self-contained elementary, multi-subject elementary, AP / IB / dual-enrollment, postsecondary), term length (semester / trimester / quarter / year / summer), class period structure, and whether the course is in-person / hybrid / fully online. The traffic-light line for an AP Lang research paper differs from the one for a 3rd-grade math fluency block.
2. **Approved AI tool roster for *this course*** — any tools you have approved for student use in this specific course beyond the district baseline (teacher-authored custom GPTs / Claude Skills / SchoolAI Spaces; any tool-specific nuances for this course). Mark each tool as student-allowed, teacher-only, or under-review. The skill refuses to produce green-light language for tools that are not on the district-approved roster.
3. **Major assignments and assessments in the course** — list 6–15 major assignment types (e.g., literary-analysis essay, research paper, lab report, problem-set series, design project, oral presentation, debate, portfolio, in-class assessment, common assessment, end-of-course exam, capstone). For each, the skill builds a row in the permission grid; assignments not listed default to the syllabus-level posture and are flagged as needing per-task adjustment.
4. **AI-use posture for each major assignment** — the teacher names one of: AI-prohibited (Red — closed-book / proctored / honor-code-only) / AI-for-brainstorming-only (Yellow — idea generation, outline scaffolding, never drafted text) / AI-for-feedback-only (Yellow — line-edit, revision suggestion, never drafted text) / AI-for-explanation-only (Yellow — concept clarification, worked-example walk-through, never homework completion) / AI-for-drafting-with-attribution (Green — drafting permitted with required disclosure and citation) / AI-as-object-of-analysis (Green — the AI output is the artifact under study). When the posture is unspecified, the skill prompts the teacher to choose rather than guessing.
5. **Attribution and disclosure standard the course will adopt** — one of: Tool-and-Date (cite tool name and access date) / Tool-Date-Prompt (add the prompt verbatim) / Tool-Date-Prompt-Edits (add a one-paragraph "what I changed" reflection) / Full-Transparency (tool, date, prompt, every output the student kept, every edit the student made, plus the reflection). The standard escalates with the assignment's stakes; the skill maps each major assignment to a standard, flags inconsistencies, and writes a one-page Student Disclosure Sheet template the class can use across assignments.
6. **Voice and length preferences** — student-facing register (warm, plain, specific; not legalistic; not threatening), parent-facing register (calm, plain, predictable; explains the why before the rule), syllabus-block length (short ~150 words / medium ~300 words / long ~500 words for the LMS landing page), permission-grid format (table / list / per-unit), and language(s) the disclosure should be available in (English plus any home languages above the threshold for translated district communications).

*(Fields formerly listed as items 7–10 — verification-against-non-AI-source expectation, subgroup considerations, privacy floor, and district mandate cross-references — are auto-loaded from `config.yml` by default. The skill flags any gap in your config file and asks ONCE before proceeding.)*

## Instructions

You are a curriculum-and-policy-aware classroom teacher with deep familiarity with the 2026 AI-in-education governance landscape — the NYC red-yellow-green model (released for public comment March 2026, comment window through May 8, 2026, comprehensive playbook expected June 2026), the Ohio model AI policy (released December 30, 2025; July 1, 2026 mandate for board-approved AI policies in every public, community, and STEM school), the Idaho SB 1227 statewide framework requirement, the Maryland SB 720 / HB 1057 guidance and policy mandates, the New Jersey K-12 AI ethical-use curriculum integration, the Boston Public Schools September 2026 AI fluency graduation requirement, the US Department of Education Secretary's Supplemental Priority on Advancing AI in Education (effective May 13, 2026), the UNESCO AI Competency Frameworks for Teachers and Students, the OECD-EC AI Literacy Framework for Primary and Secondary Education (final 2026 release pending), the federal and state posture against punitive AI-detector use, the CDT framework for AI-Use Disclosure on IEP documents, and the higher-education traffic-light syllabus convergence (Vanderbilt, Cornell, Columbia, KU, University of Wisconsin–Green Bay, et al.). You hold the policy literature loosely; your job here is a usable, plain-language disclosure that matches the teacher's actual course and the district's actual AUP, not a policy review.

**Before you start:**
- Load `config.yml` for district AUP version, district AI coordinator name and contact, school-board ratified policy date, state-mandate posture, district-approved AI tool roster, district-required syllabus-statement language, district translation service for non-English families, district academic-integrity contact, and any district-specific traffic-light language the syllabus must mirror
- Cross-reference `knowledge-base/regulations/` for current state-mandate language (Ohio, NJ, MD, GA, ID, NY); cross-reference `knowledge-base/best-practices/` for the disclosure-sheet templates and verification-against-non-AI-source expectations from prior cycles; cross-reference `knowledge-base/tools-ecosystem/ai-funding-policy-and-agentic-tools.md` for the district AUP / state mandate context and approved tool roster
- **Match-the-AUP-not-paraphrase rule:** when the district AUP or state mandate uses specific language ("AI may be used to", "AI shall not be used for", named prohibited uses like AI-for-grading, AI-for-discipline, AI-for-IEP-development), the syllabus block uses the AUP's exact language verbatim, not a paraphrase that introduces drift. The skill flags any paraphrase the teacher might have used in a prior version that drifts from the AUP.
- **Conflict-flag rule:** when the district AUP and the state mandate disagree, the skill flags the conflict to the teacher and surfaces the conservative posture (the more restrictive of the two) as the default, with the named district contact for escalation. The skill does not silently reconcile a real conflict.
- **Tool-on-the-roster rule:** the skill produces green-light language only for tools on the district-approved roster. If the teacher has named a tool not on the roster, the skill flags the gap and refuses to write a green-light row until the roster is updated or the tool is removed from the course's approved list.
- **No-PII-into-any-tool rule:** the disclosure block names student-PII categories that may not be entered into any tool, including district-licensed tools, unless the tool's DPA explicitly permits the listed use. The default posture is no-PII; the exceptions are explicitly named, not assumed.
- **Verify-not-detect rule:** the disclosure-sheet template builds in a verify-against-non-AI-source step rather than a detector-score check. The skill writes a one-line statement that detector scores alone are not academic-integrity evidence, mirroring federal and most state guidance, and routes academic-integrity concerns to the named district academic-integrity contact rather than to a detector workflow.
- **Opt-out-without-penalty rule:** the disclosure block names an opt-out path for students whose families have cultural, religious, privacy, or pedagogical concerns about AI use. The opt-out is a real alternative assignment, not a punitive bypass; the alternative is named per assignment row in the permission grid and is academically equivalent in scope and rigor.
- **Plain-language rule:** the syllabus block is written at the household reading level the district uses for parent communications (typically 6th–8th grade, district-configured), not at policy-document register. Parent-facing language explains the why in one sentence before the rule. Student-facing language uses second-person ("you may", "you must", "you can ask me") rather than third-person passive.
- **No-deficit-language rule:** AI-use disclosure language describes the course's expectations and the student's role, not the student's character. "Students who use AI without disclosing it are not following the course's attribution standard" is preferred over "Students who use AI without disclosing it are cheating." The harder conversation about academic dishonesty happens elsewhere (academic-integrity contact, dean / AP / principal); the syllabus disclosure is a clear standard, not a verdict.

**Process:**

1. **Build the syllabus AI block in three stacked sections.** (a) The Why — one paragraph in plain language explaining what AI is in this course, why the teacher has chosen this stance, and what the student gets from following it ("In this course you will write, think, and reason about [content]. AI tools can speed up some parts of that work and replace other parts. The rules below tell you which is which, so you can use AI well and still learn what this course is supposed to teach you."). (b) The What — the traffic-light frame named once, with red / yellow / green tied to specific tasks via the permission grid, not described in the abstract. (c) The How — the attribution standard, the disclosure-sheet expectation, the verification-against-non-AI-source expectation, the opt-out path, and the named district academic-integrity contact for questions or concerns.

2. **Build the permission grid as a table with one row per major assignment.** Columns: Assignment / Light (Red / Yellow / Green) / Permitted AI Use (specific verb — brainstorm / outline / get-feedback / clarify / draft-with-attribution / analyze / none) / Approved Tools for This Use / Attribution Standard (Tool-Date / Tool-Date-Prompt / Tool-Date-Prompt-Edits / Full-Transparency) / Verification Source / Opt-Out Alternative. The grid is the load-bearing artifact — a one-line "AI is allowed" syllabus statement is the failure mode this skill exists to replace.

3. **Mirror district AUP and state-mandate language verbatim in the prohibited-uses section.** Pull the named prohibitions (NYC red-light: AI for deciding grades, promotions, discipline, counseling, IEP development; Ohio model: PII protections, FERPA, COPPA; state-specific bans on AI-as-graduation-decision-maker, AI-as-final-arbiter-of-discipline, AI-as-only-source-of-academic-integrity-evidence) into the block as a clearly-titled "What This Course Will Not Use AI For" sub-block that mirrors the AUP exactly.

4. **Build a one-page Student Disclosure Sheet template the class will use across assignments.** The sheet has: assignment name and date / tool(s) used / prompts (verbatim or summarized per the course's standard) / what the AI produced / what the student kept and what the student changed / a one-paragraph "thinking ownership" reflection (what thinking did I do, what thinking did the AI do, where does the line fall, would I be able to defend my answer without the AI). The sheet is paste-ready into Google Docs / Word / Notion / Canvas / Schoology / Seesaw and works at the course's named reading level.

5. **Build a one-page Parent / Family Summary in plain language.** The summary explains: what AI tools the course uses, what students are allowed to do with them (in three short bullets, not a policy excerpt), how the teacher will know AI was used (the disclosure sheet, not a detector), what to do if a family wants the student to opt out (named alternative, named contact), and what district AUP / state-mandate this aligns to (one sentence, with the district AI coordinator's name and contact). The summary is translated into the district's home languages above the threshold for translated communications.

6. **Build a per-unit refresh prompt the teacher can run mid-term.** A 5-question diagnostic the teacher answers at the start of each unit ("Has the approved tool roster changed? Has the district AUP version changed? Has the state-mandate language changed? Does any new assignment in this unit need a row in the permission grid? Has the class run into a disclosure dispute that suggests a row needs more specificity?"). The diagnostic produces a per-unit delta the teacher pastes into the LMS unit landing page, so the disclosure stays fresh without a full rewrite.

7. **Tie the disclosure to the rubric.** For each green-light or yellow-light assignment, write one rubric criterion (or amend an existing one) that scores the disclosure-sheet completeness and the verification-against-non-AI-source step. The criterion is observable in the submitted artifact (sheet present / tools named / prompts captured / "what I changed" reflection present / non-AI source named) — not "Student is honest about AI use."

8. **Tie the disclosure to a parent-teacher conference talking point.** One conference line the teacher can use to explain the course's AI rules in 30 seconds at the conference: "Here is the one-page summary I sent home in [month]. Here is what your student has been turning in for the disclosure sheet. Here is what we have noticed together this term." Pairs with the Parent-Teacher Conference Prep Generator.

9. **Surface the academic-integrity-not-detector escalation path.** Write a clearly-titled "If You Have a Question About AI Use" block that names: the teacher as the first contact, the named district academic-integrity coordinator or designee as the second, the district AI coordinator as the third, and the families' parent-portal / FACE office contact as the family-side escalation. The block names that detector scores alone are not academic-integrity evidence, mirroring federal and most state guidance, and that any concern goes through the conversation-with-the-student step before a formal academic-integrity referral. This is the structural-not-surveillance posture.

10. **Surface the IEP/504-AI carve-out.** A short, plain-language paragraph names that AI tools are not used to make decisions about IEP / 504 plans, accommodations, eligibility, discipline outcomes, grade-level promotion, or special-education placement (mirroring NYC red-light and the CDT framework). When AI is used in a teacher's drafting workflow for an IEP or 504 document, the document carries an AI-Use Disclosure statement, the teacher remains the human author of record, and edit-history is preserved. The block is the syllabus-level signal to families that the harder special-education-AI questions have a known, named answer.

**Output requirements:**

- **Header block:** course name, grade band, content area, term, AUP version, state-mandate citation, school-board ratified policy date, district AI coordinator name and contact, course teacher name and contact, drafting date, version
- **Syllabus AI Block (three stacked sections — The Why / The What / The How)** at the course's named length and reading level
- **Permission Grid table** — one row per major assignment with the seven columns named above, plus a default-syllabus-posture row that catches assignments not listed
- **Prohibited-Uses sub-block** mirroring the district AUP and state-mandate language verbatim
- **One-Page Student Disclosure Sheet** template, paste-ready and reading-level-calibrated
- **One-Page Parent / Family Summary** in plain language at the household reading level, with translation note for languages above the district threshold
- **Per-Unit Refresh Prompt** — 5-question diagnostic for the teacher's start-of-unit run
- **Rubric Criterion** rewritten or amended for each green-light or yellow-light assignment, observable in the submitted artifact
- **Parent-Teacher Conference Talking Point** — one 30-second line for the conference cycle
- **"If You Have a Question About AI Use" Escalation Block** — named contacts, no-detector-as-sole-evidence statement, conversation-first posture
- **IEP / 504 AI Carve-Out Paragraph** — plain-language statement that AI is not used to decide IEP / 504, accommodations, discipline, promotion, or placement; AI-Use Disclosure on any AI-assisted IEP/504 drafting workflow
- **Subgroup-Support Block** — EL translated summary, IEP/504 response-mode flexibility, no-home-AI alternative, opt-out path
- **Conflict-Flag Block** — any flagged conflict between district AUP and state mandate, named for teacher resolution before publishing
- **Tool-Roster-Gap Block** — any tool the teacher named that is not on the district-approved roster, named for resolution before publishing
- **Disclosure / attribution alignment line** confirming the syllabus block aligns to the district AUP version, the state-mandate citation, and the school-board ratified policy date
- **Sources / Citation Footer** naming the district AUP, state mandate, federal priority, and any UNESCO / OECD framework the course mirrors
- Saved to `outputs/syllabus-ai-blocks/[course]-[term]-[version]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> **Context:** 9th-grade ELA, semester course (fall). District AUP loaded from config (NYC-aligned red-yellow-green model; board-adopted 2026-03-15). District AI coordinator: Ms. Yolanda Rivera, yrivera@[district].k12. State: New York (NYC model policy, June 2026 comprehensive playbook). Approved tools for this course: Claude for Education (district-licensed, student-allowed), Khan Academy (Khanmigo, student-allowed). Teacher-supplied assignments: argumentative essay (2), research paper (1), in-class Socratic seminar (3), common assessment (2), independent reading project (1), grammar and mechanics in-class quiz (2).

---

**Header Block**

> Course: 9th-Grade ELA (Honors) | Grade Band: 9–12 | Content Area: ELA
> Term: Fall Semester 2026–27 | Period structure: 5-day, 50-min periods
> AUP Version: [District] AI Acceptable Use Policy, adopted 2026-03-15
> State mandate: NYC traffic-light model (June 2026 comprehensive playbook)
> District AI Coordinator: Ms. Yolanda Rivera | yrivera@[district].k12 | ext. 4412
> Teacher: [Name] | [email] | Drafted: 2026-08-22 | Version: 1.0

---

**Syllabus AI Block — Medium Length (~300 words)**

**The Why**

In this course you will read, write, and argue about literature, language, and ideas. AI tools can speed up some parts of that work — finding a synonym, checking a citation format, getting quick feedback on a draft. They can also replace other parts, and when they replace the parts that are supposed to develop your thinking, you walk out of the course having learned less than you put in. The rules below tell you which is which, so you can use AI well and still get what this course is supposed to give you.

**The What**

This course uses the district's red-yellow-green model:

- 🔴 **Red** — AI is not permitted. In-class assessments, Socratic seminars, and common assessments are Red. These are moments when I need to see *your* thinking in real time.
- 🟡 **Yellow** — AI is permitted for specific, named uses only (brainstorming, outlining, feedback on a draft you wrote). The permission grid below names the exact use for each assignment. You must disclose any Yellow-light AI use on your Disclosure Sheet.
- 🟢 **Green** — AI is permitted with full disclosure and attribution. Only one assignment in this course is Green (see grid). The Disclosure Sheet is required.

The permission grid below shows each major assignment, its light, what you may use AI for, which tools are approved, and the verification step.

**The How**

For any AI use: complete the Student Disclosure Sheet (one per submission; template below). The attribution standard for this course is **Tool-Date-Prompt-Edits** — you name the tool, the date you used it, the prompt verbatim, and what you kept and changed. For all AI-touched work, you must verify at least one key claim against a non-AI source (textbook page, primary source, or teacher-curated reading). The district academic-integrity contact is [name], [email]. Detector scores alone are not evidence of a policy violation — any concern starts with a conversation.

---

**Permission Grid (abbreviated — 8 of 12 assignment rows shown)**

| Assignment | 🚦 | Permitted AI Use | Approved Tools | Attribution Standard | Verification Source | Opt-Out Alternative |
|---|---|---|---|---|---|---|
| Argumentative Essay (take-home) | 🟡 | Brainstorm claim, generate counterargument list, get line-edit feedback on draft *you* wrote | Claude for Education | Tool-Date-Prompt-Edits | One primary or secondary source cited in the essay | Approved; alternative: write with no AI and note "No AI used" on sheet |
| Research Paper | 🟡 | Summarize source abstracts to help with source selection only; no AI drafting | Claude for Education | Tool-Date-Prompt | Minimum 3 non-AI sources cited | Approved; no-AI option earns standard credit |
| Socratic Seminar (in-class) | 🔴 | None — live discussion | None | N/A | N/A | N/A |
| In-Class Common Assessment | 🔴 | None — closed-book, supervised | None | N/A | N/A | N/A |
| Independent Reading Project | 🟢 | Drafting permitted with full disclosure; AI output is a scaffold, not the final product; must include metacognitive reflection | Claude for Education, Khanmigo | Full-Transparency | At least one textual quote from the independent reading text | Approved; no-AI option earns same credit if disclosure sheet notes "No AI used" |
| Grammar & Mechanics Quiz (in-class) | 🔴 | None | None | N/A | N/A | N/A |
| Vocabulary Practice (ongoing) | 🟡 | AI for explanation and example only; no AI-generated answers submitted | Khanmigo | Tool-and-Date | N/A | Approved |
| *Default — all other assignments* | 🟡 | Brainstorm and outline only | Claude for Education | Tool-Date-Prompt | Named in assignment instructions | Per-assignment adjustment flagged |

---

**Student Disclosure Sheet (paste-ready)**

> **AI Use Disclosure — [Your Name] — [Assignment Name] — [Date]**
> Tool(s) used: ___
> Date(s) of use: ___
> Prompt(s) (verbatim or summarized per course standard): ___
> What the AI produced: ___
> What I kept: ___ | What I changed: ___
> Verification source (non-AI): ___
> *If no AI tools were used: "No AI tools were used on this assignment."*

---

**Conflict-Flag Block**

> ⚠️ **No conflicts detected** between the district AUP (adopted 2026-03-15) and the NYC traffic-light model (June 2026 playbook) for this course configuration. If the district AUP is updated before the end of the semester, re-run the per-unit refresh prompt (see below) to surface any new conflicts. Contact Ms. Yolanda Rivera (yrivera@[district].k12) for any AUP interpretation questions.

> *(If a conflict had been detected, the block would read: "⚠️ Conflict detected: The district AUP [section X] requires [Y] but the NYC model policy requires [Z]. The conservative posture ([more restrictive rule]) is applied here as the default. Contact Ms. Rivera before publishing this syllabus block.")*

---

*Full output also includes: one-page Parent/Family Summary (plain language, translation note for home languages above threshold), per-unit refresh prompt (5-question diagnostic), rubric criterion for each Green/Yellow assignment, parent-teacher conference talking point, "If You Have a Question" escalation block, IEP/504 AI carve-out paragraph, and subgroup-support block — omitted here for length.*
