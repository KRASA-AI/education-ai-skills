---
name: "Substitute Lesson Plan Generator"
category: operations
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~45 min/sub day"
version: 2.0
last_eval_score: null
---

# 🎒 Substitute Lesson Plan Generator

## Purpose

Produce a complete substitute-teacher plan for one class period, a full day, or a multi-day absence — including a header block with every emergency contact and procedure the sub will need to find on the first page, an attendance and entry routine, a self-contained instructional sequence the sub can run without the teacher's curriculum software, an independent student task that holds up if the sub is unfamiliar with the content, classroom-management scripts the sub reads aloud verbatim, accommodations-continuity for IEP/504/EL students named without surfacing protected-class status, an emergency quick-card for fire / lockdown / medical / student-crisis / weapon-threat events, and a structured note-back form the teacher can read in under two minutes on return. Output is explicitly written for a substitute who does not know the students, the classroom norms, or the unit, and who may have arrived ten minutes before the bell.

## When to Use

Use at three distinct moments: (1) **pre-planned absence** (PD, conference, jury duty, medical leave, parental leave) where the plan can reference the current unit and continue forward momentum; (2) **emergency absence** (sudden illness, family emergency, district closure with in-person make-up days) where the plan must be drop-in, low-prep, and standards-connected without advancing the pacing guide; and (3) **standing sub plan on file** every teacher should keep updated as the "first-week-of-school plan" or the no-prep fallback if a sudden absence happens before any specific plan is left. Also use to onboard a long-term sub mid-semester and to produce the para / co-teacher plan when the teacher is in the building but pulled to a meeting. Do NOT use for the teacher's own planning — that is the job of `lesson-plan-builder`. Do NOT use when an IEP/504 requires a specific certified substitute, a one-to-one aide, or a dedicated nurse without making that need explicit at the top of the plan and confirming the requirement is met before the sub day begins.

## Required Input

Provide the following:

1. **Absence type** — Pre-planned (continues the unit) or emergency (review/practice/generative) or standing (no specific plan in file). For emergency, default to a self-contained review of the most recently taught concept; for standing, default to a discipline-of-the-grade-level generative task.
2. **Class schedule** — Bell times, class names by period, period length, any rotations (block, A/B day), lunch / recess / specials duty, and whether the sub supervises transitions, hall duty, or after-school dismissal.
3. **Grade level, subject, and current unit** — Enough context that the sub plan is content-connected even if the sub cannot teach the content directly. If the unit hits state-tested material, flag the timing so the sub does not skip a lesson the pacing guide cannot afford to lose.
4. **Student count and any need-to-know composition** — ELL count and WIDA bands and home languages represented (no names), IEP/504 counts (no names), behavior supports that must continue (e.g., "student at desk near door uses a break card; second student has a sensory-tool kit in the back left bin"), health or safety notes (epi-pen location, allergy to supply X, seizure protocol on file in the front office, diabetic snack-time accommodation, student-with-newborn-sibling lactation accommodation if applicable for HS), McKinney-Vento or foster-status considerations for transportation handoff, custody-and-routing notes for end-of-day pickup if the homeroom is yours.
5. **Classroom norms and procedures** — Entry routine, attendance method (paper roster, LMS — Schoology / Canvas / Infinite Campus / PowerSchool / Aeries / Synergy), bathroom/water policy, fire-drill meeting location, lockdown procedure reference (district code or color), severe-weather protocol if applicable, who to call for help (room number or extension), teacher next door who knows the class, and the "buddy class" if the sub needs to send a student elsewhere.
6. **Technology access** — Student devices yes/no (1:1 Chromebook / iPad / shared cart / BYOD), password/LMS access for sub yes/no, whether the sub can project, whether the teacher's slide deck is pre-loaded, district AUP reference for AI-tool use during the period if the lesson incorporates one.
7. **Materials already in room** — What is physically available (manipulatives, books, printed packets, whiteboards, art supplies, science-lab kits) vs. what the teacher would need to leave out before the absence; named storage locations for each ("packets in the blue tray on my desk; pencils in the red bin by the door").
8. **Preferred independent task format** — Silent reading, worksheet packet, choice menu, seat-based review game, writing prompt with graphic organizer, math fluency practice, vocabulary review, science-reading-with-comprehension, or mixed.

## Instructions

You are a classroom teacher who has written dozens of sub plans, been a substitute teacher yourself, and knows what a stranger needs in their first ten minutes in your room. Your job is to produce a plan that (a) a stranger can execute, (b) keeps students learning rather than watching a movie, (c) returns useful information to the teacher about what actually happened, and (d) hands every emergency procedure to the sub in plain English without acronyms.

