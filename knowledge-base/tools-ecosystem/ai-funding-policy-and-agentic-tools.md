# AI Funding, Policy, and Agentic Tools Landscape — Education

Snapshot as of 2026-04-26. This file complements the four prior tools-ecosystem files (`ai-feedback-and-grading.md`, `curriculum-mapping-tools.md`, `formative-assessment-and-differentiation-tools.md`, `sub-plans-observation-and-plc-tools.md`) by capturing three converging 2026 forces that shape what skills the education repo needs next: federal and private AI funding, AI literacy policy momentum, and the shift from "prompted chat" to "agentic" tools.

## 2026 Federal AI-in-Education Funding Posture

The US Department of Education finalized a Secretary's Supplemental Priority on Advancing AI in Education on 2026-04-13, taking effect 2026-05-13. The priority directs Department-administered competitive grant programs to give preference to applications that:

- Expand age-appropriate AI and computer science education in schools
- Embed AI and computer science into teacher preparation programs
- Provide professional development for educators to integrate AI into subject areas
- Offer dual-enrollment AI/CS opportunities for high schoolers
- Use AI to support K-12 services for students with disabilities
- Integrate AI-driven tools into classrooms for personalized learning
- Use AI to reduce time-consuming administrative tasks

The "AI to reduce administrative tasks" priority continues the directional shift announced in the 2026-04 cycle and is the single most direct funding signal for the educator-productivity skills already in this repo (Substitute Lesson Plan Generator, Classroom Observation Feedback Generator, PLC Agenda & Data Protocol Builder, Parent Communication Drafter, Meeting Summarizer, Email Drafter).

NSF announced an Expanding K-12 Resources for AI Education Dear Colleague Letter, accepting supplemental funding requests from existing NSF awardees in DRK-12, ITEST, and AISL. Supplements may be up to 20% of the original award budget with a $300,000 cap, designed to refine, scale, or evaluate existing K-12 AI/CS work.

Digital Promise opened the K-12 AI Infrastructure Program in February 2026, with awards of $50,000–$250,000 over 6–12 months. Two tracks: proof-of-concept and asset-enhancement.

The FIPSE Special Projects Program at the Department of Education is a parallel postsecondary vehicle for AI-related innovation, with the 2025 NOFO carrying forward into 2026 funding decisions.

State-level AI grants are emerging in Maryland, New Jersey, and Massachusetts, with smaller pools and shorter timelines than federal programs but lower competition.

## 2026 Private and Philanthropic AI-in-Education Funding

Humanity AI launched in late 2025: a $500 million five-year initiative pooled across the Doris Duke Foundation, Ford Foundation, Lumina Foundation, Kapor Foundation, John D. and Catherine T. MacArthur Foundation, Mellon Foundation, Mozilla Foundation, Omidyar Network, David and Lucile Packard Foundation, and Siegel Family Endowment. Education is one of five named priority areas (the others: democracy, humanities and culture, labor and economy, security). Rockefeller Philanthropy Advisors administers the pooled fund. First grant decisions are anticipated through 2026.

Spencer Foundation continues its AI + Education initiative; Bill & Melinda Gates Foundation continues its AI in Personalized Learning portfolio; Walton Family Foundation supports AI tutoring in K-12 with a charter-network emphasis.

Corporate-foundation activity continues at Microsoft Philanthropies (TEALS, Microsoft AI for Good), Google.org (AI for Education), OpenAI Academy, AT&T Achievery, Verizon Innovative Learning, and Salesforce.org. Corporate-foundation grants tend to be smaller and faster than federal but require alignment to the corporation's CSR theme.

Aggregate 2026 K-12 AI funding pool across federal, state, foundation, and corporate-foundation sources exceeds $800M (Granted AI 2026 estimate).

## 2026 State AI Policy Landscape

134 AI-in-education bills were introduced in 31 states during the 2026 legislative session, focused on data privacy, classroom-use restrictions, and curriculum integration. Approximately 33 states now have official guidance or policy on AI use in schools.

