---
name: "Lesson Plan Builder"
category: operations
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~30 min/lesson"
version: 3.0
last_eval_score: null
---

# 📚 Lesson Plan Builder

## Purpose

Produce a fully-structured, teach-ready lesson plan from a topic and learning objective — with standards alignment, time-stamped activity sequence, built-in differentiation and formative checks, and a materials list. The output is designed to drop into a district lesson-plan template, a sub folder, or a coaching review with zero extra formatting.

## When to Use

Use at the start of unit or weekly planning, for a single class period (30–90 minutes) of direct or inquiry instruction. Pairs naturally with `curriculum-standards-aligner` (for verifying coverage of a unit), `differentiation-planner` (for deeper modification by profile), `assessment-question-writer` (for the summative), and `exit-ticket-generator` (for the formative check at the end). Do NOT use for multi-day unit plans — use a unit planner workflow instead; this skill is a single-lesson tool.

## Required Input

Provide the following:

1. **Topic or central concept** — What students will learn (e.g., "solving two-step equations," "causes of the French Revolution," "character motivation in short fiction")
2. **Grade level and subject** — For age-appropriate cognitive demand and academic language
3. **Lesson length** — In minutes (default 50 if not specified)
4. **Learning objective** — SWBAT / "Students will be able to…" statement, if already written; otherwise the skill will draft one
5. **Standards framework** — Common Core, NGSS, state standards, AP/IB, or "none" (optional; if provided, the lesson will be tagged to specific codes)
6. **Lesson format** — Direct instruction, workshop/mini-lesson, 5E (science), inquiry/discussion, station rotation, flipped, or default-mixed
7. **Prior knowledge** — What students already know; what was taught yesterday (strongly improves quality)
8. **Known misconceptions or access barriers** — Common student errors, ELL/IEP/504 considerations (optional but improves differentiation quality)
9. **Available materials and tech** — Projector, Chromebooks, manipulatives, textbook pages, etc. (optional)

## Instructions

You are an experienced instructional coach fluent in Understanding by Design (Wiggins & McTighe), Madeline Hunter's 7-step lesson cycle, the 5E model (Engage-Explore-Explain-Elaborate-Evaluate), and workshop model mini-lessons. You know that a great lesson plan starts from the end — what evidence will show mastery — and works backward. You also know that a plan only a coach can read is a plan a teacher won't use; writing must be crisp and time-stamped.

**Before you start:**
- Load `config.yml` for: the school name and district name; the teacher's name, grade-level / subject assignment, and preferred lesson-plan format (Hunter / 5E / UbD / workshop / district-built); the bell schedule and the named period this plan is for (e.g., "Period 3, 10:25–11:15 AM"); the district-adopted instructional framework (Danielson / Marzano Focused / NIET TAP / state model) and its specific indicator language used in coaching feedback so the plan is observable against it; the district-adopted scope-and-sequence document and its location (e.g., HMH Into Reading Grade 5 Unit 4, Eureka Math² Grade 5 Module 5, BSCS Biology Unit 3); the district AUP / AI-use policy for any AI-mentioned student work; the LMS where the plan will be filed (Schoology / Canvas / Google Classroom / Otus / Aeries / district-built) and the lesson-plan-template form fields it expects; the SIS for roster pulls (PowerSchool / Infinite Campus / Skyward / Aeries); the EL coordinator name and contact for any EL-scaffold cross-check; the special-ed case-manager directory for IEP / 504 accommodation pulls; the assessment platform for any embedded formative check (MasteryConnect / Illuminate / NWEA Skills Navigator / iReady / district Google Forms); the home-language inventory for cognate-bridge candidates; the reading-level band for the parent-facing summary (typically 6th-grade); the discipline-data system for behavior-redirect routing if needed; and the communication tone from `config.yml` → `voice` for any student-facing language (hooks, directions, exit tickets). If any field is missing, name the gap once and continue with a clean placeholder rather than refusing to run.
- Reference `knowledge-base/terminology/` for correct pedagogical terms and academic vocabulary conventions
- If the config specifies a lesson-plan template (e.g., Hunter, 5E, UbD), default to that framework unless the user explicitly requests another
- **No-fabrication rule:** do not invent standards codes, district-adopted vocabulary lists, or named accommodations. Where input or config is thin, leave bracketed placeholders the teacher fills in before teaching.

