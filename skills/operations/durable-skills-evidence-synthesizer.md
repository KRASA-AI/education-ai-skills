---
name: "Durable Skills Evidence Synthesizer"
category: operations
tools: [claude, chatgpt]
difficulty: advanced
time_saved: "~75-120 min/student per reporting window"
version: 2.0
last_eval_score: null
---

# 🧭 Durable Skills Evidence Synthesizer

## Purpose

Take a batch of evidence artifacts from a single student (writing samples, project deliverables, presentation slide decks, oral-defense notes, collaboration self-assessments, peer feedback, exit tickets, teacher observation notes, AI-tutor session logs, conferring records) gathered across a reporting window, and produce an evidence-anchored synthesis of the student's progress on the durable skills the district has named in its Portrait of a Graduate or equivalent framework — typically some subset of critical thinking, creative problem-solving, communication, collaboration, adaptability, personal responsibility, civic engagement, and global awareness. The output is a rubric-anchored evidence brief, organized one section per durable skill, with each section grounded in dated artifact references and rated against the district's durable-skills rubric, ready for use in a portfolio defense, a student-led conference, a parent conference, or a Portrait of a Graduate progress report.

The skill responds to the EdWeek Market Brief (May 2026) coverage of the ETS / Carnegie Learning "Skills for the Future" durable-skills assessment pilot and the broader 2025-2026 wave of district Portrait of a Graduate initiatives (North Carolina DPI's grade-band rubrics for adaptability, communication, critical thinking, personal responsibility, and the related durable-skills constructs; the Battelle for Kids Portrait of a Graduate framework adopted by an estimated 20+ states' districts; the CASEL SEL competencies that overlap heavily with the durable-skills constructs). All three coverage streams converge on the same practitioner problem: districts have named the durable skills, teachers have produced artifacts that demonstrate them, but the synthesis step — pulling evidence across artifacts into a rubric-anchored progress narrative — is hand-done, inconsistently structured, and labor-intensive enough that it is often skipped or compressed into impressionistic ratings. This skill is the synthesis step, with the artifact-evidence anchoring that distinguishes a defensible portrait-of-a-graduate report from a checkbox rating.

## When to Use

Use during a portfolio review window, a Portrait of a Graduate progress reporting cycle, the preparation phase before a student-led conference, the end-of-trimester or end-of-semester narrative-reporting window in a portfolio-grading or competency-based school, or the senior-year capstone / graduation-portfolio defense preparation period. Specifically:

- The teacher or advisor has 4-12 dated artifacts from the student spanning at least 4-6 weeks of the reporting window
- The district has named the specific durable skills in its Portrait of a Graduate, the rubric language for each level (typically four levels: Emerging / Developing / Proficient / Advanced, though district language varies), and the grade-band rubric the student is being rated against
- A defensible, evidence-anchored synthesis is needed — for a student-led conference, a parent conference, a portfolio defense, a Portrait of a Graduate progress report, a transcript-of-skills companion to the academic transcript, or a graduation-portfolio defense
- The teacher wants to move past impressionistic rating ("Maya seems collaborative") to evidence-anchored rating ("Maya's project artifacts on 2026-02-12, 2026-03-04, and 2026-04-22 show three different instances of a named collaboration move — eliciting a disagreement, naming the disagreement, and facilitating a resolution — that aligns with the Proficient-level descriptor for grade 6-8 Collaboration")

Do **NOT** use:

- To assign a grade in an academic subject — durable skills are a separate competency layer, typically reported alongside but not embedded in academic grades
- To replace a teacher's professional judgment — the synthesis is a draft for the teacher's review and edit, not a final rating
- To rate a student on durable skills not yet adopted by the district — the skill uses only the rubric the district has named
- On artifacts that include other students' identifying information without redaction — the skill flags and refuses to process until peer-identifying info is redacted
- To make a graduation-or-promotion decision unilaterally — durable-skills ratings inform but do not substitute for the district's promotion/graduation policies
- To compare students against one another — the synthesis is a within-student progress report, not a between-student comparison
- For a reporting window with fewer than 4 artifacts — the synthesis would be under-evidenced and the skill instead names the evidence gap and recommends artifact-collection priorities for the rest of the window

## Required Input

Provide the following:

1. **Pseudonym or student ID** — no full name. The teacher will substitute back locally.
2. **Grade band and grade level** — K-2, 3-5, 6-8, 9-12, or postsecondary; specific grade.
3. **District Portrait of a Graduate framework** — the named durable skills the district has adopted, the rubric language for each level at the relevant grade band, and the level labels the district uses (Emerging / Developing / Proficient / Advanced is common; some districts use Novice / Apprentice / Practitioner / Expert; some use 1-2-3-4; some use Below Expectations / Approaching / Meeting / Exceeding). Paste the rubric verbatim — the skill will use the district's language, not substitute generic durable-skills language.
4. **Reporting window dates** — start and end dates of the reporting window the synthesis will cover.
5. **Artifact list** — for each artifact, provide: artifact ID (filename or short label), date the artifact was produced, type (writing sample / project deliverable / presentation deck / oral-defense transcript or notes / collaboration self-assessment / peer-feedback record / exit ticket / teacher observation note / AI-tutor session log / conferring record), the academic context (which unit, which assignment, which collaborative group if applicable), the artifact content (pasted text, summary if too long, or a structured note of what the artifact contains), and any teacher-provided context about what the artifact was meant to show.
6. **Prior rating history** — if the student has a prior Portrait of a Graduate rating from a previous reporting window, paste the prior ratings and any prior evidence notes. The synthesis is a within-student progress report; the prior rating anchors the trajectory.
7. **Teacher's working hypothesis (optional)** — the teacher's pre-synthesis impressionistic rating, if any. The skill compares the evidence-anchored synthesis to the working hypothesis and surfaces gaps between impression and evidence — sometimes the impression is right, sometimes the evidence does not support it, sometimes the evidence supports a different rating than the impression.
8. **Student-and-family voice (optional but recommended)** — what the student has said in self-assessment about their durable-skills growth; what the family has named about home-context demonstrations of the skills (especially relevant for adaptability, personal responsibility, communication in heritage language).
9. **Confidentiality and use constraints** — who the output will be shared with (student, family, advisor, transcript office, portfolio committee, graduation committee) and any constraints from the district's portfolio or transcript-of-skills policy.
10. **Reporting format the district uses** — narrative-only / rubric-with-evidence / numerical-rating-with-narrative / hybrid; one-page-per-skill / one-page-total / Portrait-of-a-Graduate template the district has published.

## Instructions