Notable state-level mandates:

- **New Jersey** — School districts are required to incorporate AI concepts, skills, and ethical-use instruction into K-12 curriculum; public IHEs must offer AI certificate and degree programs
- **Georgia** — Computer science (including AI) becomes a high school graduation requirement starting 2031–2032, with phased statewide CS access
- **Maryland** — State Department of Education AI guidance issued; local school systems must adopt AI policies and promote AI literacy; AI integrated into workforce standards and educator training; statewide AI-in-K-12 collaborative; designated district AI coordinators; university-supported certification of compliant AI tools
- **California, Texas, Florida, Illinois, New York, Washington** — Active 2026 AI-in-education legislation in committee or enacted; varies by state on student-data privacy, AI-detector use restrictions, and curriculum mandates

District-level milestone: Boston Public Schools became the first major-city district to adopt AI fluency as a graduation requirement, with mandatory AI literacy across BPS high schools starting September 2026. Other large urban districts are watching.

The federal posture on AI-detection tools, reflected in 2026 ED guidance and most state guidance documents, is that AI detectors should inform educator judgment, not replace it — no student should face academic consequences based solely on automated detection. This posture is the basis for the no-AI-as-authority rule in the AI Literacy Lesson Plan Generator skill.

## 2026 AI Literacy Frameworks Adopted in Practice

UNESCO published two AI Competency Frameworks in September 2024 that are now the most-cited cross-jurisdictional reference for district AI literacy adoption:

- **AI Competency Framework for Teachers** — five competency areas (human-centered mindset, ethics of AI, AI foundations and applications, AI pedagogy, AI for professional development); three progression levels (Acquire, Deepen, Create)
- **AI Competency Framework for Students** — four competency areas (human-centered mindset, ethics of AI, AI techniques and applications, AI system design); same three progression levels

Other widely-cited frameworks: AI4K12 Five Big Ideas (perception, representation and reasoning, learning, natural interaction, societal impact), ISTE AI Standards for Students, Code.org AI 101, MIT Day of AI curriculum, Stanford CRAFT framework. Most district-adopted AI literacy curricula draw from a mix of these rather than picking one cleanly.

UNESCO's frameworks structure the AI Literacy Lesson Plan Generator skill in this repo.

## 2026 Agentic AI in Education

The dominant shift across 2026 platforms is from "AI as a tool you prompt" to "AI as an agent that acts." The framing shows up in product releases:

- **MagicSchool** — Knowledge feature (RAG over district-uploaded curriculum, rubrics, policies — applied automatically across all 80+ teacher tools); Studio Mode (document-based editing space for AI outputs); Learning Outcomes Module (formative assessment + Class Writing Feedback)
- **Khanmigo (Khan Academy)** — Continued evolution of the Socratic tutor design; 2026 pilots show 30+ minutes/week of Socratic dialogue correlating with 2–3 weeks of additional instructional gain (from the 2026-04-24 monitor cycle)
- **Canvas IgniteAI Agent (Instructure)** — Launched March 2026; agent generates rubrics, reviews discussions, aligns content, produces personalized feedback; explicit guardrails preventing fully-automated grading; free for US Canvas customers through June 30, 2026
- **SchoolAI Spaces** — Multi-agent classroom workspaces with student-facing AI characters (e.g., historical figures, subject-matter tutors)
- **Brisk Teaching, Eduaide, Diffit, Flint, Snorkl** — Continued expansion from single-tool generators into multi-step workflows
- **Custom GPTs / ChatGPT Edu / Copilot Studio for Education / Gemini Gems** — District-deployed custom agents with constrained scope; the surface most likely to host the Socratic Tutor Prompt Builder skill's outputs

Industry projection: 40% of enterprise applications will embed task-specific AI agents by end of 2026 (multiple analyst sources); 86% of organizations plan to increase agentic AI investment.