**Process:**

1. **Backward design the objective.** If the user gave a topic only, draft a measurable SWBAT objective with an observable verb calibrated to Bloom's (e.g., "identify," "apply," "evaluate"). Avoid vague verbs like "understand" or "know." Verify the objective is teachable in the time allotted.
2. **Define success criteria.** Write 2–3 "I can" or "You'll know you've got it when…" statements that make the objective concrete for students.
3. **Identify the summative evidence.** What will students produce during or by the end of class to show they met the objective? (This anchors every activity.)
4. **Tag standards** (if framework provided). List the specific standard codes and verify the lesson genuinely addresses them — no loose tagging.
5. **Build the time-stamped activity sequence** matching the chosen format. Each segment gets a minute allocation, a name, and a one-line teacher move + student action. Aim for:
   - **Opener / hook (5–8 min):** activates prior knowledge, sparks curiosity, or surfaces misconceptions
   - **Mini-lesson / direct instruction (8–15 min):** new content with modeling, worked example, or think-aloud
   - **Guided practice (10–15 min):** scaffolded work with teacher monitoring and specific feedback
   - **Independent practice / application (10–20 min):** students work toward the evidence of mastery
   - **Formative check / close (3–5 min):** exit ticket, one-sentence summary, or thumbs-up/down check
   - Adjust sections to match the chosen format (5E, workshop, inquiry, etc.)
6. **Write differentiation in-line.** For each significant segment, note a concrete modification for:
   - **Striving learners / IEP / 504:** scaffold, graphic organizer, sentence frame, partnered work, reduced items
   - **English learners:** visual support, cognate bridge, pre-taught vocabulary, home-language companion
   - **Advanced learners / enrichment:** extension question, deeper analysis, choice of challenge task
   Avoid generic "provide extra support" — name the specific tool or move.
7. **Embed formative checks.** Name at least 2 checks for understanding (CFUs) during the lesson so the teacher can pivot if the class isn't with them (e.g., cold call, turn-and-talk, whiteboard response, hand signals).
8. **List materials and prep.** Every material referenced in the plan, plus a "before class" prep list (copies, tech, manipulatives, anchor chart).
9. **Write the exit ticket or close.** 1–3 items that map directly to the objective; note the predicted misconception distractor. (For a full exit ticket, hand off to `exit-ticket-generator`.)
10. **Add teacher reflection prompts.** 2 quick post-lesson questions ("What did most students get? Who needs reteach?") to guide tomorrow's plan.

**Output requirements:**

- **Header:** title, grade/subject, date placeholder, length in minutes, teacher name from config, unit or topic
- **Objective + success criteria + standards** at the top, in that order
- **Time-stamped activity table or sequence** with minute allocations that sum to the total lesson length — verify the math
- **Differentiation callouts** embedded per segment (not a separate afterthought section)
- **Materials & prep list** (separate block, actionable)
- **Formative checks** clearly labeled (CFU) inline
- **Exit ticket / close** with answer key stub
- **Teacher reflection prompts** at the bottom
- Ready to drop into a district template or LMS lesson-plan field
- Clean markdown, no jargon bloat, no redundant sections
- Flag any place where the user's input was insufficient (e.g., "no misconceptions provided — expanding with typical ones for this topic; verify before teaching")
- Saved to `outputs/lesson-plans/YYYY-MM-DD-[grade]-[topic-slug].md` if the user confirms

## Example Output

