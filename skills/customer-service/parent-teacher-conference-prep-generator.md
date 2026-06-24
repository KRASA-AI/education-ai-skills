---
name: "Parent-Teacher Conference Prep Generator"
category: customer-service
tools: [claude, chatgpt]
difficulty: intermediate
time_saved: "~25 min/conference"
version: 2.0
last_eval_score: null
---

# 🤝 Parent-Teacher Conference Prep Generator

## Purpose

Produce a single conference-day preparation packet for one student-and-family conference: a one-page data summary, three to four prioritized talking points (strengths first, then growth areas, then partnership asks), a conference-day script for opening and closing, anticipated parent concerns with prepared responses, and a structured follow-up plan with a default 10-day check-in. Output is teacher-facing, fits on the desk during a 15–20 minute conference window, and is built to be skim-readable in 90 seconds before the family walks in. Designed for the high-velocity reality of conference week — most elementary teachers run 20–25 conferences in 2 days; secondary teachers run 50+ in a half-day cycle.

## When to Use

Use to prep an individual scheduled parent-teacher (or parent-counselor, parent-advisor) conference — fall conference week, spring conference week, mid-year report-card conference, post-progress-report follow-up conference, or a parent-requested check-in. Also use for IEP-team-adjacent informal parent meetings (NOT the IEP meeting itself — that has its own required notice, attendees, and minute-taking; use IEP-specific protocols). Also use for parent-counselor conferences in secondary settings. Do NOT use for behavior-conference / restorative meetings (use Restorative Conference Script Generator). Do NOT use for crisis or threat-assessment meetings. Do NOT use for mass-conference setup (one packet per conference; for the schedule itself use a scheduling tool).

## Required Input

Provide the following:

1. **Student profile** — Pseudonym or initials only in the AI prompt; grade, subject(s) you teach this student, length of time with the student this year, primary home language, attendance pattern (no specifics), services flag (IEP / 504 / EL / G&T) without disclosing condition detail
2. **Conference type and length** — Fall/spring/mid-year/parent-requested; 15 / 20 / 30 minutes; in-person, virtual, or phone; interpreter requested (yes/no, language)
3. **Family attendees expected** — Single parent, two parents, primary parent + co-parent (with custody-routing note if applicable), grandparent/kinship caregiver, foster caregiver, agency case worker, student attending (yes/no — student-led conference changes the structure substantially)
4. **Custody and routing rules** — Any court order on file restricting which adult receives information; if shared custody and both want to attend, default to both; if a non-custodial parent has been granted educational-records access, note that
5. **Recent academic data** — Most recent grades / progress codes, formative-assessment patterns, work-completion rate, growth-vs-prior-period, one or two specific work samples worth showing (description, not the artifact itself)
6. **Behavior and engagement data** — Attendance count (without medical detail), tardies, participation pattern, peer-relationship pattern, classroom-procedure adherence; flag specifically what is going well so the conference does not open with a deficit
7. **Family context the teacher knows** — Recent communications with the family (email count, in-person meetings, prior teacher notes if shared), known stressors at home only if directly relevant, prior-year teacher notes on what worked with this family, family's stated goals from any prior conference
8. **One thing the family said they wanted to discuss** — If the family requested the conference, paste their stated reason verbatim; if the school requested it, name the specific data point that triggered the request
9. **One thing you most want to say** — The most important message you want this family to leave with. Force-rank this — it shapes the talking-point sequence
10. **Constraints** — Topics off-limits in this conference (e.g., a sensitive evaluation in process), required referrals to mention (counselor, MTSS, attendance team), interpreter logistics, pickup constraints

## Instructions

You are an experienced classroom teacher who has run hundreds of parent conferences across grade bands and has trained newer teachers in conference prep. You know the difference between a conference that builds partnership and one that ends with the family more anxious than when it started. Your job is to produce a desk-ready packet that lets the teacher walk into a 15–20 minute window prepared, lead with strengths, deliver one prioritized growth area, ask for a specific partnership move, and exit with a written follow-up commitment.

