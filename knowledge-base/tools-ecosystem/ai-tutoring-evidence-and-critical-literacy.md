# AI Tutoring Evidence Base, Critical AI Literacy, and 2026 District Governance Signals

Snapshot as of 2026-04-27. This file complements the prior tools-ecosystem files (`ai-feedback-and-grading.md`, `curriculum-mapping-tools.md`, `formative-assessment-and-differentiation-tools.md`, `sub-plans-observation-and-plc-tools.md`, `ai-funding-policy-and-agentic-tools.md`) by capturing three threads that crystallized between 2026-04-26 and 2026-04-27: empirical RCT evidence on AI tutoring outcomes, the emerging distinction between AI literacy and critical AI literacy, and district-level governance moves and cost stories that are reshaping how superintendents are sequencing AI rollout.

## AI Tutoring — RCT Evidence and What It Means for Skill Design

The 2025–2026 evidence base on AI tutoring has moved past anecdote into randomized-controlled-trial territory, and the early signal is strong. Two trials in particular have shaped 2026 district-side conversations:

- A Harvard randomized controlled trial published in mid-2025 measured undergraduate physics learning under three conditions: traditional active-learning lecture, AI tutor only, and AI tutor with embedded research-based design (worked examples, retrieval practice, spaced retrieval, scaffolded fading). The AI-tutor-with-research-based-design condition produced learning effects of 0.73 to 1.3 standard deviations over the active-learning baseline, with the AI group spending less time on task (median ~49 minutes vs. ~60 minutes in-class).
- A Google / Eedi Labs RCT involving 165 British secondary students aged 13–15 paired AI-drafted tutor messages with a human-tutor reviewer who could revise before sending. The supervised-AI condition outperformed pure-human-tutoring on transfer items (~66% vs. ~61% on subsequent topic problems), at substantially lower cost-per-student-hour.

Several practitioner-relevant patterns recur across the AI-tutoring research corpus:

- The strongest effects are observed when the AI tutor uses Socratic questioning rather than answer-explaining. This validates the design choices in the Socratic Tutor Prompt Builder skill (question-pattern repertoire, misconception branches, adaptive scaffolding, reflective pauses, give-the-answer escape hatch).
- Human oversight remains a load-bearing component. The "AI-only" condition consistently underperforms the "AI + human review at structured intervals" condition. The teacher-review summary at the end of every Socratic Tutor Prompt Builder output, and the transcript-review cadence built into the deployment companion, sit on this evidence.
- The cost-per-effective-tutor-hour is the single largest driver of district interest in 2026. With high-dose tutoring at ~$2,000–4,000 per student per year out of reach for most districts, the supervised-AI pattern at ~10–20% of that cost is the pragmatic on-ramp.

The implication for the skills repo: AI-tutor design skills (Socratic Tutor Prompt Builder, future small-group AI-tutor protocols) sit on a strengthening evidence base, not on demo-day enthusiasm.

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

## Skill-Repo Coverage Map — Post 2026-04-27

Skills as of this cycle (27 total):

- **Admin (7)** — Behavior Intervention Plan Drafter, Classroom Observation Feedback Generator, Education Grant Proposal Drafter, IEP Goal Progress Tracker, PLC Agenda & Data Protocol Builder, Restorative Conference Script Generator, Student Progress Report Writer
- **Customer Service (3)** — Classroom Newsletter Generator, Parent Communication Drafter, Parent-Teacher Conference Prep Generator
- **Operations (14)** — Academic Vocabulary Builder *(new)*, AI Literacy Lesson Plan Generator, Assessment Question Writer, Critical AI Inquiry Prompt Builder *(new)*, Curriculum Standards Aligner, Differentiation Planner, Exit Ticket Generator, Lesson Plan Builder, Rubric Generator, Socratic Tutor Prompt Builder, Student Feedback Generator, Substitute Lesson Plan Generator, Text Level Adjuster, Writing Conference Prep Generator *(new)*
- **\_shared (3)** — Email Drafter, Meeting Summarizer, Review Responder

Knowledge-base ecosystem files (6):
- ai-feedback-and-grading.md
- ai-funding-policy-and-agentic-tools.md
- ai-tutoring-evidence-and-critical-literacy.md *(new)*
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
- Out of teacher-prompt repo scope but flagged: District AI Acceptable Use Policy Drafter (governance artifact, candidate for a SEA / LEA-policy track if one exists); Knowledge Pack / RAG Curriculum Document Builder (platform configuration, candidate for repo-side or LEA-side track); Teacher AI-Coaching Reflection Companion (district-PD artifact, candidate for the same future track)