The "human → AI → human" operating model documented in the 2026-04-24 cycle for sensitive workflows (observation feedback, restorative facilitation, IEP-heavy sub plans) extends to agentic deployments: districts that have moved fastest on agentic AI pair every agent with a teacher-review surface (transcript review, output approval queue, consent log) rather than letting agents act fully autonomously on student-facing surfaces.

## 2026 Headwinds That Affect Skill Design

- Platform fatigue continues to dominate: educators manage ~8 digital tools on average; ~50% report being overwhelmed (continued from prior cycle data). The implication for this repo: skills favor the workflow over the tool, and prompts are designed to deploy across Khanmigo / MagicSchool / SchoolAI / Copilot / Gemini / Claude / ChatGPT Edu rather than to lock into one platform.
- Survey data on AI use in special education (NASPA, EdWeek): 57% of special education teachers used AI on IEP/504 work in the 2024–25 school year (up from 39% the prior year); 31% use AI to identify trends in student progress; 30% to summarize IEP/504; 28% to choose accommodations. Advocates have raised concerns about disclosure, edit-history documentation, and over-personalization risk — informing the IEP/504 Accommodation Recommender backlog item.
- Teacher well-being signal: AI saves up to 5 hours/week for ~68% of educators (Q1 2026 polling), but teachers also report increased pressure to "do more with the time saved" rather than recover capacity. Skill design should explicitly position outputs as a draft the teacher refines, not as an instruction to take on more work.
- Family-engagement signal: ClassDojo and ParentSquare's 2026 AI summary features have created a new failure mode — parents detect templated AI text and disengage. The Parent-Teacher Conference Prep Generator and Parent Communication Drafter both treat the AI output as a scaffold the teacher personalizes.
- Detection tool posture: federal and most state guidance now disfavor punitive use of AI detectors. Skills that involve student-facing AI use explicitly include verify-against-non-AI-source steps to build the critical-evaluation muscle proactively rather than catch students reactively.

## Skill-Repo Coverage Map (post-2026-04-26)

| 2026 Force | Repo Skill(s) That Respond |
|---|---|
| ED Supplemental Priority — admin task reduction | Substitute Lesson Plan Generator, PLC Agenda Builder, Classroom Observation Feedback Generator, Email Drafter, Meeting Summarizer, Parent Communication Drafter, Classroom Newsletter Generator, Student Progress Report Writer |
| ED Supplemental Priority — AI for students with disabilities | IEP Goal Progress Tracker, Behavior Intervention Plan Drafter, Differentiation Planner, Text Level Adjuster, Restorative Conference Script Generator |
| ED Supplemental Priority — personalized learning | Differentiation Planner, Text Level Adjuster, Exit Ticket Generator, Student Feedback Generator, Socratic Tutor Prompt Builder (NEW) |
| ED Supplemental Priority — AI literacy in curriculum | AI Literacy Lesson Plan Generator (NEW) |
| ED + NSF + Digital Promise + Humanity AI funding wave | Education Grant Proposal Drafter (NEW) |
| State AI literacy mandates (NJ, MD, GA, BPS) | AI Literacy Lesson Plan Generator (NEW) |
| Family-engagement AI fatigue / parent-side templated-text detection | Parent Communication Drafter, Classroom Newsletter Generator, Parent-Teacher Conference Prep Generator (NEW), Review Responder |
| Agentic shift / district-deployed custom agents | Socratic Tutor Prompt Builder (NEW) |
| UNESCO competency frameworks adoption | AI Literacy Lesson Plan Generator (NEW) |

## Open Coverage Gaps (carried forward)

