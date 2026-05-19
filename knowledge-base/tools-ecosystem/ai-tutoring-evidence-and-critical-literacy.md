# AI Tutoring Evidence Base, Critical AI Literacy, and 2026 District Governance Signals

Snapshot as of 2026-05-11 (updated from 2026-04-28). This file complements the prior tools-ecosystem files (`ai-feedback-and-grading.md`, `curriculum-mapping-tools.md`, `formative-assessment-and-differentiation-tools.md`, `sub-plans-observation-and-plc-tools.md`, `ai-funding-policy-and-agentic-tools.md`) by capturing four threads that have crystallized in the 2026-04-26 → 2026-04-28 window: empirical RCT evidence on AI tutoring outcomes, the emerging distinction between AI literacy and critical AI literacy, district-level governance moves and cost stories that are reshaping how superintendents are sequencing AI rollout, and — added 2026-04-28 — the LAK26-presented finding on the in-classroom equity gap that opens up when teachers are running AI-tutoring blocks.

## AI Tutoring — RCT Evidence and What It Means for Skill Design

The 2025–2026 evidence base on AI tutoring has moved past anecdote into randomized-controlled-trial territory, and the early signal is strong. Two trials in particular have shaped 2026 district-side conversations:

- A Harvard randomized controlled trial published in mid-2025 measured undergraduate physics learning under three conditions: traditional active-learning lecture, AI tutor only, and AI tutor with embedded research-based design (worked examples, retrieval practice, spaced retrieval, scaffolded fading). The AI-tutor-with-research-based-design condition produced learning effects of 0.73 to 1.3 standard deviations over the active-learning baseline, with the AI group spending less time on task (median ~49 minutes vs. ~60 minutes in-class).
- A Google / Eedi Labs RCT involving 165 British secondary students aged 13–15 paired AI-drafted tutor messages with a human-tutor reviewer who could revise before sending. The supervised-AI condition outperformed pure-human-tutoring on transfer items (~66% vs. ~61% on subsequent topic problems), at substantially lower cost-per-student-hour.

Several practitioner-relevant patterns recur across the AI-tutoring research corpus:

- The strongest effects are observed when the AI tutor uses Socratic questioning rather than answer-explaining. This validates the design choices in the Socratic Tutor Prompt Builder skill (question-pattern repertoire, misconception branches, adaptive scaffolding, reflective pauses, give-the-answer escape hatch).
- Human oversight remains a load-bearing component. The "AI-only" condition consistently underperforms the "AI + human review at structured intervals" condition. The teacher-review summary at the end of every Socratic Tutor Prompt Builder output, and the transcript-review cadence built into the deployment companion, sit on this evidence.
- The cost-per-effective-tutor-hour is the single largest driver of district interest in 2026. With high-dose tutoring at ~$2,000–4,000 per student per year out of reach for most districts, the supervised-AI pattern at ~10–20% of that cost is the pragmatic on-ramp.

The implication for the skills repo: AI-tutor design skills (Socratic Tutor Prompt Builder, future small-group AI-tutor protocols) sit on a strengthening evidence base, not on demo-day enthusiasm.

## In-Classroom Attention Equity in AI-Tutoring Blocks — 2026-04-28 Update

A study from NC State, presented at LAK26 (the Annual Learning Analytics & Knowledge Conference, Bergen, April 27 – May 1, 2026) and titled in the published proceedings as a session-by-session analysis of teacher interventions in K-12 classrooms, surfaces an equity pattern that intuition alone does not catch:

- The analysis covered ~1.4M student-system interactions across 339 students in 14 middle and high school math classes across 10 U.S. schools during 2022-23, all using an intelligent tutoring system.
- Teacher help in these classrooms is "sticky" — students who received a teacher touch in one session were significantly more likely to receive additional teacher touches in subsequent sessions, even after controlling for current engagement state.
- The mirror finding: students who were idle or struggling but had not yet been visited tended to remain unvisited. Idle behavior alone did not draw sustained teacher attention over time.
- The learning effects of teacher help were largely session-bound — the teacher touch helped that session's task but did not produce a measurable cross-session transfer of the same magnitude as the recurrence of attention. The gap between attention-recurrence and learning-transfer is what the authors describe as "sticky help, bounded effects."

What the finding does and does not mean:

- The finding is not that teachers are biased in a hostile sense; it is that human attention allocation under cognitive load defaults to the students the teacher has already built a working relationship with — the path of least friction. The AI-tutoring block is a high-cognitive-load environment for the teacher (multiple students at multiple platforms working at multiple paces), which makes the default-to-the-familiar pattern stronger.
- The finding is also not that AI tutoring is the cause of the equity gap. Sticky-attention patterns predate AI tutoring. What the AI-tutoring environment does is make the pattern measurable at session-level granularity for the first time, because every student-system interaction is logged.
- The fix the authors describe is real-time analytics that surface attention-coverage gaps to the teacher mid-block — a dashboard view that highlights under-visited students and prompts the teacher to redistribute attention. Most 2026 AI-tutor platforms do not yet provide this view; the dashboards are student-progress-focused rather than teacher-attention-focused.

Practitioner heuristics surfacing from the finding:

- The teacher's mental model of "who needs help today" is biased toward the students who have already received help. A periodic audit against the roster — not against the teacher's mental model — is the corrective. The audit can be light (a 30-second-per-session log of touches) and still produce a useful trend signal across a 10-day window.
- Naming a fairness frame in advance (equal-time / proportional-to-need / floor-then-need) changes how the same data reads. Without a named frame, equity findings drift toward whatever the teacher's mood is on the audit day. The frame the teacher names becomes the lens; the data becomes interpretable.
- Coverage and quality are different questions. A teacher who reaches every student with a low-cognitive-demand check-in has not done better than a teacher who reaches eight students with high-leverage transferable moves. The Teacher Attention Equity Auditor measures coverage; the Classroom Observation Feedback Generator and a coach's interaction-quality observation measure quality. The pair is the durable check.
- Subgroup disaggregation is descriptive, not prescriptive. Surfacing that EL students or 504 students or below-benchmark students have averaged less attention in the window is a prompt to investigate the cause, not a directive to target the group with more attention decoupled from need. The teacher's professional judgment, not the audit, decides what to change.

The Teacher Attention Equity Auditor skill is the repo's response — a teacher-side, prompt-driven equivalent of the dashboard view the LAK26 paper recommends, designed to run weekly or biweekly across the whole roster. Distinct from the existing PLC Agenda & Data Protocol Builder (team-level grade or department data), the IEP Goal Progress Tracker (longitudinal goal data on identified students), and the Writing Conference Prep Generator (next-conference plan for one student): the auditor is the routine in-classroom equity checkpoint that runs across the whole roster.

## AI Literacy vs. Critical AI Literacy — The 2026 Framework Convergence

A distinction has emerged in 2026 that is reshaping how districts and schools sequence AI literacy work:

- **AI literacy** answers the question "how do I use this tool effectively?" — covering technical foundations, prompt design, capabilities, limitations, ethical use basics. This is where most district AI literacy curricula started in 2024–2025.
- **Critical AI literacy** answers a different question: "what does this tool do to people, knowledge, and power?" Critical AI literacy treats AI not as an instrument but as a system embedded in social, economic, and political relations. The classroom move shifts from instrumental ("does this answer look right?") to systemic ("who benefits and who is harmed if AI is used this way, at this scale, by people in roles like mine?").

The April 2026 frameworks landscape reflects this convergence:

- A six-domain critical-AI-literacy question framework — output evaluation, bias awareness, thinking ownership, system understanding, ethical awareness, strategic use — is circulating widely in 2026. Teachers are using the questions as pre-task framing, mid-task journal prompts, rubric criteria, exit tickets, and conferring questions, with the explicit aim of making the questions automatic over time.
- The OECD-EC AI Literacy Framework for Primary and Secondary Education organizes 22 competencies across four domains — Engage with AI, Create with AI, Manage AI, Design AI. Critical-thinking and human-centered competencies are present in every domain, not isolated to an "ethics" strand.
- The Open University's framework for the learning and teaching of critical AI literacy skills has become a frequently-cited reference for higher-ed and AP-level curriculum design.
- UNESCO's two competency frameworks (Teachers, Students) remain the most-cited cross-jurisdictional reference (see the prior tools-ecosystem file). Critical engagement is one of the named competencies in both.

Practitioner heuristics surfacing from district pilots:

- Pick two or three critical-AI-literacy questions per task, rather than running the full 24 every time. The questions become inert if oversaturated.
- Build the questions into rubrics, not just discussion. A rubric criterion that requires the student to point to a specific output, identify a specific pattern, and propose a specific cause is observable; a "the student is critically aware" criterion is not.
- Critical-AI-literacy questions work in K–postsecondary, but the wording, examples, and abstraction level shift sharply. K–2: "Did the computer get this right? How do you know?" 9–12: "If this tool were used at scale by teachers grading papers, who would be advantaged and who disadvantaged, and why?"

The Critical AI Inquiry Prompt Builder skill is the repo's response to this convergence: a reusable, embeddable inquiry set anchored in the six-domain framework, calibrated to grade band and AI-use posture, embedded in rubrics and conferring rather than running as a standalone discussion.

## Vocabulary Instruction Meta-Analytic Signal

A 2026 meta-analysis on AI-assisted vocabulary teaching aggregated effects across L1 and L2 contexts, age bands, and word-tier targets. Headline findings:

- AI-assisted vocabulary teaching produces moderate-to-large effects in L2 contexts at all educational levels except preschool, with the largest effects in middle and secondary grades.
- The effect size is substantially larger when the teacher is the process facilitator (selecting words, sequencing exposures, monitoring transfer) than when the AI tool acts as the primary instructor. This is the same human-in-the-loop pattern surfaced in the AI-tutoring RCT corpus.
- The exposures-required threshold for retention has not moved: 6–10 distinct exposures across modalities (read, hear, speak, write) remain the threshold for a Tier 2 academic word to enter usable vocabulary.

Observed gap in 2026 AI vocabulary tools: most generators produce a list and a definition, but stop short of the robust-vocabulary criteria for word selection (Beck / McKeown / Kucan), the multiple-exposures-across-modalities pattern, and the WIDA-banded scaffolding ELLs need. The Academic Vocabulary Builder skill is the repo's response: source-anchored word selection, student-friendly definitions, multiple-modality exposures, Bloom-tagged practice tasks, WIDA-banded scaffolds with cognate bridges, re-exposure plan across the unit runway.

## Writing Workshop and Conferring — Persistent Gap in AI Tools

Most 2026 AI feedback tools (Brisk, Knowt, TeachQuill, CK-12, StudyFetch, Snorkl, Report Card Wizard) generate written feedback that goes back on the artifact for the student to read after the fact. The conferring conversation — the live, 5–7-minute teacher-student talk that is the foundational instructional move in the writing-workshop tradition (Calkins, Atwell, Anderson, Newkirk, Graves, NWP) — is largely absent from the AI tooling landscape.

Practitioner-side reasons this matters:

- The conferring move that transfers across drafts is more durable than any single piece of corrective feedback on a single draft. The teacher who runs five 5-minute conferences per writing block over a week reaches every writer with a transferable teaching point; the teacher who writes three rounds of detailed comments per draft reaches each writer with a draft-specific fix.
- Conferring requires a different artifact than written feedback: a research–decide–teach–link script, one teaching point (not three), a mentor-text exemplar, an in-conference try-it, a take-away question for self-conferencing, and a 2–3-line conferring-log note for the next session.
- The hold-the-pen rule (the teacher does not write on the student's draft during conferring) is a workshop-model fundamental that most AI tools' "feedback" output mode quietly violates.

The Writing Conference Prep Generator skill is the repo's response — a per-conference, not per-class, artifact designed for the workshop classroom, the AP Lang / college-comp revision conference, the ELL writing-conference rotation, and the IEP writing-goal individual conference. Distinct from the existing Student Feedback Generator (which produces written feedback for after-the-fact reading) and the Rubric Generator (which produces the scoring instrument).

## District Governance and Cost-Story Signals — April 2026

District-level moves visible in the April 2026 trade press are clarifying the operating model superintendents are landing on:

- **Charlotte-Mecklenburg Schools** surveyed the school community on AI tools, received ~10,000 responses, formed an AI governance team spanning instruction / assessment / technology / principal leadership, and launched a pilot in 30 of 185 schools before any district-wide rollout. The pattern is community-survey → cross-functional governance team → bounded pilot → measured scale-up, not pilot-then-pilot-then-pilot.
- **Indianapolis Public Schools** brought the technology leader into the superintendent's leadership table, treating AI as not-a-siloed-initiative. The org-design move (technology leader at the strategy table, not in the basement) is showing up in multiple urban districts in 2026.
- **Ohio's Department of Education and Workforce** released a model AI policy in late 2025 ahead of a state requirement that every public, community, and STEM school adopt an AI framework by **July 1, 2026**. The model template emphasizes data privacy and security alignment with FERPA and PII rules, academic-integrity guidance (including thresholds some districts adopt for AI content share in student work), and stakeholder engagement across leadership / teachers / students / families.
- **Peninsula School District (Washington)** documented up to ~$250,000 in projected ed-tech contract savings by the 2026-27 school year through "vibe coding" — using AI to build small, district-specific tools that replace several SaaS subscriptions previously covering single use cases. This is the first widely-cited cost-out story attached to district AI use; other districts are watching the pattern.
- **Anthropic + Teach For All** announced a global AI training initiative reaching 100,000+ educators across 63 countries, with a six-episode AI Fluency Learning Series, an ongoing Claude Connect community for educator peer-to-peer exchange, and a Claude Lab innovation track. Localized materials are appearing in Spanish, Hindi, and 30+ languages. This is the clearest example to date of the educator-network model for AI training (vs. district-by-district PD).

Practitioner heuristics surfacing from these signals:

- The community-survey → cross-functional-governance → bounded-pilot → measured-scale-up sequence is becoming the default district playbook, not the LMS-procurement-then-roll-it-out pattern that dominated the prior decade.
- Cross-functional governance includes not just technology but instruction, assessment, and principal leadership. Single-stakeholder governance underperforms.
- State-level deadlines (Ohio's July 1 2026 mandate is the visible leading edge; expect other states to follow) are pushing districts toward documented AI policies regardless of pilot maturity. Documented policy that travels with implementation is more durable than implementation-then-policy.
- Cost-out stories are starting to compete with cost-in stories for superintendent attention. The vibe-coding pattern (replace several SaaS subscriptions with small district-built tools) has surfaced as a budget-side AI argument for the first time.

## Teacher Professional Reflection and AI Coaching

Two 2026 patterns are converging in the teacher-professional-development space:

- **AI-mediated teacher reflection** — virtual coaches that watch a teacher's recorded video and prompt structured reflection (research-based reflection prompts, near-term goal setting, action planning, impact observation). The pre-service-teacher pilot evidence shows AI-dashboard-mediated reflection improves the depth and quality of reflection vs. unguided self-assessment.
- **AI in PLCs** — custom chatbots facilitating virtual PLCs across distance and across schools; the Novobo "AI mentee" model in which teachers train an AI together using gestures and voice (the act of teaching the AI externalizes tacit pedagogical knowledge that strengthens peer collaboration).

These patterns reinforce the existing repo skills (PLC Agenda & Data Protocol Builder, Classroom Observation Feedback Generator) and surface a backlog candidate for a future cycle: a Professional Reflection Prompt Generator that produces structured reflection prompts grounded in a specific lesson video / classroom artifact / coaching-cycle stage, distinct from the more transactional post-lesson PLC reflection prompt that the AI Literacy Lesson Plan Generator already includes.

## Skill-Repo Coverage Map — Post 2026-04-28

Skills as of this cycle (28 total):

- **Admin (7)** — Behavior Intervention Plan Drafter, Classroom Observation Feedback Generator, Education Grant Proposal Drafter, IEP Goal Progress Tracker, PLC Agenda & Data Protocol Builder, Restorative Conference Script Generator, Student Progress Report Writer
- **Customer Service (3)** — Classroom Newsletter Generator, Parent Communication Drafter, Parent-Teacher Conference Prep Generator
- **Operations (15)** — Academic Vocabulary Builder, AI Literacy Lesson Plan Generator, Assessment Question Writer, Critical AI Inquiry Prompt Builder, Curriculum Standards Aligner, Differentiation Planner, Exit Ticket Generator, Lesson Plan Builder, Rubric Generator, Socratic Tutor Prompt Builder, Student Feedback Generator, Substitute Lesson Plan Generator, Teacher Attention Equity Auditor *(new)*, Text Level Adjuster, Writing Conference Prep Generator
- **\_shared (3)** — Email Drafter, Meeting Summarizer, Review Responder

Knowledge-base ecosystem files (6):
- ai-feedback-and-grading.md
- ai-funding-policy-and-agentic-tools.md
- ai-tutoring-evidence-and-critical-literacy.md *(updated 2026-04-28 with LAK26 attention-equity finding)*
- curriculum-mapping-tools.md
- formative-assessment-and-differentiation-tools.md
- sub-plans-observation-and-plc-tools.md

## Open Coverage Gaps Carried to Backlog

- **IEP/504 Accommodation Recommender** (relevance 7 / novelty 7) — held since 2026-04-26 to let the evaluator land the post-2026-04-26 skills first
- **Discussion Question Generator** (7 / 6) — Bloom + DOK + Socratic-seminar opening / core / closing question pattern
- **Choice Board / HyperDoc Builder** (7 / 6) — UDL-aligned student-choice menus
- **Success Criteria / "I Can" Converter** (7 / 6) — objectives → student-friendly success criteria using ABCD method
- **Feedback Comment Bank Builder** (7 / 7) — reusable skill-tagged comment libraries trained on the teacher's voice
- **Professional Reflection Prompt Generator** (carried) — structured reflection prompts grounded in a specific lesson video / classroom artifact / coaching-cycle stage
- **Decodable Text / Phonics-Aligned Practice Generator** (7 / 7) — newly surfaced 2026-04-28; LETRS-aligned scope-and-sequence approach; distinct from Text Level Adjuster (which adjusts existing passages by Lexile/grade band, not phonics-pattern-aligned)
- **Math Misconception Diagnostic Summary Generator** (7 / 6) — surfaced 2026-04-28; pulls misconception clusters from class-wide quiz/exit-ticket/AI-tutor data; partial overlap with Assessment Question Writer's distractor design and Student Feedback Generator's per-student feedback
- **Course-Level AI Use Disclosure / Syllabus Block Generator** (7 / 6) — surfaced 2026-04-28; classroom or course-level disclosure language and "traffic-light" task-by-task AI permission grid; distinct from district-level AUP drafter
- Out of teacher-prompt repo scope but flagged: District AI Acceptable Use Policy Drafter (governance artifact, candidate for a SEA / LEA-policy track if one exists; Ohio's July 1 2026 mandate continues to add urgency); Knowledge Pack / RAG Curriculum Document Builder (platform configuration, candidate for repo-side or LEA-side track); Teacher AI-Coaching Reflection Companion (district-PD artifact, candidate for the same future track)

---

## OECD "Performance Without Learning" Signal + Agentic AI Course Completion + Google AI Educator Series — 2026-05-11 Update

### The OECD "Performance Without Learning" Finding (2026-01)

The OECD Digital Education Outlook 2026 (published January 2026; conference held May 2026) presents what is now the most-cited global policy finding on generative AI in education: GenAI can dramatically improve student performance on assessed tasks while simultaneously undermining the learning those tasks were designed to produce. The performance advantage tends to disappear — or even reverse — when AI access is removed, as in in-class exams.

The core OECD distinction is between two outcomes that 2024–2025 discourse frequently conflated:

- **Performance** — the quality of the assessed product the student submits; easily improved by AI assistance
- **Learning** — the durable cognitive change in the student; not reliably improved by AI-assisted performance, and potentially harmed if the AI is doing the cognitive work the learning target was designed to require

The OECD's policy-side conclusion is that AI supports learning when it is deployed with clear pedagogical purpose and design — and degrades it when it is used to outsource the cognitive work that constitutes the learning target. The implication is not that AI should be banned from classrooms; it is that assessment design must assume AI access and still require genuine student cognition.

OECD also reports that in 2024, 37% of lower secondary teachers globally reported using AI in their work (TALIS survey), and 72% expressed concerns about academic integrity — confirming that the design gap between performance and learning is already a lived practitioner concern, not only a research abstraction.

**Practitioner heuristic:** the OECD finding provides the research grounding for the AI-Present Assessment Redesigner skill (2026-05-11). The skill operationalizes the design question: "given that AI can improve the submitted product, how do we redesign the assignment so that the cognitive work constituting the learning target remains genuinely required of the student?" The audit, strategy menu, and rubric-criteria update steps in the skill respond directly to the OECD's pedagogical-purpose-and-design condition.

**CAQA parallel:** A related industry-education finding (CAQA Compliance, citing the OECD report) frames the same risk in vocational education terms: students who use AI to complete assessments are "performing without learning" — passing the assessment without building the competency. The signal travels across K-12, higher education, and vocational contexts.

### Agentic AI Course Completion — The "Einstein" Case (2026-02)

In February 2026, a 22-year-old developer (Advait Paliwal) launched a tool called Einstein capable of autonomously logging into Canvas, watching recorded lectures, completing assignments, and submitting homework — without the student engaging. Inside Higher Ed coverage (February 26, 2026) framed the question directly: agentic AI can complete whole courses — now what?

The Einstein case represents the logical extreme of the performance-without-learning dynamic: the performance (course completion) fully decoupled from the learning. The tool faced legal challenges, but its release accelerated faculty and institutional policy conversations about which course designs are most vulnerable to agentic completion and which are more durable.

Inside Higher Ed's coverage identified the most vulnerable assignment types: asynchronous quizzes, discussion board posts graded on participation (word count or submission presence, not content), take-home essays on generic topics, and problem sets with answer-key-recoverable solutions. The most agentic-completion-resistant designs share features that closely track the AI-Present Assessment Redesigner skill's strategy menu: process documentation, personal-context anchoring, in-class components, oral defense, and multi-stage feedback-response cycles.

**Practitioner heuristic:** the Einstein case is not primarily an academic integrity enforcement problem; it is an assessment design problem. Courses designed primarily around content-delivery-and-recall assessments are structurally vulnerable to agentic completion regardless of policy. The durable response is to redesign the assessment's center of gravity toward disciplinary judgment, personal context, and iterative human-feedback-response — work that agentic tools can approximate but cannot genuinely perform.

### Google AI Educator Series (Launch: 2026-05-13)

Google launched a free, comprehensive AI training program for all 6 million K-12 and higher-education educators in the US, in partnership with ISTE+ASCD. Key features:

- **Format:** short, non-sequential micro-trainings (K-12 sessions: 10–15 minutes; higher-ed: 30–45 minutes), broken into three tracks: Foundational Understanding, Pedagogical Applications, and Administrative Applications
- **Grade-level specificity:** K-12 Pedagogical Applications sessions are grade-level specific
- **Micro-credentials:** teachers earn badges on completion, suitable for PD documentation
- **Job-embedded design:** specifically structured to be completed during contracted hours (prep periods, lunch)
- **Recurring content:** starting September 2, 2026, new content released the first Wednesday of each month
- **Tools covered:** Gemini and NotebookLM integration with Google Classroom; AI-in-LMS workflows
- **New K-12 integration:** Gemini LTI support for Moodle (launching May 2026) brings Gemini and NotebookLM directly into Moodle's LMS environment alongside the existing Google Classroom integration

**Practitioner heuristic:** the Google AI Educator Series is the largest single US educator AI-training event of 2026-Q2, reaching the universe of educators who use Google Workspace for Education. The training's emphasis on pedagogical applications (not just technical how-to) aligns with the OECD finding's policy-side recommendation: AI supports learning when guided by clear teaching principles. Districts looking to fulfill ED Supplemental Priority AI-literacy professional development requirements should consider the Google AI Educator Series as a no-cost option. The AI Literacy Lesson Plan Generator skill in this repo can scaffold the discussion of these sessions during staff meetings or PD debriefs.

### Skill-Repo Coverage Map (post-2026-05-11 additions)

| 2026 Force | Repo Skill(s) That Respond |
|---|---|
| OECD "performance without learning" — assessment design response | **AI-Present Assessment Redesigner (NEW)**, Critical AI Inquiry Prompt Builder, AI Literacy Lesson Plan Generator |
| Agentic AI course completion (Einstein / Canvas) — assessment design response | **AI-Present Assessment Redesigner (NEW)** |
| End-of-year reporting cycle — comment bank efficiency | **Feedback Comment Bank Builder (NEW)**, Student Feedback Generator, Student Progress Report Writer |
| Google AI Educator Series (May 13, 2026) — PD scaffolding | AI Literacy Lesson Plan Generator |
| Gemini in Moodle / Google Classroom AI integration | AI Literacy Lesson Plan Generator (platform-calibration list updated) |

### Sources Behind the 2026-05-11 Update

OECD Digital Education Outlook 2026 (January 2026 publication; OECD conference May 2026; CAQA, EPALE, Digital Skills and Jobs Platform, CIDDL, and youthrex summaries); Inside Higher Ed "Agentic AI Can Complete Whole Courses. Now What?" (February 26, 2026; also covered by UPCEA, 8allocate, ScholarsJournal, edCircuit, IEEE Xplore Agentic AI in Education State of the Art, AIR Institutional Research); eSchoolNews / eCampusNews "The AI-resistant classroom is a myth: Designing assessments that assume AI is present" (March 2026); UMass Amherst CTL "How Do I Redesign Assignments and Assessments in an AI-Impacted World?"; monsha.ai "7 Strategies to AI-proof Assessment Design" and "30 Ideas and Examples for AI-resilient Assessments"; Digital Learning Institute "AI for Learning in 2026: Tools, Workflows, and Assessment"; Educators Technology "AI-Resistant Assessments: Practical Tips and Strategies for Teachers" (February 2026); Google blog "Google launches AI literacy training for 6 million US educators" and "From test prep to graduation, our latest AI tools support learners"; GovTech "Google, ISTE+ASCD Offer AI Training to All Teachers"; ISTE+ASCD announcement; Google Gemini in Moodle LTI announcement (May 2026); MagicSchool blog "AI Teaching Tools For Planning, Assessment & Feedback Updates 2026" (Knowledge feature: RAG over district-uploaded curriculum docs up to 50MB, Org Admin Enterprise accounts); Educators Technology MagicSchool AI Review (February 2026); Brisk Teaching 500k+ educator adoption data; Khanmigo NBER study early 2026 (34% greater learning gains vs. traditional tutoring); MagicSchool 5M+ educator platform data (80+ teacher-specific workflows; Knowledge feature grounding AI responses in district curriculum documents). All references are factual attributions; no verbatim text was copied into this knowledge-base file.

---

## Durable-Skills Assessment + Special-Education AI Adoption + District Build-vs-Buy + Anthropic Teacher Training Reach — 2026-05-18 Update

### The Durable-Skills Assessment Pilot Signal (2026-05)

The EdWeek Market Brief feature "Inside a Pilot Using AI to Rethink Assessment, Capture Students' Durable Skills" (May 2026) details ETS and Carnegie Learning's "Skills for the Future" initiative — a pilot that uses generative AI to assess student progress on durable skills (creativity, critical thinking, communication, collaboration) that traditional grading and standardized testing have struggled to measure. The pilot is one strand of a broader 2025-2026 wave: 20+ states' districts have adopted some form of Portrait of a Graduate framework (Battelle for Kids, North Carolina DPI, Virginia, Ohio, Texas, and others), and a parallel set of districts uses CASEL SEL competencies or the Mastery Transcript Consortium framework to similar ends. The market gap is consistent: districts have named the durable skills, teachers have produced artifacts that demonstrate them, but the synthesis step — pulling evidence across artifacts into a rubric-anchored progress narrative — has remained hand-done and inconsistently structured.

**Practitioner heuristic:** the durable-skills assessment signal grounds the Durable Skills Evidence Synthesizer skill (2026-05-18). The skill operationalizes the synthesis step: take a batch of dated student artifacts and the district's named Portrait of a Graduate rubric, and produce an evidence-anchored per-skill brief — every rating cites artifact evidence; ratings unsupported by artifact evidence are not produced; the synthesis stays within-student (no peer comparison) and growth-oriented (no fixed-trait framings). The skill consumes whichever framework the district has adopted as input, rather than substituting a generic durable-skills framing, so it works equally well for districts using Battelle for Kids, NC DPI, CASEL, Mastery Transcript, P21 4Cs, or the OECD 2030 transformative competencies.

### Special-Education AI Adoption: 57% in 2024-25 (CDT Survey)

The Center for Democracy & Technology's most recent special-education survey (covered in EdWeek's "Teachers Are Using AI to Help Write IEPs. Advocates Have Concerns," October 2025, with follow-on coverage in K-12 Dive and GovTech through Q2 2026) reports that 57% of special-education teachers used AI to help with IEPs or 504 plans in 2024-25 — up from 39% in 2023-24. 15% used AI to write IEPs or 504 plans in full (up from 8%). Use breakdowns: 31% use AI to identify trends in student progress for goal setting, 30% to summarize IEPs and 504 plans, and 28% to help choose accommodations. The CDT framework warns that an AI tool generating IEP/504 content from sparse student-specific input — without significant human review — likely fails the IDEA individualization requirement (34 CFR §300.320) and may introduce bias against the very students the IEP/504 process exists to protect. Tools in the space include Playground IEP, Flint K12's accommodation suggestion tool, Undivided's HIPAA-compliant IEP assistant, and several enterprise EdTech platforms (Frontline, SpedTrack, Embrace) integrating AI features.

**Practitioner heuristic:** the 57% adoption signal, combined with Ohio's July 1, 2026 mandate (now ~6 weeks out from this cycle date) and the CDT individualization warning, justifies converting the IEP/504 Accommodation Recommender from backlog (where it had been carried since 2026-04-26). The skill is designed as the inverse of the CDT failure mode: heavy input requirements (PLAAFP data + access barriers + state-assessment context + family/student voice + implementation history), mandatory team-review framing on every recommendation, source-attribution per recommendation (NCEO category / WIDA category / state manual category), explicit anti-bias checks against the four bias patterns documented in special-education AI literature (over-recommendation of behavioral controls for students of color; under-recommendation of acceleration for twice-exceptional students; gender bias in autism-related accommodations; language-load conflation with cognitive load for multilingual learners), no-PII floor, advisory-only frame (the output is never the IEP/504 plan, never enters the plan verbatim, and never is shared with families before team review), and IDEA-compliant AI-use disclosure language.

### District Build-vs-Buy: "Vibe Coding" Saves $200-250K (2026-05)

EdWeek ("A District Expects to Save $200K From AI-Powered 'Vibe Coding'. Here's How," May 2026) and K-12 Dive ("'Vibe coding' helped a Washington district save $250K in ed tech costs") detail Peninsula School District's strategy of using Claude Code and similar agentic coding tools to build internal apps, simulations, and operational tools — replacing some commercial ed-tech subscriptions and customizing open-source alternatives. The Peninsula CIO's portfolio includes LessonLens (a special-ed lesson-accessibility tool), choose-your-own-adventure historical simulations, accounting and HR utilities, and a customized open-source e-signature tool. The strategy reduces vendor lock-in, allows hyper-local customization, and shifts technology spending from license fees to staff capacity-building. The strategy generated significant interest at the Consortium for School Networking (CoSN) annual conference and is being explored by additional districts.

**Practitioner heuristic:** the vibe-coding district trend is structurally significant but largely **out of scope for a teacher-prompt skills repo** — the activity is district-CIO / IT-leadership work that requires technical capacity and policy guardrails (data privacy, accessibility, sustainability of internally-built tools) that exceed the teacher-prompt artifact's scope. The trend is logged here as KB context because it changes the question the repo answers: as more districts internalize EdTech development, the durable value of an open-source teacher-prompt skill library grows (the skills are portable across whatever stack the district builds), while the value of any single commercial AI tool's "teacher prompt library" diminishes. The repo's open-source positioning aligns well with the build-vs-buy shift. A future repo track for IT-leadership / CIO-level artifacts (data privacy review protocols, vendor procurement frameworks, internally-built-tool sustainability plans) is a candidate for the out-of-scope flag list.

### NC State LAK26 "Sticky Help, Bounded Effects" (2026-04) — Carried Reference

The April 2026 NC State / LAK26 paper ("Sticky Help, Bounded Effects: Session-by-Session Analytics of Teacher Interventions in K-12 Classrooms," Qiao Jin et al., NC State + Carnegie Mellon, to be presented at the 16th Annual Learning Analytics & Knowledge Conference) found that teachers using AI-powered tutoring systems tend to provide assistance to similar subsets of students across sessions — students who received help earlier were more likely to receive additional help later, even after accounting for current engagement state — while idle students did not receive sustained attention. Help coincided with immediate within-session learning but did not predict skill acquisition in later sessions. The implication: real-time attention-coverage analytics that highlight under-visited students are needed to support equitable and effective allocation of teacher attention.

**Status this cycle:** this finding was incorporated into the Teacher Attention Equity Auditor skill (2026-04-28) and is the primary evidence base referenced in that skill's design rationale. The 2026-04-28 KB note on the LAK26 finding is the existing primary reference; this 2026-05-18 entry expands the reference to a full paragraph for the durable record and notes that the LAK26 conference presentation (scheduled for the LAK26 conference proper) may produce supplementary findings worth re-scanning in a future cycle.

**Practitioner heuristic:** the Teacher Attention Equity Auditor skill remains the repo's primary response to the sticky-help finding. No skill change this cycle.

### MagicSchool Class Writing Feedback Workflow (2026-05)

MagicSchool's May 2026 platform update added a Class Writing Feedback workflow: teachers review AI-suggested comments grounded in their rubric, personalize them, and send the feedback directly into students' Google Docs. The workflow extends MagicSchool's existing per-student feedback tools to a class-batch pattern, with rubric-grounding (the Knowledge feature, where Enterprise districts upload curriculum docs up to 50MB, anchors the AI's rubric understanding) and direct LMS-side delivery (no copy-paste step from MagicSchool to Google Classroom / Google Docs).

**Practitioner heuristic:** the workflow signal does not require a new skill — the Student Feedback Generator skill already covers per-artifact feedback generation, and the Feedback Comment Bank Builder skill (2026-05-11) covers the reusable comment library that underlies efficient comment generation. The MagicSchool workflow is a platform-side implementation of the same pattern at the class-batch level; teachers who do not have MagicSchool Enterprise can replicate the workflow with the Student Feedback Generator + Feedback Comment Bank Builder pair, calibrated to their own rubric. The MagicSchool workflow is logged here as confirmation that the rubric-grounded, teacher-personalized, LMS-delivered feedback pattern is the converging market pattern for writing feedback in 2026.

### Anthropic + Teach For All AI Literacy & Creator Collective (2026-01 → 2026-05)

Announced January 2026 and active through Q2 2026, the Anthropic + Teach For All AI Literacy & Creator Collective (AI LCC) provides Claude access and AI fluency training to 100,000+ educators across 63 countries through the Teach For All network. Components: an AI Fluency Learning Series (six live episodes covering AI fluency, Claude capabilities, and practical classroom applications — over 530 educators attended the first series in November 2025); Claude Connect (the community's ongoing learning hub with 1,000+ educators representing 60+ countries exchanging prompts, use cases, and discoveries); cohort-specific cohorts (e.g., the November 2025 cohort; the spring 2026 cohort). Reported teacher-built artifacts include an interactive climate education curriculum built by a teacher in Liberia using Claude Artifacts within weeks of attending training, and a gamified math learning app with boss battles, leaderboards, and XP rewards built by a teacher in Bangladesh for Grade 6-7 students.

**Practitioner heuristic:** the AI LCC is the largest current Claude-specific teacher training initiative globally, and a useful counterweight to Google's domestic-US-focused AI Educator Series (2026-05-13). Districts and teacher-preparation programs designing AI literacy professional development can offer Anthropic Academy's four free courses (AI Fluency for Students, for Educators, Teaching AI Fluency, AI Fluency Framework & Foundations) as a no-cost, vendor-diverse complement to the Google AI Educator Series. The AI Literacy Lesson Plan Generator skill in this repo can scaffold the lesson-design step that follows either training stream.

### ETS Adapt AI Teacher Literacy Assessment (early 2026)

ETS released Adapt AI, a formal teacher AI competency assessment that measures four areas: recognizing and understanding AI, identifying AI features within existing edtech tools, practical and ethical application of AI in classroom settings, and AI-supported pedagogy. Districts can use Adapt AI as a baseline-and-growth measure for AI literacy PD investment; ETS has positioned the assessment to support potential future state-level AI literacy certification requirements (no state has yet mandated AI literacy as a certification component as of May 2026; Ohio's mandate addresses policy adoption rather than certification). ISTE is concurrently updating its Teacher Ready framework to reflect AI competencies, with release scheduled for early-to-mid 2026.

**Practitioner heuristic:** the ETS Adapt AI assessment and the ISTE Teacher Ready framework update both formalize what counts as teacher AI literacy. The AI Literacy Lesson Plan Generator skill in the repo can scaffold the lesson-design competency layer; the four Anthropic Academy courses cover the recognition/understanding/ethical-application layers; the Google AI Educator Series covers the practical-tool-fluency layer. Districts designing AI literacy PD pathways can mix the three with the ETS Adapt AI assessment as the measurement instrument.

### Student AI Advisory Panel Signal (2026-04) — New Backlog Item

EdWeek ("A Group of Students Took a Deep Dive Into AI. Here's What They Told Teachers," April 2026) documents the Percy Julian Middle School (Oak Park, Illinois) student AI advisory panel pattern: students investigate AI tools throughout the year, present findings and recommendations to faculty in a panel format, and shape building-level AI norms. The pattern is part of the broader student-voice-in-AI literature (BCcampus "Centring Student Voice and Choice in AI-Enhanced Teaching and Learning," December 2025; Teach Plus teacher-leadership cohorts; the long-standing student-voice literature on partnership-with-students-as-co-architects-of-learning). The pattern is currently anchored on case examples rather than a widely adopted framework.

**Practitioner heuristic:** the pattern is intriguing enough to add to the backlog (7/7) as a Student AI Advisory Panel Facilitator skill candidate — a teacher-side tool to help facilitate the student panel's investigation, prepare the student presenters, and document the panel's recommendations for building-level AI policy work. Held at backlog this cycle pending additional case examples that would clarify the design envelope (panel size, investigation cadence, evidence-gathering protocols, faculty-response protocols, link to building AI committee structure if any).

### Skill-Repo Coverage Map (post-2026-05-18 additions)

| 2026 Force | Repo Skill(s) That Respond |
|---|---|
| Durable-skills assessment pilot (ETS / Carnegie Learning; broader Portrait of a Graduate movement) | **Durable Skills Evidence Synthesizer (NEW)** |
| Special-education AI adoption (57% per CDT) + Ohio July 1 mandate (~6 weeks out) | **IEP/504 Accommodation Recommender (NEW)**, IEP Goal Progress Tracker, Behavior Intervention Plan Drafter |
| NC State LAK26 "sticky help" attention-equity finding | Teacher Attention Equity Auditor (carried) |
| MagicSchool Class Writing Feedback workflow (rubric-grounded, teacher-personalized, LMS-delivered) | Student Feedback Generator + Feedback Comment Bank Builder (carried) |
| Anthropic + Teach For All AI LCC (100K educators, 63 countries) | AI Literacy Lesson Plan Generator (carried; pairs with Anthropic Academy four free courses) |
| ETS Adapt AI teacher literacy assessment + ISTE Teacher Ready framework refresh | AI Literacy Lesson Plan Generator (carried) |
| District build-vs-buy ("vibe coding," $200-250K savings at Peninsula) | Out-of-scope flag (IT-leadership track candidate); reinforces open-source repo positioning |
| Student AI Advisory Panel pattern (Percy Julian; BCcampus) | Backlog: Student AI Advisory Panel Facilitator (7/7) |

Knowledge-base ecosystem files (6 — unchanged count; 2026-05-18 update is in-place extension of this file):
- ai-feedback-and-grading.md
- ai-funding-policy-and-agentic-tools.md
- ai-tutoring-evidence-and-critical-literacy.md *(updated 2026-05-18 with durable-skills, special-ed AI adoption, vibe-coding, MagicSchool workflow, Anthropic Teach For All, ETS Adapt AI, student advisory panel signals)*
- curriculum-mapping-tools.md
- formative-assessment-and-differentiation-tools.md
- sub-plans-observation-and-plc-tools.md

### Sources Behind the 2026-05-18 Update

EdWeek Market Brief "Inside a Pilot Using AI to Rethink Assessment, Capture Students' Durable Skills" (May 2026; ETS and Carnegie Learning Skills for the Future initiative); EdWeek Market Brief "K-12 Assessments May Soon Look Very Different. Here's Why" (April 2026); North Carolina DPI Portrait of a Graduate durable-skills rubrics (K-2, 3-5, 6-8, 9-12 grade bands for adaptability, communication, critical thinking, personal responsibility, and the related durable-skills constructs); Battelle for Kids Portrait of a Graduate framework; Mastery Transcript Consortium framework; CASEL SEL competencies framework; P21 4Cs framework; OECD Future of Education and Skills 2030 transformative competencies; Center for Democracy & Technology "AI in Special Education" framework; EdWeek "Teachers Are Using AI to Help Write IEPs. Advocates Have Concerns" (October 2025, with follow-on 2026 coverage); K-12 Dive "Heightened AI use in special education brings elevated risks"; GovTech "AI Gains Ground in Special Ed, Raising Legal and Ethical Concerns"; NAPSA "Use of AI to Create IEPs and 504 Plans is on the Rise"; Playground IEP, Flint K12 accommodation suggestion tool, Undivided IEP assistant, OpenEduCat special-education AI overview, Next Generation Learning Challenges AI-and-special-education coverage, IEPFocus accommodation cheat sheet — all factual attributions to the tool/site; EdWeek "A District Expects to Save $200K From AI-Powered 'Vibe Coding'. Here's How" (May 2026); K-12 Dive "'Vibe coding' helped a Washington district save $250K in ed tech costs"; NC State / LAK26 paper "Sticky Help, Bounded Effects: Session-by-Session Analytics of Teacher Interventions in K-12 Classrooms" (Qiao Jin et al., NC State + Carnegie Mellon, April 2026; phys.org, NC State News, NC State Engineering, NC State CSC, NC State Research, EurekAlert summaries); MagicSchool blog "AI Teaching Tools For Planning, Assessment & Feedback Updates 2026" (Class Writing Feedback workflow; Knowledge feature for Enterprise districts); MagicSchool Class Writing Feedback walkthrough video (February 2026); Anthropic + Teach For All "Anthropic and Teach For All launch global AI training initiative" (January 2026, with follow-on coverage through May 2026 in EdTech Innovation Hub, eWEEK, GovTech, Dataconomy, YourStory, TechBriefly, Teach For All news); Anthropic Academy four free courses (AI Fluency for Students, for Educators, Teaching AI Fluency, AI Fluency Framework & Foundations); ETS Adapt AI teacher literacy assessment (Applied Coaching coverage; School Entrance Tests AI Simulations for Teachers coverage, May 2026); ISTE Teacher Ready framework refresh announcement; ISTE+ASCD AI Innovator Challenge; EdWeek "Do Teachers Have the Skills to Use AI? New Test Aims to Find Out" (February 2026); EdWeek "A Group of Students Took a Deep Dive Into AI. Here's What They Told Teachers" (April 2026; Percy Julian Middle School, Oak Park IL); BCcampus "Centring Student Voice and Choice in AI-Enhanced Teaching and Learning" (December 2025); Teach Plus teacher-leadership cohort coverage; MultiState "AI in Education Legislation: 2026 State Policy Trends" (April 2026); FutureEd "Legislative Tracker: 2026 State AI in Education Bills" (53 bills, 25 states; Oklahoma Responsible Technology in Schools Act adoption deadline 2027-28); ExcelinEd "Preparing Our Schools: AI Guardrails for State and School District Leaders to Consider" (February 2026); Ohio Department of Education and Workforce AI Model Policy (carried). All references are factual attributions; no verbatim text was copied into this knowledge-base file.