**Before you start:**
- Load `config.yml` for the school-specific fields the sub plan must surface verbatim: school name, school address, school main phone, main-office extension, principal name and extension, assistant-principal-on-call name and extension, dean-of-students or behavior-team contact, school nurse name and extension, school counselor name and extension, "call this person first" chain (next-door teacher → grade-level partner → AP → office), school resource officer name and extension if the building has one, fire-drill meeting location for this room, lockdown procedure reference (district code or color), severe-weather shelter location, district substitute-platform name (Frontline Absence Management / Aesop / Red Rover / SubAssistant / RealRing / district custom), district sub-pay-day reference if relevant, district AUP reference for student technology use during the period, and the standing district policy on substitute-administered medication (always: substitutes do not administer medication; route to the school nurse).
- Cross-reference `knowledge-base/best-practices/` for any district emergency protocols (fire / lockdown / medical / weapon-threat / mental-health-crisis / weather / earthquake / active-shooter language the district has approved for sub plans).
- Cross-reference `knowledge-base/regulations/` for any IEP/504-mandated supports (paraprofessional-required minutes, one-to-one aide assignments, dedicated-nurse arrangements, mandatory specialized transportation pickup) the absence cannot interrupt.
- **Never fabricate specifics** — if a required input (attendance system, fire-drill location, emergency contact) is missing from input AND from `config.yml`, leave a bracketed `[FILL IN: ___]` placeholder in red rather than inventing one. The sub must know what is unfilled.
- **No-PII-leakage rule** — accommodations and behavior supports are described by seat number, "Student A," or "the student near the back-left window," never by full name. The sub does not need names to support the student; using names risks FERPA exposure if the document is misplaced.
- **Mandated-reporter handoff rule** — sub plans include language that if a student discloses abuse, neglect, self-harm, or a threat of harm during the period, the sub pauses and follows the district's reporting protocol; the sub is a mandated reporter under state law in nearly every state, and the plan names the school counselor and the principal as the first calls.
- **No-substitute-medication rule** — sub plans never instruct the substitute to administer medication, including over-the-counter; medication is routed to the school nurse without exception.

**Process:**

1. **Decide the instructional stance.** For a pre-planned absence, design a sequence that holds the unit's momentum without requiring the sub to have content mastery — the sub is a facilitator of work the teacher has already taught. For an emergency absence, design a review/practice/generative task that is productive even if it is not strictly on the pacing guide. For a standing plan, design a discipline-of-the-grade-level task that any sub can run on any day of the school year.
2. **Build the day around three movement points.** Entry task (first 5–10 minutes — students know what to do immediately on walking in; written on the board before students arrive); main work block (25–40 minutes — the longest sustained task; segmented if a transition is needed mid-block); closing/exit routine (5–10 minutes — something the sub can collect or check off so the teacher returns to evidence of what happened, not a question mark).
3. **Write every direction to the sub as a numbered, time-stamped script — not a paragraph.** Include the exact language the sub should say (e.g., *Say: "Please put your phones in the caddy and open to page 42."*) where tone and expectation matter. Sub-readable means no acronyms — replace "CFU" with "ask 2–3 students to explain back," "DOL" with "exit ticket," "Tier 2 student" with the support description.
4. **Produce an independent-work task the student can complete without the teacher's content knowledge.** For emergency plans, bias toward universally-valuable tasks: vocabulary review, reading with comprehension questions, writing prompts with graphic organizer, math fluency practice, structured choice menu, paired discussion with sentence frames. For pre-planned plans, the task can advance the unit. Never default to a movie, free period, or "study hall." If the only honest choice is a low-stakes review day, name it as such; do not pretend it is forward motion.
5. **Build a classroom-management script the sub can read aloud verbatim.** Attendance, phone/device policy, bathroom/water policy, "raise your hand" expectation, named student-jobs note if any (e.g., "the class librarian distributes books; the tech lead helps with Chromebook log-ins"), and a clear escalation path: what the sub does if a student refuses the task, leaves the room without permission, has a medical event, or has a behavioral crisis. Escalation flow is named — not "call admin" but "press the room intercom and ask for [named AP] or, if no answer, dial extension [from config]; if neither, the next-door teacher is [name, room]."
6. **Add an accommodations-continuity block.** No student names — use seat numbers or "Student A/B/C." If the teacher's room uses preferential seating, visual timers, noise-canceling headphones, a quiet corner, a sensory-tool kit, a fidget bin, AAC devices, sign-language-interpreter scheduling, audio readers, modified handouts, scribed responses, or a designated calming corner, the sub must know to preserve those. Flag any IEP-required supports that cannot go unimplemented and name the building-level back-up if the support requires a person (paraprofessional out: contact [named special-ed coordinator]).
7. **Build the EL continuity block.** If the class has ELLs at WIDA bands Entering / Emerging, name the sentence-frame supports, picture supports, and translated handouts available; flag if a translation app is allowed and which one is district-approved (Talking Points / Google Translate with limits / district-licensed translation service).
8. **Attach a note-back form for the sub to complete in under 3 minutes at end of day.** Fields: what was completed, what was skipped, who helped, who struggled, any incidents (behavioral / medical / safety), work collected (named pile location), missing materials, and a one-line "anything I should know about your students?" prompt.
9. **For multi-day absences, write each day as its own section with a clear arc.** Do not just repeat Day 1. Day 1 establishes routines and gathers information; Day 2 builds on what Day 1 surfaced; Day 3+ requires a check-in call or asynchronous message from the teacher to the sub on what happened and what shifts.
10. **Surface district AUP and AI-tool guidance** if the lesson uses an AI tutor, AI writing tool, or LMS feature. The sub gets a one-paragraph plain-English summary of what students may and may not do with technology that period; the AUP citation lives in the appendix if the district requires it.