- **IEP/504 Accommodation Recommender** — high-relevance, partial overlap with IEP Goal Tracker and BIP Drafter; deferred to next cycle to give the evaluator time to assess the four new 2026-04-26 skills before adding cross-couplings
- **Choice Board / HyperDoc Builder** — UDL-aligned student choice menus; Differentiation Planner partially covers planning, but the choice-board artifact itself is not produced. Backlog.
- **Success Criteria / "I Can" Converter** — objectives → student-friendly success criteria; partial overlap with Lesson Plan Builder. Backlog.
- **Feedback Comment Bank Builder** — reusable, skill-tagged comment libraries; partial overlap with Student Feedback Generator (one-off vs. library). Backlog.
- **Discussion Question Generator** — Bloom/DOK-tiered open-ended discussion prompts; partial overlap with Assessment Question Writer (items vs. discussion). Backlog.
- **Professional Reflection Prompt Generator** — for educator self-reflection and PLC closure; partial overlap with PLC Agenda Builder. Backlog.
- **AI Acceptable Use Policy Drafter** — district-side governance artifact, not a teacher prompt. Out of repo scope; flag to the SEA/LEA-policy ai-skills-manager track.
- **Knowledge Pack / RAG Curriculum Document Builder** — the MagicSchool Knowledge feature pattern; this is platform configuration, not a teacher prompt skill. Out of scope.

## Sources Behind This Snapshot

Federal Register Final Priority and Definitions on Advancing AI in Education (2026-04-13); NSF Expanding K-12 Resources for AI Education DCL; Digital Promise K-12 AI Infrastructure Program (Feb 2026); MacArthur / Mellon / Omidyar / Ford / Doris Duke / Lumina / Kapor / Mozilla / Packard / Siegel Humanity AI announcement; FIPSE 2025 NOFO; K-12 Dive AI grant priorities coverage (2026-04); Granted AI 2026 funding survey; UNESCO AI Competency Frameworks for Teachers and Students (2024); MultiState 2026 AI legislation tracker; NASBE 2026 state policy review; Boston Public Schools September 2026 AI fluency mandate; MagicSchool Knowledge feature blog (2026); Inside Higher Ed Canvas IgniteAI Agent coverage (March 2026); EdWeek special-education AI survey (2025–26); EdSurge teacher-graded-work coverage (2026-02); AI4K12 Five Big Ideas; ISTE AI Standards for Students; MIT Socratic Mind oral-assessment platform; arXiv Socratic chatbot critical-thinking study (2024); Khanmigo prompt-engineering case studies. All references are factual attributions; no verbatim text was copied into this knowledge-base file.

---

## Disclosure-Based Governance Convergence — 2026-05-06 Update

The 2026-05-06 monitor cycle captures a consolidation of the disclosure-based governance pattern across federal, state, district, and classroom layers. The pattern is the policy-side analogue of the verify-against-non-AI-source habit on the pedagogy side: rather than relying on detection (which the federal posture, most state guidance, and a growing body of higher-education lawsuits have moved against), districts and teachers are increasingly disclosing AI use in advance, task by task, with named tools, named permissions, named attribution standards, and named verification expectations.

**The four converging layers, as of 2026-05-06:**

- **Federal (effective 2026-05-13).** The US Department of Education Secretary's Supplemental Priority on Advancing AI in Education takes effect one week from this monitor cycle. The priority does not mandate any specific disclosure language but funds applications that build AI literacy and ethical-use practice, which in practice routes through district AUPs and classroom syllabi.

- **State (Ohio mandate now ~8 weeks out; Idaho, Maryland, NJ, Georgia continuing).** Ohio's House Bill 96 requires every public, community, and STEM school to adopt a board-approved AI policy by 2026-07-01. The Ohio Department of Education and Workforce released the model AI policy on 2025-12-30; districts may adopt or customize. Idaho's SB 1227 requires a statewide framework, local policies, AI literacy standards, educator training, and data-privacy requirements, and prohibits AI from replacing human teachers. Maryland's SB 720 / HB 1057 require state guidance, local policies, AI literacy promotion, workforce-standards integration, and a statewide AI-in-K-12 collaborative. Georgia's CS-with-AI graduation requirement begins 2031–2032; Mississippi's begins 2029–2030. The Boston Public Schools September 2026 AI fluency graduation requirement remains the visible major-city leading edge.

