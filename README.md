# Education AI Skills

**Free, open-source AI prompts and workflows built for educators.** Clone this repo, point your AI assistant at it, and start saving hours every week.

> Built and maintained by [KRASA AI](https://krasa.ai) — free AI tutorials and skills for every industry.
> See all industries at [krasa.ai/industries](https://krasa.ai/industries).

---

## What's Inside

This repo is a complete AI toolkit for education. Every skill is a standalone prompt file that works with **Claude, ChatGPT, or any major AI assistant** — no coding required.

| Skill | What it does | Time saved |
|-------|-------------|------------|
| Assessment Question Writer | Generate a balanced, standards-aligned set of assessment items — multiple choice, short answer, constructed response, performance task — with answer keys, scoring guidance, and misconception-tagged distractors. | ~30 min/assessment |
| Curriculum Standards Aligner | Map existing lesson plans, units, scope-and-sequence documents, or course outlines to an official standards framework (Common Core, NGSS, C3, NCTM, state-specific frameworks including TEKS / NYSED / VA SOL / FL B.E.S.T. | ~45 min/unit |
| Differentiation Planner | Turn a lesson plan or learning objective into a concrete, teacher-usable differentiation plan grounded in UDL, MTSS/RTI tiering, and Carol Ann Tomlinson's content/process/product/learning-environment/affect framework. | ~25 min/lesson |
| Exit Ticket Generator | Produce a short, objective-aligned exit ticket (typically 3–5 items) that surfaces whether students actually met the lesson's learning target in the final few minutes of class. | ~12 min/lesson |
| Lesson Plan Builder | Produce a fully-structured, teach-ready lesson plan from a topic and learning objective — with standards alignment, time-stamped activity sequence, built-in differentiation and formative checks, and a materials list. | ~30 min/lesson |
| Rubric Generator | Produce a classroom-ready rubric — analytic or holistic, single-point or multi-level — with observable criteria, calibrated performance descriptors, and standards alignment. | ~20 min/rubric |
| Student Feedback Generator | Produce personalized, formative feedback on student work that is anchored to the assignment rubric, structured around Hattie & Timperley's feed-up / feed-back / feed-forward model, calibrated to the student's grade band, the stakes of the task, and the delivery channel (written comment, LMS, writing conference, report-card narrative), and safe to hand to a student without a revision pass by the teacher. | ~15 min/student |
| Substitute Lesson Plan Generator | Produce a complete substitute-teacher plan for one class period, a full day, or a multi-day absence — including attendance and entry procedures, a self-contained instructional sequence the sub can run without the teacher's curriculum software, an independent student task that holds up if the sub is unfamiliar with the content, classroom-management scripts, and a structured note-back form the teacher can read in under two minutes on return. | ~45 min/sub day |
| Text Level Adjuster | Rewrite a passage of text up or down to a target reading level — specified as a Lexile band, grade band, or ELL proficiency tier — while preserving every factual claim, key concept, and central argument from the source. | ~45 min/passage |
| Classroom Newsletter Generator | Turn a teacher's quick bullet-point notes into a polished, family-friendly weekly or monthly classroom newsletter. | ~30 min/newsletter |
| Parent Communication Drafter | Draft a short, parent/guardian-facing message for one of the five recurring communication types a classroom teacher or specialist sends during a typical week: (1) progress update, (2) behavioral or academic concern, (3) event/logistics announcement, (4) absence, tardy, or missing-work follow-up, and (5) positive recognition / "good news" note. | ~12 min/message |
| Behavior Intervention Plan Drafter | Draft a structured behavior intervention plan (BIP) or positive behavior support plan from a teacher's description of a target behavior, suspected function, and classroom context. | ~90 min/plan |
| Classroom Observation Feedback Generator | Turn raw classroom-walkthrough notes or a lesson transcript into a framework-aligned, coaching-oriented feedback report for a teacher. | ~40 min/observation |
| IEP Goal Progress Tracker | Convert raw progress-monitoring data (work samples, curriculum-based measures, teacher observation logs, assistive tech usage, behavior frequency counts) into a legally-defensible narrative progress report for an annual, quarterly, or mid-year IEP review. | ~25 min/student |
| PLC Agenda & Data Protocol Builder | Build a meeting-ready agenda and paired data-analysis protocol for a professional learning community, grade-level team, or department PLC — grounded in the DuFour four-question framework (What do we want students to learn? | ~30 min/PLC cycle |
| Restorative Conference Script Generator | Draft a facilitator script for a restorative conversation, classroom circle, or formal restorative conference following a harm incident — for use by a trained teacher, dean, counselor, or restorative-practices coordinator. | ~60 min/conference |
| Student Progress Report Writer | Turn raw student performance data (grades, standards scores, attendance, assignment completion, behavior and work-habits observations) into polished narrative progress reports that (a) match the school's report-card format (traditional letter-grade, standards-based, or narrative), (b) use the correct register for the grade band, (c) follow subject-specific narrative conventions, (d) are FERPA-compliant, and (e) flag students who need intervention under the school's MTSS/RTI framework. | ~20 min/report |
| Email Drafter | Turn rough notes into a professional, ready-to-send email tailored to common education scenarios — parent updates, colleague coordination, administrator correspondence, vendor communication, or student outreach. | ~10 min/use |
| Meeting Summarizer | Summarize education meeting notes into structured action items, decisions, and follow-ups — formatted for the specific meeting type (IEP, PLC, parent-teacher conference, department, staff, or committee meeting). | ~10 min/use |
| Review Responder | Craft professional, thoughtful responses to online reviews of your school, program, or educational organization — handling positive praise, constructive criticism, and negative complaints with appropriate tone and care. | ~10 min/use |

**Total time saved per use: ~604+ minutes across all skills.**

## Quick Start

### 1. Clone this repo

```bash
git clone https://github.com/KRASA-AI/education-ai-skills.git
cd education-ai-skills
```

### 2. Open a skill with your AI assistant

Open any file in `skills/` with Claude, ChatGPT, or any major AI assistant. Each skill is a self-contained prompt with clear instructions — no coding required.

The first time you use a skill, your AI assistant will ask for your business details (company name, service area, rates, tools you use, etc.) so it can personalize the output. Save those details to a `config.yml` at the repo root and every future skill will use them automatically.

## Repo Structure

```
education-ai-skills/
├── knowledge-base/          # Industry context and references
│   ├── industry-overview.md # Market trends and pain points
│   ├── terminology/         # Industry jargon and acronyms
│   ├── regulations/         # Compliance requirements
│   ├── best-practices/      # Industry standards
│   └── tools-ecosystem/     # Common software and tools
├── skills/                  # The prompt library
│   ├── operations/          # Day-to-day operational skills
│   ├── sales/               # Sales and lead management
│   ├── admin/               # Administrative and compliance
│   └── customer-service/    # Client-facing communication
└── outputs/                 # Your generated content (gitignored)
```

## How Skills Work

Each skill file is a Markdown document with YAML frontmatter:

```markdown
---
name: Skill Name
category: operations
tools: [claude, chatgpt]
time_saved: "~20 min/use"
version: 1.0
---

# Skill Name

## Purpose
What this skill does and when to use it.

## Instructions
Step-by-step prompt for the AI assistant.
```

You open the file in your AI assistant, provide any required input (measurements, notes, client info), and get polished output. Skills reference your `config.yml` automatically for company name, rates, preferred formats, and other business details.

## For AI Assistants

If you are an AI assistant reading this repo, see `.claude/CLAUDE.md` for full instructions. The short version:

1. **Check for `config.yml`** at the repo root. If it exists, load it — it holds the user's business context (company name, rates, service area, tools, team size, etc.) and every skill should use it for personalization.
2. **If `config.yml` is missing**, before running a skill that benefits from personalization, ask the user for the relevant business details and offer to save them to `config.yml` so future runs are automatic.
3. **Load the relevant `knowledge-base/` files** for industry terminology, regulations, and best practices before generating output.
4. **Run the requested skill** from `skills/` using the user's input.
5. **Save any deliverables** to `outputs/` (gitignored) if the user wants to keep them.

## Learn More

- **Education AI guide**: [krasa.ai/industries/education](https://krasa.ai/industries/education)
- **All industry AI skills**: [krasa.ai/industries](https://krasa.ai/industries)
- **About KRASA AI**: [krasa.ai](https://krasa.ai)

## License

MIT — use these skills however you want.