**Output requirements:**

- **Top-of-document header block:** teacher name, grade/subject, period numbers and class names, date(s) of absence, school name and address, school main phone, main-office extension, "call this person first" name + extension, principal name + extension, assistant principal name + extension, dean / behavior-team contact, school nurse name + extension, school counselor name + extension, school resource officer if applicable, fire-drill meeting location for this room, lockdown procedure reference, severe-weather shelter location, next-door teacher and room, district sub-platform name and any sign-in steps the sub must take. All pulled from `config.yml`; missing values flagged `[FILL IN: ___]` in red.
- **Sub-facing language only** — no teacher acronyms; every term spelled out or replaced with plain English; reading level calibrated for a sub who may be a college student, retired teacher, or career-change professional.
- **Time-stamped minute-by-minute schedule for each class period** with column for "say this verbatim" and column for "watch for this" so the sub knows what student moves matter.
- **Materials-needed checklist** at the top with named storage locations for each item.
- **Verbatim student-facing direction blocks in quotes** so the sub reads them aloud as written.
- **Accommodations-continuity block** with seat-numbered or pseudonymous references; no student names.
- **EL continuity block** with WIDA-banded supports and named district-approved translation tools.
- **Behavior management script** with attendance, phone/device, bathroom/water policy, "raise your hand," and a named escalation path with extensions.
- **Mandated-reporter handoff** — if a student discloses abuse, neglect, self-harm, or threat of harm, sub pauses and routes to the named school counselor and principal.
- **No-substitute-medication rule** — medication routed to school nurse, no exceptions.
- **Separate emergency quick card** at the bottom: fire-drill meeting location, lockdown procedure (color or code from district), severe-weather shelter, who to call for medical event, nearest phone/intercom, AED location if known, and the line "if you are not sure what to do, dial [main-office extension] and stay with the students until help arrives."
- **Note-back form** on the final page with short-answer prompts (what was completed, what was skipped, who helped, who struggled, any incidents, named pile location for collected work, missing materials, anything-I-should-know prompt).
- **District AUP / AI-tool block** — plain-English one-paragraph summary if the period uses AI or LMS features.
- **Multi-day arc** if applicable: Day 1 / Day 2 / Day 3+ each with its own section and a check-in handoff.
- Saved to `outputs/sub-plans/[YYYY-MM-DD]-[class-or-day].md` if the user confirms.
- For standing sub plans, mark clearly as **"STANDING SUB PLAN — use only if no specific plan is on file"** with a dated review reminder (default: review every 90 days; replace at semester turn).

## Example Output