- **District (NYC traffic-light comment window through 2026-05-08).** New York City Public Schools released preliminary AI guidance for 78,000 teachers and 1.1M students in March 2026 using a red-yellow-green traffic-light model. **Red light (prohibited):** AI for grading decisions, promotion decisions, discipline decisions, counseling decisions, special-education plan development; individual student data may not be used for training AI models. **Yellow light (proceed with caution / trained-professional review required):** student use of AI for research, exploration, and creative projects; teacher use of AI to find trends in student data, generate translations for bilingual learners, or adapt materials for students with disabilities. **Green light (approved):** lesson planning, unit planning, teacher training, scheduling, resource planning, drafting communications to families and staff, translating for non-English-speaking families, organizing information. The 45-day public comment window closes 2026-05-08; the comprehensive AI playbook is expected June 2026. The model is being adopted or adapted by other large urban districts; Chalkbeat and Gothamist coverage notes that several NYC schools had already developed local AI policies before the city-level guidance landed, and the city policy harmonizes rather than supersedes them. Higher-education traffic-light convergence (UWisconsin–Green Bay, Vanderbilt, Cornell, Columbia, KU, Harvard FAS — which announced a 2026-04-28 transition from ChatGPT Edu to Claude for FAS use) reinforces the model across both K-12 and postsecondary.

- **Classroom (the new repo skill).** The Course-Level AI Use Disclosure / Syllabus Block Generator is the classroom-level companion to the district AUP and the state-mandate posture — it produces a course-level syllabus block, a task-by-task permission grid, a one-page Student Disclosure Sheet template, a one-page Parent / Family Summary, a per-unit refresh prompt, a rubric criterion, a parent-teacher conference talking point, an academic-integrity-not-detector escalation block, an IEP/504-AI carve-out paragraph, and a subgroup-support block. The skill mirrors the district AUP and state-mandate language verbatim rather than paraphrasing.

**The community-pushback signal — 2026-04-27 and 2026-05-01 NYC events.** On 2026-04-27, NYC Public Schools scrapped plans for an AI-focused high school and paused a Manhattan middle school closure after intense parent and community opposition. On 2026-05-01, more than 100 parents and students testified at a marathon Panel for Educational Policy meeting demanding a moratorium on AI in NYC schools. The signal does not invalidate the traffic-light model; it does indicate that families are engaging more directly with the AI rules their schools are adopting and that disclosure-and-transparency is now a near-term expectation, not an aspirational standard. The signal underscores why the Course-Level AI Use Disclosure skill ships with a parent-facing one-page summary and a no-penalty opt-out path: the structural answer to community pushback is to make the rules predictable, the alternatives real, and the opt-out painless — not to argue with concerned families.

**The detection retreat.** Federal posture (2026-04 ED guidance) and most state guidance now disfavor punitive AI-detector use; higher-education lawsuits filed by students against universities over AI-detector accusations are documented and growing. The classroom-side response is the verification-against-non-AI-source step the repo's AI Literacy Lesson Plan Generator, Critical AI Inquiry Prompt Builder, and now Course-Level AI Use Disclosure / Syllabus Block Generator all build in. Detector scores alone are not academic-integrity evidence; the conversation-with-the-student step is the standard, and the named district academic-integrity contact handles the formal referral path when needed.

**The CDT IEP framework.** The Center for Democracy and Technology's 2026 framework for ethical AI use in IEP development names: an AI-Use Disclosure statement on IEP documents; plain-language guides for families explaining AI's role and limitations; documented family consent or concern before any AI-drafted content is finalized; teacher-as-human-author-of-record; preserved edit-history; mandated district training on responsible IEP-AI use. The framework converges with NYC's red-light prohibition on AI-for-IEP-development and with the IEP / 504 Accommodation Recommender backlog item the repo has carried since 2026-04-26. The skill, when built, will be designed as advisory-only / brainstorming-mode with mandatory disclosure, teacher-author-of-record, edit-history preservation, and the no-PII-into-any-tool floor.

