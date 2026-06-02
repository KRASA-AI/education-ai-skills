---
name: "PLC Agenda & Data Protocol Builder"
category: admin
tools: [claude, chatgpt]
difficulty: intermediate
time_saved: "~30 min/PLC cycle"
version: 2.0
last_eval_score: null
---

# 📊 PLC Agenda & Data Protocol Builder

## Purpose

Build a meeting-ready agenda and paired data-analysis protocol for a professional learning community, grade-level team, or department PLC — grounded in the DuFour four-question framework (What do we want students to learn? How will we know they learned it? What will we do if they didn't? What will we do if they did?) and designed so the meeting produces concrete next-instructional-move commitments, not discussion-for-discussion's-sake. Output is structured for the team facilitator, with explicit roles, a time-stamped agenda, a protocol matched to the data on the table, and a commitment-tracking block.

## When to Use

Use for recurring PLC meetings (weekly grade-level, biweekly department), data-team meetings following a common formative/summative assessment, and MTSS/RTI team meetings where the conversation must move from data review to differentiated next steps within a fixed block of time. Also use for "data days" after interim assessments and for launching new collaborative-inquiry cycles. Do NOT use as a summary of a meeting that has already happened — that is the job of `meeting-summarizer`. Do NOT use for IEP meetings (use IEP-specific protocols and notice requirements).

## Required Input

Provide the following:

1. **Team type and cadence** — Grade-level PLC, content-area department, vertical team, MTSS/RTI team, coaching team; meeting cadence (weekly, biweekly); length of the meeting block
2. **Current cycle stage** — Launching a unit, mid-cycle progress check, post-common-assessment data review, intervention-planning, or reflection/closure
3. **DuFour question(s) in focus** — Which of the four (learn / know / didn't / did) is the main driver for this meeting? Most data-review meetings live in questions 2–4; planning meetings lean on question 1.
4. **Student data available** — Common formative assessment results, unit test, interim assessment, behavior data, attendance, work samples, student survey, or running record. The protocol changes with the data source.
5. **Team roles filled** — Facilitator, recorder, timekeeper, norms monitor, data lead; flag any that are empty so the agenda can assign them at the top.
6. **Team norms and agreements** — Paste the team's current norms (e.g., "start and end on time," "evidence before opinion," "name disagreement directly"). The agenda references them explicitly during the opening.
7. **Essential standard(s) or learning targets in focus** — The specific standards-aligned targets the data speaks to, so the protocol keeps the conversation anchored
8. **Commitments from last meeting (if any)** — What the team agreed to try; the agenda opens with a check-in on those before moving to new data
9. **Equity lens** — Specific subgroup(s) the team is tracking (ELL, students with IEPs, a named focal group) and whether disaggregated data is available

## Instructions

You are an experienced PLC coach familiar with DuFour's Learning by Doing, Solution Tree PLC at Work, Looking at Student Work (LASW) protocols, the Data Wise improvement process, and NSRF Critical Friends protocols. Your job is to produce an agenda and a matched protocol that fits the time available, keeps the conversation on evidence, and ends with named commitments each team member owns.

**Before you start:**
- Load `config.yml` for: the district's named PLC framework (e.g., "Solution Tree PLC at Work," "Data Wise Improvement Process," "NSRF Critical Friends," "district-built model based on DuFour"); the building-level PLC coach or instructional coach name and contact (e.g., "Ms. Quintero, instructional coach, ext. 218"); the team's standing facilitator / recorder / timekeeper / norms-monitor / data-lead naming convention; the team's written norms (paste verbatim); the assessment-platform inventory in use (e.g., MasteryConnect, Illuminate, Mastery Manager, NWEA MAP, iReady, Renaissance Star, district-built Google Form bank) so the data block names the actual platform; the MTSS/RTI coordinator name and contact for the Tier-3 referral path; the EL coordinator name and contact for the EL-subgroup pattern review; the special-ed coordinator name and contact for the IEP-subgroup pattern review; the district student-information system (PowerSchool, Infinite Campus, Skyward, Aeries) for the disaggregation handoff; the district's PLC artifact-retention convention (where minutes / commitments / data exhibits are filed, e.g., a SharePoint PLC archive, Google Drive folder, or BrightBytes Learning Platform); the discipline-data system (Educlimber, Branching Minds, Kickboard, Review360, Panorama, paper log) if behavior data is on the table; the district-adopted instructional framework name (Danielson, Marzano Focused, NIET TAP, state model) for the next-instructional-move language register; the reading-level band for any parent-facing communication that flows out of the meeting; the FERPA-aligned student-reference convention (student ID, pseudonym, last-name initial). If any field is missing, name the gap once and continue with a clean placeholder rather than refusing to run.
- Cross-reference `knowledge-base/best-practices/` for protocol preferences if specified
- **No-fabrication rule:** do not invent student data, standards, or prior commitments. Where the input is thin, leave bracketed placeholders the facilitator fills in before the meeting.
- **Protocol-fit rule:** the protocol must match the data. Common formative data → ATLAS-style LASW or data-driven dialogue protocol. Behavior data → Check-In/Check-Out review protocol. Interim assessment data → Data Wise Step 3–5 protocol. Survey data → Tuning protocol for analysis.
- **PII rule:** all student references use the convention from config (ID, pseudonym, or last-name initial). No first-and-last-name combinations on shared agenda documents; full names live only in the facilitator's local working file.

**Process:**

1. **Select a protocol that fits the data and the time.** A 45-minute block cannot run a full Data Wise cycle; a 75-minute block can. A 30-minute block fits a Pareto-focused "one question, one commitment" protocol. Name the protocol at the top so the team knows what they signed up for.
2. **Time-box the agenda so it actually fits.** Sum every block (opening + data review + discussion + commitments + close) and confirm it equals the meeting length — over-packed agendas are the single biggest cause of PLC drift. If the inputs require more than the meeting length allows, flag the overrun and suggest what to defer.
3. **Open with norms and last-meeting commitments.** Every meeting opens with (a) a 2-minute norm reminder keyed to the team's stated norms, (b) a check-in on commitments from the last meeting — what was tried, what was observed, what changed. If no prior commitments, open with DuFour Q1 (what do we want students to learn) as the anchoring move.
4. **Structure the data block as observe → interpret → act.** Separate "what do you notice in the data" (facts only, no interpretation) from "what does this suggest is happening in the classroom" (interpretation, tentative) from "what will we do next" (action). Mixing these three is the second-biggest cause of PLC drift.
5. **Disaggregate where equity matters.** If subgroup data is available, surface disaggregated patterns explicitly. If the team has flagged a focal group, open the data block with their data, not with the whole-class average.
6. **Sort next-step commitments by tier.** Use an MTSS/RTI lens on whatever was identified: what does Tier 1 instruction need to do differently for the whole class? What small group needs Tier 2 support? Which individuals need Tier 3 referral for consideration? Force each row to have an owner, a target date, and a visible-evidence metric.
7. **Close with a 3-minute commit-out.** Each team member names the one move they will make before the next meeting, observable and small. The recorder captures these verbatim — this becomes the opening of the next meeting.
8. **Scale the protocol depth to team maturity.** A newly-formed team gets more scaffolding (sentence starters, explicit roles, shorter protocol). A veteran team gets a tighter protocol and more team-owned pacing. Do not default to the same template for both.

**Output requirements:**

- **Header block:** team name, date, meeting length, facilitator, recorder, timekeeper, norms monitor, data lead, DuFour question(s) in focus, essential standard(s) in focus, protocol selected
- **Time-stamped agenda** summing to the meeting length — each block lists the section, time, role who leads it, and success indicator ("we leave this block when ___")
- **Data-analysis protocol** matched to the data source, with step-by-step prompts the facilitator reads
- **Observation / interpretation / action columns** (or sequenced sections) the recorder fills in live
- **Disaggregated data slot** if subgroup data is available
- **Commitment grid:** commitment → owner → target date → evidence of completion
- **Norms reminder** keyed to the team's stated norms, not generic norms
- **Parking lot** for items outside scope
- **Next meeting preview** with any pre-work assigned (data to bring, readings, student work to collect)
- Facilitator-facing language throughout — the document is a run-the-meeting tool, not a teacher-facing handout
- **No student PII** — data should be referenced by ID or pseudonym in any shared artifact
- Saved to `outputs/plc/[team-name]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> **5th-Grade ELA PLC — Common Formative Assessment Data Review**
> **DRAFT — facilitator review before distribution.**
>
> **District:** Riverbend Unified School District (from config) | **School:** Cesar Chavez Elementary
> **Framework:** Solution Tree PLC at Work (district adopted, from config) | **Instructional coach:** Ms. Quintero, ext. 218 (from config)
> **Team:** 5th-Grade ELA PLC (4 teachers + coach attending) | **Cadence:** Weekly, Wednesdays 2:50–3:40 PM | **Meeting length:** 50 min
> **Meeting #:** 14 of 36 (Unit 4, Week 2) | **Date:** 2026-05-13
> **Cycle stage:** Post–common formative assessment data review (CFA-4.2 administered Monday 2026-05-11)
> **DuFour question(s) in focus:** Q2 (How will we know they learned it?) → Q3 (What will we do if they didn't?)
> **Essential standard(s) in focus:** RI.5.6 — *Analyze multiple accounts of the same event or topic, noting important similarities and differences in the point of view they represent.*
> **Protocol selected:** Data Wise Steps 3–5 (Dig into student data → Examine instruction → Develop an action plan) — 50-min compressed variant
>
> **Roles (from team rotation, per config naming convention):**
>
> | Role | Name |
> |---|---|
> | Facilitator | Mr. Park |
> | Recorder | Ms. Idris |
> | Timekeeper | Ms. Bell |
> | Norms monitor | Mr. Vega |
> | Data lead | Ms. Quintero (coach) |
>
> ---
>
> **Time-stamped agenda (sums to 50 min — verified)**
>
> | Block | Time | Min | Lead | We leave this block when… |
> |---|---|---|---|---|
> | Opening: norms reminder + last-meeting commitment check | 2:50–2:55 | 5 | Mr. Park | Each teacher has named whether the Tier-1 turn-and-talk move from last week was tried, and what was observed |
> | Data overview: CFA-4.2 results, whole-class and disaggregated by EL / IEP / focal group | 2:55–3:05 | 10 | Ms. Quintero | The team has read the data exhibit silently and noted three observations each on the recorder's shared doc — *observation only, no interpretation yet* |
> | Observe → Interpret block: facilitated round | 3:05–3:20 | 15 | Mr. Park | The team has surfaced 2–3 candidate hypotheses for why the data looks the way it does, with explicit "we don't yet know" language where evidence is thin |
> | Act block: tiered next-move planning (Tier 1 / Tier 2 / Tier 3 referral consideration) | 3:20–3:33 | 13 | Mr. Park + Ms. Quintero | Each tier has at least one committed move with an owner, target date, and visible-evidence metric |
> | Commit-out: each teacher names the one move they own before next Wednesday | 3:33–3:37 | 4 | Mr. Park | Each teacher has named their single move in observable language; recorder has captured verbatim |
> | Close: parking-lot review, next-meeting pre-work | 3:37–3:40 | 3 | Mr. Park | Pre-work is named; meeting ends on time |
>
> *Total: 50 min ✓*
>
> ---
>
> **Norms reminder (keyed to the team's stated norms, from config)**
>
> 1. *"Start and end on time."* — We have 50 minutes, not 51. The timekeeper has authority to advance.
> 2. *"Evidence before opinion."* — During the Observe block, we describe what we see in the data, not what we think it means. Interpretation lives in the next block.
> 3. *"Name disagreement directly."* — If you disagree with a hypothesis, say so. The facilitator will hold the space.
> 4. *"Student names stay in the room."* — Per district FERPA discipline, the agenda uses student IDs; full names live only in the assessment platform.
>
> ---
>
> **Last-meeting commitment check (from 2026-05-06 minutes)**
>
> | Teacher | Committed move | Tried? | What was observed |
> |---|---|---|---|
> | Mr. Park | Add a 3-minute turn-and-talk on point-of-view evidence before independent writing on Tuesday and Thursday | [ ] | [Recorder captures live] |
> | Ms. Idris | Pre-teach the academic-vocabulary list (perspective, account, bias, evidence) to the EL small group in the Wednesday push-in block | [ ] | [Recorder captures live] |
> | Ms. Bell | Use the point-of-view anchor chart from the unit binder during the Monday mini-lesson; refer to it by name during guided practice | [ ] | [Recorder captures live] |
> | Mr. Vega | Add a graphic organizer scaffold for the two IEP-reading students during independent practice | [ ] | [Recorder captures live] |
>
> ---
>
> **Data exhibit — CFA-4.2 results (10 multiple-choice + 1 short-constructed-response item, max 12 points)**
>
> *Source: MasteryConnect (per config). Class roster N=24. Disaggregation pulled from PowerSchool (per config). All references use student ID, per FERPA convention.*
>
> | Group | N | Mean | % at/above proficient (≥9/12) | % approaching (7–8/12) | % below (≤6/12) |
> |---|---|---|---|---|---|
> | Whole class | 24 | 7.6 | 42% | 33% | 25% |
> | EL (WIDA 2–3) | 4 | 5.3 | 0% | 25% | 75% |
> | IEP — SLD reading | 3 | 5.0 | 0% | 33% | 67% |
> | Focal group (2024–25 Tier 2 ELA cohort, per coach flag) | 6 | 6.2 | 17% | 33% | 50% |
> | Whole-class minus focal/EL/IEP subgroups | 11 | 9.4 | 73% | 27% | 0% |
>
> *Item-level breakdown (whole class):*
>
> | Item | Standard sub-claim | % correct |
> |---|---|---|
> | 1 | Identify whose account a passage is from | 88% |
> | 2 | Identify whose account a passage is from | 79% |
> | 3 | Compare two accounts for shared facts | 71% |
> | 4 | Compare two accounts for shared facts | 67% |
> | 5 | Identify point-of-view evidence in a single passage | 58% |
> | 6 | Identify point-of-view evidence in a single passage | 50% |
> | 7 | Distinguish point-of-view from fact | 46% |
> | 8 | Distinguish point-of-view from fact | 42% |
> | 9 | Cite specific text evidence to support a point-of-view claim | 33% |
> | 10 | Cite specific text evidence to support a point-of-view claim | 29% |
> | 11 (SCR) | Explain how two accounts differ in point of view, citing evidence from both | 38% (rubric 3–4/4) |
>
> ---
>
> **Observe block — what we notice (facts only, no interpretation)**
>
> *[Facilitator script: "Read silently for 90 seconds. Then we go around the table — each person names one observation. We are not yet asking 'why.' Just 'what.'"]*
>
> *Recorder fills in live:*
>
> - [Observation 1 — e.g., "Item-level scores fall as items move from identifying point of view to citing evidence for it."]
> - [Observation 2]
> - [Observation 3]
> - [Observation 4]
> - [Observation 5]
>
> ---
>
> **Interpret block — what we think is happening (tentative, evidence-anchored)**
>
> *[Facilitator script: "Now we move from 'what' to 'why.' Stay tentative. Use 'one hypothesis is…' or 'this might be because…' rather than 'students don't…'."]*
>
> *Candidate hypotheses surfaced (recorder captures):*
>
> 1. [Hypothesis 1 — e.g., "Students can identify point of view when prompted explicitly but are not yet citing text evidence to support the identification — Items 9–10 and SCR-11 require the evidence-citation move and drop sharply."]
> 2. [Hypothesis 2 — e.g., "EL students at WIDA 2–3 may be losing access during the SCR because the prompt requires multi-clause written explanation without scaffolded sentence frames."]
> 3. [Hypothesis 3 — e.g., "The two IEP-SLD-reading students may be hitting a decoding ceiling on the longer passages — the pattern of error is concentrated on Items 5–6, where passage length jumps."]
>
> *Disagreements named:* [Recorder captures any]
>
> *"We don't yet know" list:* [Recorder captures any]
>
> ---
>
> **Act block — tiered next-move plan**
>
> *[Facilitator script: "Each tier needs at least one committed move with an owner, a target date, and a visible-evidence metric. We are not solving everything in 13 minutes — we are picking the smallest move that would tell us something next week."]*
>
> | Tier | Move | Owner | Target date | Visible-evidence metric |
> |---|---|---|---|---|
> | Tier 1 (whole class) | Add a 5-minute "cite-the-evidence" structured guided-practice routine to the Monday mini-lesson — explicit "find the line that tells you" prompt, with two partner check-ins | All 4 teachers | 2026-05-18 (Monday) | Item 9–10 equivalents on CFA-4.3 (2026-05-20) reach 60% correct |
> | Tier 2 (focal group + EL subgroup) | Pull a 15-minute small-group block during Wednesday independent practice for the 6 focal-group students + the 4 EL students — sentence-frame scaffolded SCR rehearsal using a fresh passage pair from the unit anchor texts; coach co-models the first session | Mr. Vega + Ms. Quintero | 2026-05-20 (Wednesday) | Each student produces a written SCR draft scoring ≥3/4 on the unit rubric (coach scores during the session) |
> | Tier 3 (consideration) | The two IEP-SLD-reading students show a decoding-ceiling pattern that may need formal SLD-reading team review; refer to MTSS coordinator (Ms. Dey, ext. 305, from config) for a discussion of whether the Tier 3 reading-fluency block should be extended for this unit; special-ed coordinator (Mr. Achebe, ext. 312, from config) cc'd for IEP-goal alignment | Ms. Idris (case manager) | 2026-05-15 (Friday) | MTSS meeting scheduled within 2 weeks; outcome documented in Branching Minds (per config) |
>
> *EL coordinator (Ms. Khoury, ext. 207, from config) was emailed the EL-subgroup pattern for awareness; she will join next Wednesday's PLC for 10 min to review the WIDA-band scaffold quality.*
>
> ---
>
> **Commit-out — one move per teacher, verbatim (recorder captures)**
>
> *[Facilitator script: "Each person names the one move you will make before next Wednesday. Observable, small, your move, not a team move. No qualifiers."]*
>
> - Mr. Park: [verbatim]
> - Ms. Idris: [verbatim]
> - Ms. Bell: [verbatim]
> - Mr. Vega: [verbatim]
>
> *These open next week's meeting.*
>
> ---
>
> **Parking lot**
>
> - [Item raised but outside scope of today's meeting]
> - [Item raised but outside scope of today's meeting]
>
> ---
>
> **Next meeting (2026-05-20) — pre-work**
>
> - All teachers: bring CFA-4.3 results from MasteryConnect (administered 2026-05-20 first period)
> - Ms. Quintero: bring the small-group SCR drafts collected 2026-05-20
> - Ms. Idris: bring the MTSS meeting outcome summary if scheduled
> - Mr. Park: bring an updated anchor chart with the "cite-the-evidence" routine added
>
> *Pre-work expectation per team norm: "No data, no meeting" — if the CFA cannot be administered Wednesday, the meeting becomes a planning meeting and the data review is rescheduled.*
>
> ---
>
> **Artifact filing**
>
> Per district PLC retention convention (from config), this agenda + completed recorder doc + data exhibit are filed to:
> `Riverbend Unified > Cesar Chavez Elementary > 5th-Grade ELA PLC > 2025-26 > 2026-05-13_CFA-4.2_review.md`
> SharePoint location (per config). Retention: 3 years.
>
> ---
>
> **Equity scan (built in, not optional)**
>
> The disaggregated table shows the focal group, EL subgroup, and IEP-SLD subgroup each scoring >2 standard deviations below the non-subgroup cohort on this CFA. The Act block above commits Tier 1, Tier 2, and Tier 3 moves directly responsive to those gaps — no "we'll get to it" deferrals on subgroup data. The 8-week disaggregated trend will be reviewed at the next data day (per district PLC framework, from config).
>
> ---
>
> **Facilitator note**
>
> This agenda is a tool for running the meeting, not a deliverable. The recorder's filled-in version after the meeting is the artifact of record. If a Tier 3 referral is initiated, the special-ed coordinator and MTSS coordinator are the named contacts in config; this PLC does not initiate special-ed eligibility procedures, only flags them for the appropriate team.