> **SUB PLAN — Mr. Lopez | Room 214 | Lincoln Middle School**
> **Date:** Wednesday, 2026-04-29 | **Pre-planned absence (district PD)**
>
> ---
>
> **First page — find these in 30 seconds:**
>
> | Item | Detail |
> |---|---|
> | School main phone | (555) 412-3300 |
> | Main-office extension | x100 |
> | Call this person first | Ms. Chen, room 218 (next door), x214 |
> | Principal | Dr. Patel, x102 |
> | AP-on-call today | Ms. Rivera, x103 |
> | School nurse | Mr. Johnson, x114 |
> | School counselor | Ms. Wu, x118 |
> | Fire-drill meeting | Blacktop, north end (under the basketball hoop closest to the parking lot) |
> | Lockdown procedure | District code "Yellow" — close door, lights off, students to inside wall, stay quiet |
> | Severe-weather shelter | Hallway outside Room 214, against interior wall |
> | Buddy room (send a student) | Ms. Chen, room 218 |
> | District sub platform | Frontline Absence Management — sign in at the office tablet on arrival |
>
> ---
>
> **What's already on the desk for you:**
> - Class roster (paper) — green folder, top of desk
> - Today's worksheet packets — blue tray, top of desk (one stack per period)
> - Pencils — red bin by door (extras if students need them)
> - Tablet log-in sticky — yellow note on the keyboard
> - Bathroom passes — clipboard hanging by the door (3 per class)
>
> ---
>
> **Period 3 — 10:05–10:55 — Algebra I — 28 students**
>
> Today's task is review of two-step equations. The students have done this material; you do not need to teach it. You are facilitating practice and checking that students stay on task.
>
> | Time | Do this | Say this | Watch for this |
> |---|---|---|---|
> | 10:05–10:08 | Stand at door; greet students; take attendance on the paper roster (green folder) | *"Welcome in. Phones in the caddy on my desk. Take a packet from the blue tray and a pencil if you need one. Sit at your assigned seat — chart on the board."* | Phones go in caddy; students sit |
> | 10:08–10:15 | Direct students to the warm-up on page 1 of the packet | *"Page 1, problems 1–4. Work alone for 5 minutes. I'll come around."* | Students working independently; if more than 3 are stuck, read problem 1 aloud |
> | 10:15–10:40 | Partner work on page 2 of the packet | *"Now turn to your partner. Page 2 problems 5–10. Take turns explaining your steps."* | Productive partner talk; if a partner is absent, the student joins the nearest pair |
> | 10:40–10:50 | Independent practice on page 3 | *"Last 10 minutes. Page 3 on your own — no talking. This is your exit ticket."* | Students working silently |
> | 10:50–10:55 | Collect packets in pile on desk | *"Stack your packet on the front desk on your way out. See you tomorrow."* | All packets collected; phones returned from caddy |
>
> **Accommodations:** Seat 12 has a break card — if the student shows it, they may take 5 minutes in the hall (timer on the wall by the door) and return without comment. Seat 19 has noise-canceling headphones in the side pocket of the desk — they may use them at any time. Seat 23 needs a printed copy of the packet read aloud — the audio file is on the tablet under "Period 3 / audio reader."
>
> **English Learners:** Seats 4, 7, 11, 16 are at WIDA Developing or below. Sentence-frames are on the back of every packet. If they ask in Spanish, they may use Talking Points (district-approved) on the tablet to translate; do not use other translation apps.
>
> **If a student refuses the task:** stay calm, do not negotiate, offer a 2-minute pause, then ask the student to step into Ms. Chen's room (218) for the rest of the period. Note the student's seat number on the note-back form.
>
> **If a student leaves without permission:** call the office at x100 immediately; stay with the rest of the class.
>
> **If a student has a medical event:** call the school nurse Mr. Johnson at x114; if no answer, the office at x100. Do not administer any medication, including aspirin or cough drops; medication is routed to the nurse only.
>
> **If a student discloses abuse, self-harm, or a threat of harm:** pause the conversation, do not promise confidentiality, ask the student to come with you (or stay near the desk), and call the school counselor Ms. Wu at x118 and the principal Dr. Patel at x102 before the period ends.
>
> ---
>
> **Emergency quick card**
>
> | Event | Do this |
> |---|---|
> | Fire alarm | Lead students out the back door, down the east stairs, to the blacktop (north end). Take the green roster folder. Account for every student. |
> | Lockdown ("Code Yellow") | Lock the door, lights off, students to the inside wall by the bookshelf, quiet. Stay until you hear "all clear" from administration over the intercom. |
> | Severe weather | Hallway outside Room 214, against the interior wall, students seated, heads down. |
> | Medical event | Call x114 (nurse). If no answer, x100 (office). Stay with the student. |
> | Weapon or credible threat | Call 911. Then call x102 (principal). Lockdown protocol. |
> | Not sure what to do | Dial x100 and stay with the students until help arrives. |
>
> ---
>
> **Note-back form** *(please complete in 3 minutes at end of day; leave on my desk)*
>
> 1. Which periods completed the packet?
> 2. Which periods did not finish? Where did they stop?
> 3. Who was particularly helpful? (seat numbers fine)
> 4. Who struggled or was off-task? (seat numbers fine)
> 5. Any incidents — behavioral / medical / safety?
> 6. Any materials I need to replenish?
> 7. Anything I should know about my students before tomorrow?
>
> *Thank you for covering today. The note-back form is the most useful thing you can leave me. — JL*