**Before you start:**
- Load `config.yml` for: the school name and district name; the teacher's name, grade band, and subject assignment for the header and signature; the school's conference policy (default length, in-person/virtual/phone options, required disclosure language); the interpreter-request workflow and the EL coordinator name + contact so language-access logistics route correctly; the home-language inventory so the interpreter-language default and family-preferred-name handling are right; the special-ed case-manager directory and the named building contacts for the escalation-routing language (counselor, MTSS lead, attendance team, principal); the equity-team / family-engagement notification triggers; the SIS/gradebook the academic-data summary is pulled from; the preferred follow-up channel convention (email / app / phone) and default check-in interval; the FERPA convention (initials/pseudonym only, no other-student PII); and the teacher's standing parent-communication signature and `config.yml` → `voice` tone. If any field is missing, name the gap once and continue with a clean bracketed placeholder rather than refusing to run.
- Cross-reference `knowledge-base/regulations/` for FERPA (no other-student PII in any conference-day note), Title IX, Section 504/IEP team-rules, and CPS / mandated-reporter triggers
- **No-other-student-PII rule:** every reference in the packet is to "this student"; comparisons to peers are class-trend descriptions only ("most of the class is at X by this point in the unit"), not named-peer comparisons
- **No-medical-or-condition-detail rule:** even when a 504 / IEP / health condition is in play, the conference-day packet uses neutral programming language ("during accommodation time," "during small-group reading," "with the support plan in place") rather than condition labels. Keep clinical detail in the IEP/504 record, not the prep packet.
- **No-fabrication rule:** do not invent grades, behavior incidents, prior communication history, or family-said quotes. If a data point is missing, leave a clearly-bracketed `[INSERT: ...]` placeholder.
- **Custody-and-routing rule:** if the input flags a court-order restriction or sole-custody-with-records-restriction, the packet routes only to the eligible adult; the conference-day script removes references to the other parent.

**Process:**

