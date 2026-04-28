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