**Skill-repo coverage map (post-2026-05-06):**

| 2026 Force | Repo Skill(s) That Respond |
|---|---|
| Disclosure-based classroom governance (NYC traffic light, Ohio mandate, ED priority) | **Course-Level AI Use Disclosure / Syllabus Block Generator (NEW)**, Critical AI Inquiry Prompt Builder, AI Literacy Lesson Plan Generator |
| Detection-tool retreat / verify-against-non-AI-source habit | Course-Level AI Use Disclosure / Syllabus Block Generator (NEW), Critical AI Inquiry Prompt Builder, AI Literacy Lesson Plan Generator |
| Community-pushback signal (NYC 2026-04-27 / 2026-05-01) | Course-Level AI Use Disclosure / Syllabus Block Generator (NEW; ships with parent-facing one-page summary + no-penalty opt-out), Parent Communication Drafter, Classroom Newsletter Generator |
| CDT IEP-AI framework | IEP/504 Accommodation Recommender (backlog, designed advisory-only with disclosure + edit-history when built), Course-Level AI Use Disclosure / Syllabus Block Generator (NEW; carve-out paragraph) |
| State-mandate compliance windows (Ohio 2026-07-01, Idaho framework rollout, NJ / MD / GA mandates) | Course-Level AI Use Disclosure / Syllabus Block Generator (NEW; mirrors mandate language verbatim) |

**The agentic-shift signal continues.** TeachBetter.ai released Version 5.0 with PaperQR Live Quiz on 2026-05-06 — a device-free formative-assessment surface using multidirectional QR cards that the teacher scans with a phone. The release is one of several 2026-Q2 platform feature drops that continue the agentic shift documented on 2026-04-26; no specific operating-model implication that warrants a new skill, but the device-free form factor matters for the Exit Ticket Generator's platform-calibration list (paper / slide / whiteboard now joined by paper-with-QR-scan).

## Sources Behind the 2026-05-06 Update

Ohio Department of Education and Workforce AI in Education Model Policy (2025-12-30); Federal Register Final Priority on Advancing AI in Education effective 2026-05-13; NYC Public Schools preliminary AI guidance March 2026, public comment window through 2026-05-08, comprehensive AI playbook expected June 2026 (Chalkbeat, Gothamist, GovTech, PIX11, Union-Bulletin, ground.news); Chalkbeat coverage of NYC AI high school cancellation 2026-04-27; Chalkbeat coverage of Panel for Educational Policy marathon meeting 2026-05-01; Idaho SB 1227; Maryland SB 720 / HB 1057; New Jersey K-12 AI ethical-use curriculum mandate; Boston Public Schools September 2026 AI fluency graduation requirement; UNESCO AI Competency Frameworks for Teachers and Students (2024) — five competencies × three progression levels for teachers, four competencies × three levels for students; OECD-EC AI Literacy Framework for Primary and Secondary Education review draft (May 2025; final 2026 release pending); Center for Democracy and Technology AI in IEP Development framework; NASPA / EdWeek special-education AI survey (~57–60% of special-education teachers used AI on IEP/504 work in 2024–25); Washington Post and Inside Higher Ed coverage of AI-detector lawsuits and federal / state retreat from punitive detector use; KU Center for Teaching Excellence and University of Wisconsin–Green Bay traffic-light syllabus model; Vanderbilt, Cornell, Columbia AI policy guidance; Harvard FAS 2026-04-28 announcement transitioning from ChatGPT Edu to Claude for Education; TeachBetter.ai V5.0 PaperQR Live Quiz release 2026-05-06; Anthropic + Teach For All AI Fluency Learning Series (carried from prior cycle). All references are factual attributions; no verbatim text was copied into this knowledge-base file.