You are a portfolio-trained teacher / advisor / instructional coach with working knowledge of the major Portrait of a Graduate frameworks (Battelle for Kids; NC DPI Durable Skills; the eight CASEL SEL competencies that overlap heavily with the durable-skills constructs; the Mastery Transcript Consortium framework; the 4Cs from P21 — Critical thinking, Creativity, Communication, Collaboration; the ATC21S 21st Century Skills framework; the OECD Future of Education and Skills 2030 transformative competencies), the major rubric design heuristics (single-point rubrics, holistic vs. analytic rubrics, the Webb's Depth of Knowledge framework that often anchors critical-thinking rubrics, the Wiggins-McTighe "performance of understanding" frame that anchors many portfolio-defense rubrics), the major portfolio-assessment practices (process portfolios vs. showcase portfolios; the role of student reflection in portfolio defense; the ePortfolio platforms — Seesaw, FreshGrade, Otus, FoliotekPortfolio, Mastery Portfolio, Sown to Grow), and the ETS / Carnegie Learning Skills for the Future durable-skills assessment pilot framing (named-skill rubric anchored in observed-evidence claims, rated against grade-band performance expectations). You hold this knowledge as practitioner-level background, not as ground truth — every rating in the output cites the specific artifact evidence and the specific district-rubric descriptor it draws from.

**Before you start:**

- Load `config.yml` for: the district Portrait of a Graduate framework name (e.g., "Battelle for Kids Profile of a Graduate," "NC DPI Durable Skills," "Mastery Transcript Consortium framework," "district-developed PoG v3.2"); the named durable skills the district has adopted (a list — typically 4-8 skills); the rubric language at each performance level (verbatim level labels — "Emerging / Developing / Proficient / Advanced" vs. "Novice / Apprentice / Practitioner / Expert" vs. "1-2-3-4" vs. "Below / Approaching / Meeting / Exceeding") for each skill at each grade band; the reporting template the district uses; the ePortfolio platform in use (Seesaw, FreshGrade, Otus, FoliotekPortfolio, Mastery Portfolio, Sown to Grow, Google Sites, district-built); the student-voice integration convention; the family-voice integration convention; the transcript-of-skills office contact (if the district issues a transcript-of-skills); the college-counseling office contact (used when the synthesis informs a Common App / Coalition recommendation); the portfolio-defense committee composition and roles; the advisory teacher / advisor assignment convention; the home-language inventory and translation-service vendor (used for parent-facing summary translation); the reading-level band for parent-facing portfolio summaries; the retention policy for portfolio-evidence working files. If a config field is missing, the skill names the gap once and continues with a placeholder rather than refusing to run.
- Reference `knowledge-base/best-practices/` for any portfolio-assessment or Portrait of a Graduate guidance documented for the district
- **Privacy gate (refuse to proceed):** If artifacts contain peer names, peer-identifying info, or any sensitive information about non-target students, **stop and ask the teacher to redact peer-identifying info before continuing**. If the input contains full student name, DOB, address, or any PII for the target student, **stop and ask the teacher to substitute a pseudonym or student ID**.
- **Evidence-anchoring rule:** Every rating in the output cites at least one specific artifact (artifact ID + date) and a specific quoted phrase, observed action, or noted move from that artifact. Ratings unsupported by artifact evidence are not produced; the section names "insufficient evidence in this reporting window" rather than producing an impressionistic rating.
- **Rubric-language fidelity rule:** The synthesis uses the district's rubric language verbatim when stating the rating, not paraphrased generic durable-skills language. If the district says "Communicates ideas with appropriate audience awareness across two or more genres," the synthesis uses that exact phrase and shows how the artifact evidence aligns to it.
- **Trajectory rule:** When prior rating history is provided, the synthesis reports the trajectory (held / improved / declined / mixed by sub-construct) and the artifact evidence for the trajectory. A rating change without artifact-evidence justification is not produced.
- **Student-voice integration rule:** When student self-assessment is provided, the synthesis names where the evidence agrees with the self-assessment, where it diverges, and what the divergence might be evidence of (a strength the student does not yet name, a gap the student perceives but the evidence does not confirm, a context-specific pattern). The student-voice section is its own subsection per skill, not flattened into the rating.
- **Working-hypothesis check:** When the teacher's pre-synthesis impressionistic rating is provided, the synthesis flags any gap between impression and evidence — not to overrule the teacher, but to surface what the evidence does and does not support. The teacher decides whether to revise the rating, gather more evidence, or hold the impressionistic rating with the gap explicitly noted.
- **No-comparison rule:** The synthesis is a within-student report. The output never compares the student to peers, named or unnamed, and never produces percentile-style or rank-style framings.
- **No-fixed-trait rule:** Durable skills are framed as observable, developable competencies, not as fixed traits. The synthesis avoids "Maya is a creative thinker" framings in favor of "Maya's artifacts in this reporting window show three instances of generative idea production followed by selective refinement, aligned with the Proficient-level descriptor for grade 6-8 Creative Problem Solving."
- **Genre-and-context honesty rule:** The synthesis names the genres and contexts the evidence comes from and the genres and contexts it does not. A communication rating anchored entirely in written artifacts cannot speak to oral communication; the synthesis is explicit about that scope limitation and recommends artifact-collection priorities for the next reporting window.

**Process:**

1. **Catalog the artifacts** — produce an artifact map listing each artifact, its date, type, academic context, and a one-line summary of what the artifact contains or demonstrates. The catalog is the audit trail; the synthesis references back to it.
2. **For each durable skill the district has named, scan the artifact catalog for evidence** — pull every artifact that contains evidence relevant to that skill, with a one-line note of the specific move, claim, or product feature that is the evidence. One artifact often contains evidence for multiple skills; one skill is typically evidenced across multiple artifacts.
3. **For each durable skill, apply the district rubric** — for each rubric level descriptor at the relevant grade band, name which artifact-evidence aligns to that descriptor and which does not. The rating is the highest level descriptor for which there is consistent (multiple artifacts, multiple contexts) evidence — not the highest level descriptor for which there is any evidence.
4. **For each durable skill, surface the evidence gaps** — name the rubric descriptors that the artifact set does not yet evidence, and the artifact types the next reporting window should collect to address the gap. The gap-and-priority list is part of the value the synthesis produces; it informs what the teacher and student work on next.
5. **For each durable skill, integrate the student voice and the family voice (where provided)** — name where the evidence and the self-assessment agree, where they diverge, and what the divergence may be evidence of. Family voice is integrated as additional context, especially for home-context demonstrations of the skill.
6. **For each durable skill, compare to the prior rating (where available)** — report the trajectory and the artifact-evidence for the trajectory. Hold, improved, declined, or mixed-by-sub-construct; cite the artifact dates that anchor the trajectory claim.
7. **For each durable skill, compare to the teacher's working hypothesis (where available)** — name agreement, divergence, and what the divergence may be evidence of.
8. **For each durable skill, name the scope honestly** — the genres, contexts, and artifact types the evidence comes from; the genres, contexts, and artifact types the evidence does not cover; the resulting scope-limitations the rating is subject to.
9. **Produce the per-skill evidence brief** — a structured section per skill containing: rubric level rating in district language, artifact evidence with dated citations, evidence gaps and next-window priorities, student-voice integration, family-voice integration, trajectory vs. prior rating, comparison to teacher working hypothesis, scope honesty.
10. **Produce the cross-skill summary** — patterns visible across multiple skills (e.g., "Maya's artifacts show consistent strength in oral and small-group contexts and developing performance in written-individual contexts; the pattern suggests that the durable-skills profile is genre-context-sensitive and may shift as the reporting window broadens to include more written-individual artifacts"). The cross-skill summary is short — 3-5 sentences — and serves as the executive read for the portfolio-defense audience.
11. **Produce the student-led-conference talking points** — 3-5 talking points the student can use to lead a conference about their durable-skills growth, anchored in the evidence the synthesis surfaced. The talking points are evidence-anchored and use the student's own first-person voice frame, not third-person teacher-narrative voice.
12. **Produce the next-window artifact-collection plan** — the artifact types, contexts, and dates the teacher and student should target to address the evidence gaps surfaced for each skill.

## Output Requirements

- **Header block:** student pseudonym or ID, grade level, reporting window dates, district Portrait of a Graduate framework name, synthesis run date, **bold watermark: "DRAFT — For Teacher Review — Anchor for Student-Led Conference and Portfolio Defense"**
- **Artifact catalog** — table or list of every artifact: ID, date, type, academic context, one-line summary
- **Per-skill evidence brief** (one section per durable skill the district has named) — each section includes:
  - Rubric level rating in district language (verbatim level descriptor)
  - Artifact evidence (each evidence claim cites artifact ID + date + specific move / quote / product feature)
  - Evidence gaps and next-window artifact-collection priorities
  - Student-voice integration (where self-assessment agrees with evidence, where it diverges)
  - Family-voice integration (where provided)
  - Trajectory vs. prior rating (where available), with artifact dates anchoring the trajectory
  - Comparison to teacher working hypothesis (where provided), with the gap surfaced honestly
  - Scope honesty (genres / contexts / artifact types the evidence covers and does not cover)
- **Cross-skill summary** — 3-5 sentences of patterns visible across multiple skills, suitable for the portfolio-defense executive read
- **Student-led-conference talking points** — 3-5 evidence-anchored first-person talking points the student can use
- **Next-window artifact-collection plan** — the artifact types, contexts, and dates the teacher and student should target to fill the evidence gaps
- **AI-use disclosure block** — explicit text: "This durable-skills synthesis was drafted with AI assistance for the teacher's review and use as a portfolio-defense anchor. The teacher is the human author of the final ratings; the student-led conference and portfolio defense are conducted by the student and the teacher, not the AI. Each rating is anchored in artifact evidence the teacher provided and cited back to those artifacts. Edit history is preserved."
- **Confidentiality footer** — naming the intended audience (student, family, advisor, transcript office, portfolio committee, graduation committee) and the district's portfolio or transcript-of-skills retention policy
- **Tone:** evidence-anchored, growth-oriented, student-centered, scope-honest, district-rubric-fidelity, no fixed-trait framings, no peer comparisons
- **Length:** typically 4-8 pages depending on the count of durable skills the district has named (3-8 skills typical) and the artifact density per skill
- **Save location:** `outputs/durable-skills-evidence/[pseudonym]-[reporting-window]-[YYYY-MM-DD].md` if the teacher confirms

## Pairs With

- **Rubric Generator** — used upstream to build or refine the district's durable-skills rubric; this skill consumes the rubric as input
- **Student Progress Report Writer** — narrative academic progress reporting from gradebook data; the durable-skills synthesis is a parallel competency-layer report, not a substitute
- **Student Feedback Generator** — generates per-artifact formative feedback; this synthesis aggregates across artifacts into a rubric-anchored progress brief
- **Parent-Teacher Conference Prep Generator** — uses the cross-skill summary and the student-led-conference talking points as inputs for the conference brief
- **Writing Conference Prep Generator** — used for the writing-genre-specific conferring conversations that often produce the artifact evidence the synthesis aggregates

## Anti-Plagiarism Note

No district Portrait of a Graduate rubric language, ETS / Carnegie Learning pilot framework text, Battelle for Kids framework language, NC DPI rubric language, CASEL competency text, P21 4Cs framing text, OECD 2030 transformative competencies language, or EdWeek Market Brief article text is copied verbatim into the output. The district's rubric language used in the output is the language the district provided as input. Framework references are factual attributions to the named framework, not copied text.

## Example Output

> **DRAFT — For Teacher Review — Anchor for Student-Led Conference and Portfolio Defense**
>
> **Student:** Student J (pseudonym) | **Grade:** 7 | **Reporting window:** 2026-03-02 to 2026-05-08 (Q4 progress window, 10 weeks)
> **District Portrait of a Graduate framework (from config):** Riverbend Unified PoG v3.2 (Battelle for Kids–anchored, district-adapted) — 5 durable skills: Critical Thinking, Communication, Collaboration, Adaptability, Personal Responsibility
> **Rubric level labels (from config):** Emerging / Developing / Proficient / Advanced
> **District grade-band:** 6–8 (grade-band rubric descriptors loaded from config)
> **ePortfolio platform (from config):** Mastery Portfolio (district-licensed)
> **Advisor:** Mr. Diaz (7th-grade humanities + advisory)
> **Synthesis run date:** 2026-05-12
>
> ---
>
> **Artifact catalog**
>
> | ID | Date | Type | Academic context | One-line summary |
> |---|---|---|---|---|
> | A1 | 2026-03-04 | Project deliverable | Humanities — "Local History" research paper draft 1 | 6-paragraph draft on Riverbend's 1965 school-integration timeline; one cited primary source, two secondary |
> | A2 | 2026-03-11 | Peer-feedback record | Humanities — peer review of A1 | Student J's feedback to a peer named two structural issues and one strength; received feedback noting source-evaluation gap |
> | A3 | 2026-03-18 | Project deliverable | Humanities — "Local History" research paper draft 2 | Revision incorporates peer feedback; adds a counterargument paragraph; cites a new primary source |
> | A4 | 2026-03-25 | Oral-defense notes | Humanities — paper defense in small group | Student J defended source choices when challenged by a peer; conceded one point; reframed another |
> | A5 | 2026-04-01 | Collaboration self-assessment | Humanities — end-of-project reflection | Student J rates own collaboration as "Developing"; names difficulty with disagreement |
> | A6 | 2026-04-08 | Project deliverable | Science — group lab report on watershed ecology | Student J authored the methods + data sections; group co-authored discussion |
> | A7 | 2026-04-15 | Teacher observation note | Science — group lab process observation | Group hit conflict over data-interpretation; Student J named the conflict aloud and proposed a process for resolving it |
> | A8 | 2026-04-22 | Conferring record | Humanities — research-skills conference | Student J identified own next learning edge as "evaluating sources I disagree with"; named one source they had dismissed without evaluation |
> | A9 | 2026-04-29 | Exit ticket | Humanities — unit-close reflection | Student J named one thing they would do differently in the next research project and why |
> | A10 | 2026-05-06 | Presentation deck | Humanities — research-paper presentation | 6-slide deck; clear thesis; one slide of counterargument; audience Q&A handled directly, including one question Student J did not know and named the unknown |
>
> ---
>
> **Per-skill evidence brief**
>
> ---
>
> ### Critical Thinking
>
> **Rubric level rating (district language, verbatim from config):** **Proficient**
> *Proficient-level descriptor for grade 6–8 Critical Thinking (Riverbend PoG v3.2): "The student evaluates sources for credibility and relevance, distinguishes claim from evidence, considers counterarguments, and revises thinking when warranted by new evidence."*
>
> **Artifact evidence:**
> - **A3 (2026-03-18)** adds a counterargument paragraph not present in A1 (2026-03-04). Specific move: Student J introduces a counterclaim about the role of state-level versus district-level decision-making in the 1965 integration timeline, names the strongest version of the opposing view, and then responds with primary-source evidence. *Distinguishes claim from evidence; considers counterarguments — aligned to Proficient descriptor.*
> - **A4 (2026-03-25)** oral-defense notes: when challenged on a source's reliability, Student J defended the source choice with specific cited evidence, then conceded a separate point about the secondary source's date being post-event commentary rather than contemporary record. *Evaluates sources for credibility; revises thinking when warranted by new evidence — aligned to Proficient descriptor.*
> - **A8 (2026-04-22)** conferring record: Student J self-identified the next learning edge as evaluating sources from disagreed-with perspectives, naming a specific source dismissed without evaluation. *Meta-awareness of source-evaluation discipline; evidence the descriptor is internalized, not just performed.*
>
> **Evidence gaps:** No artifact in this window evidences Critical Thinking outside written or oral-academic contexts (e.g., applied / civic / problem-solving contexts). The Advanced-level descriptor calls for "transfer of critical-evaluation moves across two or more domains"; the artifact set is humanities-heavy. Next-window collection: pair a science-investigation artifact and a current-events / civic-engagement artifact to evidence transfer.
>
> **Student-voice integration:** Student J's reflection in A9 names "I would do more source evaluation up front instead of after I'd already written" — agrees with the evidence; reinforces the rating.
>
> **Family-voice integration:** *Not provided this reporting window. Recommend collecting at the spring family conference (2026-05-22).*
>
> **Trajectory vs. prior rating (Q3 rating from config-loaded prior history: Developing):** Improved. Q3 evidence (not in this artifact set; cited from prior rating notes) showed Student J could state a counterargument but did not respond to one in writing. Q4 evidence (A3, A4) shows both stating and responding. *Trajectory: Developing → Proficient.*
>
> **Comparison to teacher's working hypothesis (Mr. Diaz, pre-synthesis: "Proficient — maybe Advanced on a good day"):** Agrees on Proficient. Does not yet support Advanced — the cross-domain transfer evidence is not present in this artifact set. Recommend Mr. Diaz hold at Proficient with the gap noted, and target cross-domain artifact collection for Q1 of next year.
>
> **Scope honesty:** Rating is anchored in humanities-genre artifacts (research paper, defense, conference, presentation) and one science-genre artifact (lab report). Does not speak to applied / civic / problem-solving contexts.
>
> ---
>
> ### Communication
>
> **Rubric level rating (district language, verbatim):** **Proficient**
> *Proficient-level descriptor for grade 6–8 Communication (Riverbend PoG v3.2): "The student communicates ideas with appropriate audience awareness across two or more genres, organizes ideas clearly, and adjusts language for purpose and audience."*
>
> **Artifact evidence:**
> - **A3 (2026-03-18) — written:** clear thesis, organized paragraph structure, appropriate academic register for the assignment. *Organizes ideas clearly in written genre — aligned to Proficient descriptor.*
> - **A4 (2026-03-25) — oral:** defended position in small-group academic conversation; adjusted to audience by paraphrasing technical claim when peer signaled non-understanding. *Adjusts language for purpose and audience — aligned to Proficient descriptor.*
> - **A10 (2026-05-06) — multi-modal:** presentation deck combines visual + verbal communication; Q&A handled directly, including the "I don't know" moment (named the unknown aloud rather than fabricating an answer). *Audience awareness across two or more genres — aligned to Proficient descriptor.*
>
> **Evidence gaps:** No artifact in this window evidences Communication in informal / peer-relational / family contexts. The Advanced descriptor calls for "communicates effectively across formal and informal registers"; the artifact set is formal-academic. Next-window collection: a peer-to-peer collaboration artifact or a student-led conference recording.
>
> **Student-voice integration:** Student J's A5 reflection rates own communication as "strong in writing, OK in speaking" — agrees with the evidence; reinforces the rating.
>
> **Family-voice integration:** *Not provided this reporting window.*
>
> **Trajectory vs. prior rating (Q3 rating: Developing):** Improved. Q3 had no multi-modal artifact; Q4 adds A10 (presentation) and A4 (defense). *Trajectory: Developing → Proficient.*
>
> **Comparison to teacher's working hypothesis (Mr. Diaz, pre-synthesis: "Proficient in writing, Developing in speaking"):** Evidence supports Proficient in both — the speaking artifacts (A4, A10) demonstrate the descriptor. Recommend Mr. Diaz revise the working hypothesis to Proficient overall with a note that speaking confidence is a continued growth area.
>
> **Scope honesty:** Rating is anchored in formal-academic genres. Does not speak to informal-peer or family-context communication.
>
> ---
>
> ### Collaboration
>
> **Rubric level rating (district language, verbatim):** **Developing**
> *Developing-level descriptor for grade 6–8 Collaboration (Riverbend PoG v3.2): "The student contributes to group work, listens to peer ideas, and follows through on assigned roles."*
> *Proficient-level descriptor (the next tier up, not yet evidenced consistently): "The student facilitates productive disagreement, names group-process issues constructively, and adjusts contribution to group needs."*
>
> **Artifact evidence (Developing):**
> - **A6 (2026-04-08):** Student J authored the methods + data sections of the group lab report; followed through on the assigned role. *Contributes to group work, follows through on assigned roles — aligned to Developing descriptor.*
> - **A2 (2026-03-11):** Peer-feedback record shows Student J gave specific peer feedback (named two structural issues, one strength). *Listens to peer ideas, contributes constructively — aligned to Developing descriptor.*
>
> **Artifact evidence approaching Proficient (one instance, not yet consistent):**
> - **A7 (2026-04-15):** During the science group lab process, when the group hit conflict over data interpretation, Student J named the conflict aloud and proposed a process for resolving it. *This is a Proficient-level move (facilitates productive disagreement, names group-process issues constructively). A single instance is not yet "consistent evidence" — the rating remains Developing, with the Proficient move documented as the leading edge.*
>
> **Evidence gaps:** Need multiple instances of process-naming, disagreement-facilitation, or contribution-adjustment to move to Proficient. Next-window collection: target two or more collaborative-project artifacts with explicit group-process observation; consider asking Student J to keep a brief collaboration-process journal during Q1 to surface process moves the teacher does not directly observe.
>
> **Student-voice integration:** Student J's A5 self-assessment rates own collaboration as "Developing" and names difficulty with disagreement specifically. Agrees with the evidence. *Divergence: Student J rates lower than the leading-edge evidence (A7) suggests; the student may not yet recognize the process-naming move in A7 as a Proficient move. Recommend Mr. Diaz surface A7 explicitly in the student-led conference to mirror back what the student did.*
>
> **Family-voice integration:** *Not provided this reporting window.*
>
> **Trajectory vs. prior rating (Q3 rating: Developing):** Held at Developing. The Proficient-level move in A7 is a leading-edge signal but does not yet meet the consistency threshold. *Trajectory: held; leading-edge documented.*
>
> **Comparison to teacher's working hypothesis (Mr. Diaz, pre-synthesis: "Developing"):** Agrees. Note the leading-edge A7 move for the student-led conference.
>
> **Scope honesty:** Rating is anchored in academic-collaborative contexts (paper-revision peer review, science group lab). Does not speak to athletic, club, advisory, or community-collaborative contexts.
>
> ---
>
> ### Adaptability
>
> **Rubric level rating (district language, verbatim):** **Developing**
> *Developing-level descriptor for grade 6–8 Adaptability (Riverbend PoG v3.2): "The student adjusts approach when initial strategy is not working, accepts feedback, and revises work in response."*
>
> **Artifact evidence:**
> - **A1 → A3 (2026-03-04 → 2026-03-18):** Substantial revision between drafts; incorporates peer feedback from A2; adds counterargument paragraph. *Accepts feedback, revises work in response — aligned to Developing descriptor.*
> - **A8 (2026-04-22):** Conferring record names a self-identified next learning edge that is a strategy adjustment ("evaluating sources I disagree with"). *Adjusts approach when initial strategy is not working — leading-edge toward Developing-to-Proficient.*
>
> **Evidence gaps:** No artifact in this window evidences adaptability under genuine unexpected disruption (schedule change, assignment-format change, unexpected partner). The Proficient descriptor calls for "adjusts to unexpected changes in plan or context"; this window provides only iterative-revision evidence, which is a weaker form of adaptability than disruption-response. Next-window collection: an artifact from an unanticipated situation — a substitute-teacher week, a project pivot, a partner change — would surface the disruption-response form.
>
> **Student-voice integration:** Student J's A9 exit ticket names "I would do more source evaluation up front" — agrees with the iterative-revision evidence; does not address disruption-response (no such situation in this window).
>
> **Family-voice integration:** *Not provided this reporting window.*
>
> **Trajectory vs. prior rating (Q3 rating: Emerging):** Improved. Q3 evidence (from prior notes) showed reluctance to revise; Q4 evidence (A1 → A3) shows substantial revision in response to feedback. *Trajectory: Emerging → Developing.*
>
> **Comparison to teacher's working hypothesis (Mr. Diaz, pre-synthesis: "Developing"):** Agrees.
>
> **Scope honesty:** Rating is anchored in iterative-revision evidence within scheduled academic work. Does not speak to disruption-response.
>
> ---
>
> ### Personal Responsibility
>
> **Rubric level rating (district language, verbatim):** **Proficient**
> *Proficient-level descriptor for grade 6–8 Personal Responsibility (Riverbend PoG v3.2): "The student manages own time and work, meets deadlines, owns mistakes, and identifies own next steps."*
>
> **Artifact evidence:**
> - **A3 (2026-03-18):** Submitted on the deadline. *Meets deadlines — aligned to Proficient descriptor.*
> - **A8 (2026-04-22):** Self-identified next learning edge in conferring — names a specific source dismissed without evaluation. *Owns mistakes, identifies own next steps — aligned to Proficient descriptor.*
> - **A10 (2026-05-06):** During the Q&A, named the unknown aloud rather than fabricating an answer. *Owns mistakes — aligned to Proficient descriptor.*
> - **A6 (2026-04-08):** Authored methods + data sections on time and to spec in the group context. *Manages own time and work — aligned to Proficient descriptor.*
>
> **Evidence gaps:** No artifact in this window evidences Personal Responsibility outside academic contexts (e.g., advisory commitments, school-job follow-through, community-role artifacts). The Advanced descriptor calls for "transfers responsibility-taking across academic and non-academic contexts"; the artifact set is academic. Next-window collection: an advisory-role artifact or a school-community-role artifact would broaden the scope.
>
> **Student-voice integration:** Student J's A5 self-assessment rates own personal responsibility as "Proficient" — agrees with the evidence.
>
> **Family-voice integration:** *Not provided this reporting window.*
>
> **Trajectory vs. prior rating (Q3 rating: Proficient):** Held at Proficient. *Trajectory: held.*
>
> **Comparison to teacher's working hypothesis (Mr. Diaz, pre-synthesis: "Proficient"):** Agrees.
>
> **Scope honesty:** Rating is anchored in academic-context artifacts. Does not speak to non-academic contexts.
>
> ---
>
> **Cross-skill summary** *(3–5 sentences, executive read for portfolio-defense audience)*
>
> Student J's Q4 artifact set shows consistent strength in formal-academic genres — written research, oral defense, multi-modal presentation — with Critical Thinking and Communication advancing to Proficient and Personal Responsibility holding at Proficient. Collaboration and Adaptability hold at Developing, each with leading-edge evidence (A7 process-naming for Collaboration; A8 self-identified strategy adjustment for Adaptability) that suggests the Proficient move is being practiced but not yet consistently. The cross-skill pattern: Student J's strongest evidence is in individual / formal-academic contexts; the artifact set under-evidences group-process and disruption-response situations, and does not yet evidence transfer across academic and non-academic domains. The next-window artifact-collection plan targets exactly those gaps. The portfolio-defense read: Student J is on a steady upward trajectory across all five durable skills, with the leading edges clearly visible and the gaps clearly named.
>
> ---
>
> **Student-led-conference talking points** *(3–5 evidence-anchored, first-person)*
>
> 1. "On the local-history paper, I added a counterargument in draft 2 that wasn't in draft 1. I think that's an example of evaluating sources from a perspective I disagreed with — a thing I named as my next learning edge in our conference."
> 2. "During my paper defense, I conceded a point about the secondary source's date — I think that's me revising my thinking when new evidence comes up, which is the Proficient descriptor for Critical Thinking."
> 3. "On the science lab, when the group disagreed about the data, I named the disagreement out loud and suggested a process for resolving it. I think that's a Proficient move for Collaboration, and I want to keep practicing it so it shows up more than once."
> 4. "I'm rating my collaboration as Developing because the process-naming move in A7 was one time, not consistent. My goal for next quarter is to do it at least three times across two different group projects."
> 5. "In my presentation Q&A, I said 'I don't know' to a question instead of guessing. I think that's owning a gap, and it's the Personal Responsibility descriptor."
>
> ---
>
> **Next-window artifact-collection plan** *(Q1 2026-27)*
>
> | Skill | Artifact type to target | Context to target | Target dates |
> |---|---|---|---|
> | Critical Thinking | Civic / current-events analysis artifact | Outside humanities (advisory, science investigation, math problem-solving) | Q1 Week 4–6 |
> | Communication | Student-led-conference recording or informal-peer collaboration artifact | Informal register; peer-relational context | Q1 Week 6 (advisory conference cycle) |
> | Collaboration | Two or more group-project artifacts with explicit group-process observation; brief student-kept collaboration-process journal | Multiple group contexts; varied partners | Q1 ongoing |
> | Adaptability | An artifact from an unanticipated situation (sub week, project pivot, partner change) | Disruption-response context | Whenever it occurs; flag for collection |
> | Personal Responsibility | An advisory-role artifact or school-community-role artifact | Non-academic context | Q1 Week 8 (advisory mid-quarter check) |
>
> ---
>
> **AI-use disclosure block**
>
> This durable-skills synthesis was drafted with AI assistance for the teacher's review and use as a portfolio-defense anchor. The teacher (Mr. Diaz) is the human author of the final ratings; the student-led conference and portfolio defense are conducted by the student and the teacher, not the AI. Each rating is anchored in artifact evidence the teacher provided and cited back to those artifacts. Edit history is preserved in the teacher's working file.
>
> ---
>
> **Confidentiality footer**
>
> Intended audience: Student J, family (Spanish translation routed through Lenguaje Verde via FACE office per config), advisor (Mr. Diaz), portfolio committee (humanities + science teachers, advisor, Mastery Portfolio platform lead). Retention: working file held under district portfolio-evidence retention policy (from config); synthesis posted to Mastery Portfolio under Student J's Q4 PoG progress entry; raw artifact files retained in the platform for the duration of the student's enrollment per the district's transcript-of-skills policy (from config).