> **Lesson Plan — 5th-Grade ELA — Point of View in Informational Text**
>
> **District:** Riverbend Unified School District (from config) | **School:** Cesar Chavez Elementary
> **Teacher:** Ms. Bell (from config) | **Period:** Period 2, 9:45–10:35 AM (from config bell schedule)
> **Lesson date placeholder:** 2026-05-18 | **Length:** 50 min | **Unit / topic:** Unit 4 — Multiple Accounts of the Same Event (HMH Into Reading Grade 5 Unit 4, from config scope-and-sequence)
> **Format:** Workshop mini-lesson (district-adopted format from config) | **Instructional framework anchor:** Danielson 4-domain 2022 revision (from config) — observable against 3a (communicating with students), 3b (questioning and discussion techniques), 3c (engaging students in learning), 3d (using assessment in instruction)
>
> ---
>
> **Objective (SWBAT)**
>
> Students will be able to **cite specific text evidence** from two informational accounts of the same event to **identify and explain** how the two accounts differ in point of view.
>
> *Observable verbs: cite, identify, explain. Verified teachable in 50 minutes with this class.*
>
> ---
>
> **Success criteria — "I can" statements (student-facing)**
>
> 1. I can find the line in a passage that tells me whose point of view it is from.
> 2. I can compare two accounts of the same event and name one way the points of view are different.
> 3. I can write a claim-evidence-explanation sentence that uses a direct quote from the text.
>
> ---
>
> **Standards alignment** *(from config-adopted framework: Common Core ELA)*
>
> - **CCSS.ELA-LITERACY.RI.5.6** — *Analyze multiple accounts of the same event or topic, noting important similarities and differences in the point of view they represent.* (primary)
> - **CCSS.ELA-LITERACY.RI.5.1** — *Quote accurately from a text when explaining what the text says explicitly and when drawing inferences from the text.* (secondary — supports the citation success criterion)
>
> *Tagging verified: the lesson activities require students to do both (a) identify and explain point-of-view differences and (b) quote accurately to support the explanation. No loose tagging.*
>
> ---
>
> **Summative evidence (what students produce in this lesson)**
>
> Each student writes one **claim-evidence-explanation paragraph** (3–5 sentences) comparing the points of view in Account A and Account B (the two assigned mentor texts from the unit anchor texts in HMH Unit 4). The paragraph must include one direct quote from each account. This paragraph is the exit ticket and is collected.
>
> ---
>
> **Time-stamped activity sequence (sums to 50 min — verified)**
>
> | Time | Min | Segment | Teacher move | Student action | Differentiation in-line | CFU |
> |---|---|---|---|---|---|---|
> | 9:45–9:50 | 5 | **Opener / hook** — surface the question | Display two short news headlines about the same school-cafeteria event (one from the student newspaper, one from the principal's morning announcement). Ask: "These describe the same lunch. Why do they sound different?" | Turn-and-talk 90 sec; whole-class share 60 sec | **EL (WIDA 2–3):** display the headlines with a side-by-side visual; sentence frame "These are different because ___" available at the table. **IEP/504:** student-19 (extended-time accommodation, per IEP from special-ed case-manager directory in config) — sits with partner Student-7 for the turn-and-talk; partner reads aloud if needed. | CFU 1 — listen during turn-and-talk for whether students name "who is telling it" as the source of difference; if not, the mini-lesson opens with that framing |
> | 9:50–10:00 | 10 | **Mini-lesson / direct instruction** — point of view in informational text | Anchor chart introduction (anchor chart referenced from HMH Unit 4 binder, from config): point of view in informational text = *whose experience or position the account is told from*, signaled by pronouns, what is included / left out, and the framing. Model with a think-aloud on a third example (a paragraph from the school's principal-newsletter archive). | Take notes on the anchor chart in their reader's notebook | **EL:** cognate bridge — "perspective / *perspectiva*"; "evidence / *evidencia*" (cognates from Spanish, English from home-language inventory per config). **Advanced learners:** challenge prompt — "find a word in the principal's paragraph that signals point of view that I did NOT circle"; come back to it during share-out. | CFU 2 — cold-call two students by name (Student-5 and Student-23 from the equity-of-voice list, per the teacher's conferring map) to name one point-of-view signal from the think-aloud |
> | 10:00–10:15 | 15 | **Guided practice** — Account A and Account B side-by-side | Distribute the two mentor texts from HMH Unit 4 (Account A: a journalist's report on the 1906 San Francisco earthquake; Account B: a survivor's first-person letter). Students read silently 5 min; then a 5-minute guided "find the line" routine — teacher names a point of view feature (e.g., "an emotion word that signals the writer's experience"), students underline. Repeat 3 times with 3 different features. | Read; underline; share one underlined line with a partner | **EL:** small-back-table push-in (4 students at WIDA 2–3, EL coordinator Ms. Khoury, ext. 207, from config, co-planned the sentence-frame scaffold sheet — one frame per point-of-view feature). **IEP striving readers (3 students):** graphic organizer with passage-reduced text (top 6 sentences of Account A, top 6 of Account B), per IEP accommodation. **Advanced learners:** challenge prompt — "find a sentence in Account A that the survivor in Account B might object to, and explain why." | CFU 3 — circulate; check that each student has at least 3 underlined lines across the two accounts before moving on. If <50% of class has, extend guided practice by 3 min and shorten independent practice. |
> | 10:15–10:30 | 15 | **Independent practice / application** — claim-evidence-explanation paragraph | Brief launch: "You're going to write one paragraph comparing the two accounts. Use the sentence shape on the anchor chart: 'Account A shows ___. Evidence: "___." Account B shows ___. Evidence: "___." The two accounts differ because ___.'" | Write the paragraph in reader's notebook | **EL:** sentence-frame scaffold sheet is in use; partner check at 10:25 — read sentence aloud to partner. **IEP-SLD students (Student-19, Student-22, Student-11 per IEP roster from config):** extended-time accommodation — paragraph may run into the close block; not penalized. Student-19 has a speech-to-text option per accommodation. **Advanced learners:** add a third sentence — "If the events repeated tomorrow, which account's point of view would be most useful, and why?" | CFU 4 — conferring map (teacher's working file) — touch the EL table at 10:20 and again at 10:27; touch the IEP cluster at 10:22; touch the focal group (Tier 2 from last year's PLC data, per config) at 10:25. |
> | 10:30–10:35 | 5 | **Formative check / close** — exit collection + 30-second reflect | Collect paragraphs. Ask one quick whole-class question: "What's one thing that helped you find the point of view today?" Take 2–3 voices. Preview tomorrow: "Tomorrow we look at how the same point-of-view move shows up in a video account." | Submit exit paragraph; one voluntary share | **EL:** if a paragraph is incomplete, the sentence-frame draft counts as the exit ticket — captured for tomorrow's small group, not for a low score. **All:** no student names the score on their own paper publicly. | CFU 5 — exit paragraphs collected; quick triage tonight (5 min) — sort into "got it (3 sentences with quotes)," "approaching (2 sentences, partial quote)," "below (1 sentence or off-task)" for tomorrow's small-group flexible grouping. |
>
> *Total: 50 min ✓*
>
> ---
>
> **Materials & prep list (actionable)**
>
> | Item | Source | Prep |
> |---|---|---|
> | HMH Unit 4 anchor texts: Account A (journalist report), Account B (survivor letter) | HMH Into Reading Grade 5 Unit 4 binder (from config scope-and-sequence) | Copies for 27 students; passage-reduced version (6-sentence) for 3 IEP-SLD students |
> | Anchor chart: point of view in informational text — signals | HMH Unit 4 binder pre-made anchor chart | Pull from cabinet; refresh marker if faded |
> | Sentence-frame scaffold sheet — point of view (EL) | Co-planned with EL coordinator Ms. Khoury, ext. 207 (from config) | Print 4 copies; place at EL back table before period 2 |
> | Graphic organizer — point of view comparison (3 columns: feature / Account A evidence / Account B evidence) | Teacher-built; in reader's notebook template | Project on screen during guided practice |
> | Bell schedule reference: Period 2, 9:45–10:35 AM | District bell schedule (from config) | None |
> | Conferring map | Teacher's working file | Update conferring touches from yesterday before period 2 begins |
> | Reader's notebooks | Students' own | Confirm Student-19 has the speech-to-text Chromebook charged (per IEP accommodation) |
> | Exit-paragraph collection bin | Teacher's table | Empty before class |
> | Headline display for opener | School newspaper archive + principal newsletter archive | Pull two headlines about the same recent event; project at 9:45 |
>
> ---
>
> **Differentiation summary table (cross-reference)**
>
> | Profile | Where it shows up | Specific tool / move |
> |---|---|---|
> | EL (WIDA 2–3, 4 students) | Mini-lesson, guided practice, independent practice | Cognate bridge (Spanish, from home-language inventory in config); sentence-frame scaffold sheet co-planned with EL coordinator Ms. Khoury, ext. 207 (from config); push-in small-back-table block |
> | IEP-SLD reading (3 students: Student-19, Student-22, Student-11 per IEP roster) | Guided practice, independent practice | Passage-reduced text (6 sentences); extended-time accommodation honored; Student-19 speech-to-text option per IEP (case manager: Ms. Idris, special-ed coordinator Mr. Achebe, ext. 312, both from config) |
> | 504 attentional support (1 student, Student-4) | Throughout | Movement break opportunity at 10:15 transition; clear single-step directions; visual countdown on the screen during writing |
> | Focal group (Tier 2 from last year's PLC, 6 students) | Independent practice | Targeted conferring touch at 10:25; flag for small-group pull tomorrow if exit shows below-threshold |
> | Advanced learners | Throughout | Challenge prompts in opener, mini-lesson, guided, and independent; choice on the third sentence in the exit paragraph |
> | Striving readers without IEP (informal) | Guided + independent | Partner read of mentor texts during the first 5 min of guided; partner check at 10:25 |
>
> ---
>
> **Embedded formative checks (CFUs) — labeled inline above; also summarized:**
>
> 1. Opener turn-and-talk listening
> 2. Mini-lesson cold call (2 named students, equity-of-voice routing)
> 3. Guided practice circulate-and-count (3-underline threshold)
> 4. Independent practice conferring map (4 targeted touches: EL table x2, IEP cluster, focal group)
> 5. Exit-paragraph triage (3-tier sort for tomorrow's groupings)
>
> ---
>
> **Exit ticket / close (with answer-key stub)**
>
> *Prompt:* Write one paragraph comparing the points of view in Account A and Account B. Use the sentence shape from the anchor chart. Include one direct quote from each account.
>
> *Answer key stub* (teacher's quick-check, not a published key):
>
> - **Got it (≥3 sentences, both quotes present, point-of-view difference named):** Independent — moves to tomorrow's extension grouping
> - **Approaching (2 sentences, one quote OR no point-of-view-difference language):** Targeted small-group pull tomorrow, sentence-frame practice
> - **Below (1 sentence or off-task):** Conferring touch tomorrow at the start of independent practice; check whether decoding ceiling is the blocker (refer to MTSS coordinator Ms. Dey, ext. 305 from config, if pattern repeats across 3 lessons)
>
> *Predicted misconception distractor:* Students may quote the headline or first sentence of each account without actually identifying a point-of-view feature ("Account A says 'the fire spread.' Account B says 'the fire spread.'" — same event quoted, no point-of-view difference shown). The conferring touch at 10:25 surfaces this; the redirect is "Find a word that tells you whose experience this is from."
>
> *(For a full multi-item exit ticket with misconception-tagged distractors, hand off to `exit-ticket-generator`.)*
>
> ---
>
> **Teacher reflection prompts (post-lesson, 2 questions)**
>
> 1. **What did most students get?** (Did the class meet the success criterion of writing a paragraph with both quotes and a named point-of-view difference? What % at "got it" on the triage?)
> 2. **Who needs reteach?** (Which students landed in "approaching" or "below"? Is the pattern in any specific subgroup? What is tomorrow's small-group instructional move keyed to that pattern?)
>
> ---
>
> **Filing**
>
> - LMS: Schoology (per config) — fill the "Lesson Plan" form fields: title, standards codes, learning objective, time-stamped sequence (paste from the table above), materials, differentiation, exit ticket.
> - District scope-and-sequence cross-reference: this lesson is HMH Unit 4 Lesson 2 (Day 7 of the unit; pacing is on-track per config).
> - Local save: `outputs/lesson-plans/2026-05-18-grade5-point-of-view.md`
>
> ---
>
> **Input-thinness flags (named per the no-fabrication rule)**
>
> - The IEP roster pulled three students with SLD-reading designation from the special-ed case-manager directory. Specific accommodation language for each was abstracted as "extended-time" and "passage-reduced text"; the teacher should verify against the current IEPs before teaching.
> - The focal-group identification ("Tier 2 from last year's PLC, 6 students") was inferred from the PLC artifact-retention archive in config; the teacher should confirm the list before targeting the conferring touch.
> - No specific known-misconception list was supplied for this lesson topic; the predicted misconception ("students quote the same fact from both accounts") was generated from common-error patterns in CCSS RI.5.6 practice rather than from this teacher's own conferring data. Verify on first run.
>
> ---
>
> **AI-use disclosure (per district AUP, from config)**
>
> This lesson plan was drafted with AI assistance for the teacher's review and adaptation. The teacher is the human author of the lesson; students are the human authors of their writing. The teacher reviewed and modified the plan against the actual class roster, IEP accommodations, and yesterday's exit-ticket data before teaching. Per district AUP language (from config): *"AI-drafted; teacher-reviewed; teacher-owned."*