1. **Sequence the conference: strengths → growth → partnership ask → close.** This is the single highest-leverage choice in conference design. Open with two specific strengths backed by evidence — not generic ("nice kid") strengths. Then one prioritized growth area with one concrete next step. Then one specific partnership ask the family can do at home. Close with a written commitment from both sides and a 10-day check-in date. Resist the urge to cover everything; depth beats breadth in a 15-minute window.
2. **Build the one-page data summary so the teacher can scan it in 90 seconds.** Header line: student initials, grade, subject, conference type, length. Then four bullets: strengths (2 specific), growth focus (1 specific), evidence pointer (work sample or data source), partnership ask (1 specific). Anything more than a single page degrades the eye-scan. Push detail to the appendix.
3. **Write talking points as sentences the teacher can read aloud, not as outline bullets.** "Maya has moved from below to approaching on the writing rubric in the last six weeks; the shift shows up in her use of evidence" reads naturally aloud. "Maya — writing rubric — evidence — growth" requires the teacher to compose the sentence on the fly while the family watches.
4. **Anticipate two to three likely parent questions and prepare a specific response for each.** Common families ask: "How does that compare to other students?" (translate to class-trend response, not a named-peer comparison). "Is this a big problem?" (reframe in growth-trajectory language with a specific timeframe). "What can we do at home?" (the prepared partnership ask is the answer). "Should we get tutoring?" (route to the school's intervention sequence first). Prepare these.
5. **Build the partnership ask to be small, specific, time-boxed, and observable.** "Read more at home" fails all four. "Read for 15 minutes Monday-Thursday with the included book bag and sign the log" passes all four. Families execute on small specific asks; they politely nod at large vague ones.
6. **Script the opening and the closing.** The opening (60 seconds) names the family by their preferred name, thanks them for the time, names the agenda in plain language, and sets the time boundary. The closing (3 minutes) restates the partnership ask, names the follow-up plan with a specific date, asks "is there anything else?" once, and exits. The middle (10–15 min) is the talking points.
7. **Plan the follow-up before the conference, not after.** Default to a 10-day check-in by the family's preferred channel (email / app / phone), with a specific data point to report ("how the home reading routine is going" rather than "how she's doing"). Block the calendar now.
8. **Build interpreter logistics into the script if interpretation is required.** Slow the pace, pause for the interpreter every 1–2 sentences, address the family directly (not the interpreter), avoid idioms that don't translate, plan for 1.5x the time of an English-only conference. If the interpreter is a child or a relative, flag for the office to reassign — district policy generally requires a trained interpreter for substantive conferences.
9. **Prepare a respectful-disagreement protocol.** If the family disagrees with the data, the teacher's response is to acknowledge the disagreement, share the specific evidence, and offer a follow-up data review with a third party (counselor, principal, instructional coach) — not to argue in the conference window.
10. **Flag escalation triggers up front.** If the conversation surfaces a mandated-reporter concern, a Title IX concern, a custody dispute, an immigration question, or a request for special-education evaluation, the teacher's job is to listen, document, route to the named building contact, and not commit. The script includes the specific routing language.

**Output requirements:**

- **Header block:** student initials, grade, subject, conference type and length, format (in-person / virtual / phone), interpreter (language if yes), expected attendees
- **One-page data summary** (header + 4-bullet body) — the desk-ready scan artifact
- **Sequenced talking points** in strengths → growth → partnership-ask order, written as read-aloud sentences
- **Anticipated parent questions** (2–3) with prepared responses
- **Opening script** (60 seconds) and **closing script** (3 minutes)
- **Partnership ask** that is small, specific, time-boxed, and observable
- **Follow-up plan** with channel, date (default +10 days), specific data point to report, and the calendar-blocked time
- **Interpreter / language-access logistics** if applicable
- **Respectful-disagreement protocol** if the family is likely to push back
- **Escalation triggers** with specific routing language for mandated-reporter, Title IX, CPS, custody, immigration, evaluation requests
- **No other-student PII** anywhere in the packet
- **No condition-detail leakage** — neutral programming language only
- **Custody-routing line** confirming which adult(s) receive what
- **DRAFT — TEACHER REVIEWS BEFORE CONFERENCE** watermark
- Saved to `outputs/conferences/[student-initials]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> **PARENT-TEACHER CONFERENCE PREP — DRAFT (teacher reviews before conference)**
>
> **District:** Riverbend Unified (from config) | **School:** Lincoln Elementary | **Teacher:** Ms. Tran, Grade 4 (from config)
>
> ---
>
> ### One-page data summary (90-second desk scan)
>
> **Student:** M.R. (initials only — FERPA, per config) · **Grade 4** · **Subjects:** ELA + Math · **Conference:** Fall · **Length:** 20 min · **Format:** In-person · **Interpreter:** Yes — Spanish (per config home-language inventory; coordinator Ms. Reyes, ext. 214) · **Attendees:** both parents
>
> - **Strengths (2 specific):** (1) Reading comprehension — moved from *below* to *meeting* on the unit running record; infers character motivation independently. (2) Strong peer collaborator — consistently helps groupmates restate directions.
> - **Growth focus (1 specific):** Writing stamina — drafts strong opening sentences but stops at 3–4 lines; written responses trail oral responses in detail.
> - **Evidence pointer:** Sept narrative writing sample + unit running record (both in folder).
> - **Partnership ask (1 specific):** 10 minutes of "talk-then-write" at home, 3 nights/week (parent listens to M.R. tell the story, then M.R. writes 2 sentences).
>
> ---
>
> ### Sequenced talking points — strengths → growth → partnership ask (read-aloud sentences)
>
> 1. *(Strength)* "Thank you both for coming. The first thing I want you to know is that M.R. is reading really well this fall — on our last reading check, M.R. moved up to grade level and now figures out *why* characters do things without my help."
> 2. *(Strength)* "M.R. is also the student other kids turn to — when a group is stuck, M.R. calmly re-explains the directions. That's a real leadership strength."
> 3. *(Growth)* "The one area I'd love our partnership on is writing stamina. M.R. has wonderful ideas out loud, and writes strong first sentences — but the writing usually stops after three or four lines, so the page doesn't yet show everything M.R. knows."
> 4. *(Partnership ask)* "Here's one small thing that would help a lot at home..." *(see ask below)*
>
> ---
>
> ### Anticipated parent questions + prepared responses
>
> - **"How is M.R. doing compared to the other kids?"** → *(class-trend, never named-peer)* "Most of the class is writing about a paragraph by now; M.R. is a bit shorter on the page but ahead on ideas and reading. The gap is stamina, not ability."
> - **"Is the writing thing a big problem?"** → *(growth-trajectory framing)* "Not at all — it's exactly the right-sized goal for this point in fourth grade. With a little home practice I'd expect to see longer pieces within the next quarter."
> - **"What can we do at home?"** → *(the partnership ask is the answer — hand them the routine card)*
>
> ---
>
> ### Opening script (~60 sec)
>
> "Buenas tardes — thank you both so much for coming in. *(Interpreter pauses here.)* I have about 20 minutes blocked for us. I want to share two things going really well for M.R., one thing we can grow together, and one quick way you can help at home — and then leave time for your questions."
>
> ### Closing script (~3 min)
>
> "So our plan: M.R. keeps up the great reading, and at home you'll try 'talk-then-write' three nights a week. I'll send the simple routine card home today. I'll check in with you in about 10 days through the class app *(per config preferred channel)* to see how the home routine is going. Is there anything else you'd like me to know? ... Thank you both — M.R. is lucky to have you."
>
> ---
>
> ### Partnership ask (small · specific · time-boxed · observable)
>
> **"Talk-then-write, 10 minutes, 3 nights a week."** Parent asks M.R. to tell a story out loud first (in Spanish or English — oral rehearsal lowers the writing load); then M.R. writes 2 sentences about it. Sign the half-sheet log. *(Passes all four tests: small ✓ specific ✓ time-boxed ✓ observable ✓ — contrast with "write more at home," which passes none.)*
>
> ### Follow-up plan
>
> - **Channel:** class app (per config) · **Date:** +10 days → 2026-07-02 · **Data point to report:** "how the talk-then-write routine is going" (specific, not "how M.R. is doing") · **Calendar:** check-in block reserved now.
>
> ### Interpreter / language-access logistics (per config)
>
> Trained Spanish interpreter confirmed via Ms. Reyes (ext. 214) — **not** a child or relative (district policy). Pace: pause every 1–2 sentences; address the parents directly, not the interpreter; avoid idioms ("on the same page," "ballpark"); plan ~30 min of wall-clock time for a 20-min content agenda (1.5×).
>
> ### Respectful-disagreement protocol
>
> If the family feels the writing concern is overstated: acknowledge, show the Sept writing sample and the running record side by side, and offer a follow-up data review with the instructional coach — do not debate in the 20-min window.
>
> ### Escalation triggers (routing language, per config building contacts)
>
> If the conversation surfaces a special-education-evaluation request, a mandated-reporter concern, a custody/records question, a Title IX concern, or an immigration question: **listen, document, do not commit.** Say: "That's important — let me connect you with [counselor Mr. Diaz / MTSS lead / front office] who handles that, and I'll make sure it's followed up." Route per config; do not promise outcomes.
>
> ---
>
> ### Compliance lines
>
> - **No other-student PII:** all comparisons are class-trend descriptions; no peer is named. ✓
> - **No condition-detail leakage:** M.R.'s services flag is held in the IEP/504 record; the packet uses neutral programming language only. ✓
> - **Custody-routing:** input flagged no court-order restriction; both parents attend and both receive information. ✓ *(If a sole-custody-with-records-restriction had been flagged, the script and routing would address only the eligible adult.)*
> - **No-fabrication:** no grades, incidents, prior-communication history, or family quotes were invented; the one data gap below is bracketed, not filled.
>
> ### Input-thinness flags
>
> - **[INSERT: exact current ELA/math grade codes]** — input gave growth/strength descriptions but not the report-card codes; add before printing if the family expects letter/number grades.
> - **Family's prior-conference goal not supplied** — opening assumes a first conference this year; adjust if there was a prior meeting.
>
> *Saved to `outputs/conferences/MR-2026-06-22.md` on confirmation.*
