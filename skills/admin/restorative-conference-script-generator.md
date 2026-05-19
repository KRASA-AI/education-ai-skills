---
name: "Restorative Conference Script Generator"
category: admin
tools: [claude, chatgpt]
difficulty: intermediate
time_saved: "~60 min/conference"
version: 2.0
last_eval_score: null
---

# 🕊️ Restorative Conference Script Generator

## Purpose

Draft a facilitator script for a restorative conversation, classroom circle, or formal restorative conference following a harm incident — for use by a trained teacher, dean, counselor, or restorative-practices coordinator. The output includes the facilitator's preamble, the sequenced restorative questions for the person(s) responsible, the person(s) harmed, and supporters, an agreement-to-repair template, and follow-up checkpoints. It is explicitly scoped as a **draft for a trained facilitator** — not a substitute for certified training in restorative practice or a replacement for a formal mediation/Title IX/CPS process where one is required.

## When to Use

Use for Tier 2 responses to harm between students or between a student and staff where (a) both parties voluntarily agree to participate, (b) the facilitator has foundational training in restorative practice, and (c) the incident does not meet a threshold requiring a formal process (law enforcement, Title IX, CPS, IEP manifestation determination, or district-specific alternative-to-suspension protocols). Also use for proactive community-building circles, re-entry conferences after suspension, and staff-to-student repair after a relational rupture. Do NOT use for incidents involving weapons, sexual harm, credible safety threats, suspected abuse or neglect, or as a diversion from a required legal/Title IX/CPS process. Do NOT use to pressure a person harmed into participating — consent is foundational and must be explicit.

## Required Input

Provide the following:

1. **Incident summary** — Factual, observable description of what happened (not character assessment). Pseudonymize all names before entering — use "Student A," "Student B," "Teacher C."
2. **Parties** — Who was harmed, who caused harm, who else was affected (bystanders, family, class community). Note relationships (peer, teacher-student, cross-grade).
3. **Stage of the process** — Pre-conference (individual prep meeting), conference (facilitated gathering), or post-conference (follow-up/accountability check)
4. **Consent status** — Has each party individually and voluntarily agreed to participate? If no or unknown, the skill will produce a **pre-conference prep script only** and flag consent as prerequisite to any joint meeting.
5. **Facilitator training level** — Entry (classroom affective statements / community circles), Intermediate (Tier 2 conferences), Advanced (formal restorative conferences, IIRP-style). The depth and safeguards in the output scale with this.
6. **Ages and any known vulnerabilities** — Grade level(s), IEP/504 status with relevant considerations (e.g., communication supports), language access needs, trauma history flags (not detail — just "trauma-informed adaptations needed: yes/no")
7. **Setting** — Classroom, office, private room, outdoor space; time allocated; presence of family/guardians (required for most formal conferences involving minors)
8. **Desired outcome focus** — Understanding + acknowledgment, repair plan + actions, re-entry after suspension, relationship repair, or community norm-setting

## Instructions

You are a restorative-practices specialist trained in the IIRP Real Justice model and familiar with school-based adaptations (IIRP, CRJ, community-specific traditions such as Navajo peacemaking or Māori whānau conferencing where locally referenced). Your job is to produce a script that (a) honors the voluntariness of the process, (b) centers the person(s) harmed, (c) surfaces the impact of the harm before moving to repair, and (d) leaves space for the facilitator's professional judgment — the script is a scaffold, not a replacement for facilitator skill.

**Before you start:**
- Load `config.yml` for: the district's restorative-practices framework name (e.g., "IIRP Real Justice," "CRJ school-based circles," "district-developed model based on RP4SS"); the building-level restorative-practices coordinator name and contact (e.g., "Ms. Holloway, RP coordinator, ext. 142"); the dean / AP-on-call contact; the school counselor contact; the social worker / school psychologist contact; the Title IX coordinator name and contact (used in the escalation-routing block); the CPS / mandated-reporter call-line number and the district's mandated-reporter reminder language verbatim; the district's restraint-and-seclusion policy reference; the district's home-language inventory and translation-service vendor (used for the language-access block); the FACE / family-engagement office contact; the reading-level band for the district's parent-facing communications; the district's pre-conference-consent form filename if one exists; the discipline-data system in use (Educlimber, Branching Minds, Kickboard, Review360, Panorama, or paper log) for the follow-up checkpoint entry. If any of these are missing from `config.yml`, the skill names the gap once and continues with a placeholder rather than refusing to run.
- Reference `knowledge-base/best-practices/` for district-approved protocols if present
- **Consent check:** if the input indicates a party has not individually consented to participate, the output must be pre-conference-prep only. Do not generate a joint-conference script.
- **Mandated-reporter reminder:** include language that if the conference surfaces information meeting a mandated-reporting threshold (suspected abuse, neglect, credible threat of harm), the facilitator must pause the process and follow district reporting protocols — restorative practice does not supersede mandated reporting. The reminder uses the district's verbatim mandated-reporter language and CPS call-line number from `config.yml`.
- **No-fabrication rule:** do not invent facts about the incident, student identities, or prior relationships. Where detail is missing, leave placeholder language.

**Process:**

1. **Stage-match the output.** Pre-conference produces individual prep scripts: voluntariness conversation, what-happened-from-your-view, who-was-affected, what-do-you-need-to-feel-ready, what-outcome-would-feel-meaningful. Conference produces the joint script. Post-conference produces the accountability check script.
2. **Sequence the core questions.** Use the restorative-questions skeleton — (a) what happened, (b) what were you thinking at the time, (c) what have you thought about since, (d) who has been affected, (e) what do you think needs to happen to make things as right as possible — adapted to age and stage. Never lead with "why did you do it" — the model is behavior-and-impact focused, not motive-probing.
3. **Center the person harmed.** Questions for the person harmed come before questions for the person who caused harm in the joint conference sequence. The person harmed is never pressured to speak, accept an apology, or forgive. Every prompt for them includes an explicit pass option.
4. **Surface supporters.** Include a section for each supporter (family, chosen adult, peer advocate) with prompts that invite their observation of impact without letting them speak for the principal parties.
5. **Draft an agreement-to-repair template** — student-written language, signed by the parties involved, with concrete actions, timelines, and follow-up checkpoints. Not a punishment list. Not a contract to "never do it again." A short set of commitments tied to the harm and the relationships.
6. **Build in pauses and regulation supports.** Script in explicit breaks (water, movement, quiet) and flag emotional-regulation cues the facilitator should watch for. Scale these for younger students and for trauma-informed contexts.
7. **Language-access and accommodations.** If an input lists a language other than English as the family's home language, flag the need for a qualified interpreter (not a peer, not a family member if the conference involves minors). If a party has communication supports on an IEP, flag the need to continue those (AAC device, sign-language interpreter, additional time).
8. **Close with belonging.** The conference closes with a brief re-entry statement — what the classroom/community needs to do to welcome the person back — and a named next-touch date.
9. **Write the facilitator's voice, not the student's.** Do not pre-scripted student responses. Give the facilitator the questions and the pacing; the humans in the room provide the content.

**Output requirements:**

- **Stage banner at top:** pre-conference / conference / post-conference — scope limited accordingly
- **Consent and readiness check** box at the top the facilitator fills in for each party before proceeding
- **Preamble the facilitator reads aloud** (confidentiality scope, voluntariness, pass option, mandated-reporter boundary, time frame, ground rules)
- **Sequenced question blocks** for person(s) harmed, person(s) who caused harm, supporters — with facilitator instructions in brackets (e.g., "[Pause. Give as much time as needed. Do not fill silence.]")
- **Agreement-to-repair template** with blanks for student-generated language, timelines, and checkpoints
- **Follow-up checkpoint schedule** (e.g., 1 week, 4 weeks, 8 weeks) with questions for each
- **Safeguard callouts:** mandated-reporter reminder, Title IX / CPS / safety-threat escalation note, language-access requirement, accommodation continuity
- **Non-restorative fallback:** a named path if the conference is not the right process after all (referral to counselor, administrator, formal mediation)
- **DRAFT watermark** — "DRAFT — for facilitator review and adaptation; does not substitute for facilitator training"
- Trauma-informed, strengths-based language throughout — no shame-based framing, no public-confession framing
- All student references are pseudonymized (Student A, Student B) until the facilitator inserts real names locally
- Saved to `outputs/restorative/[incident-slug]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> **STAGE: CONFERENCE — Joint Restorative Conference Script**
> **DRAFT — for facilitator review and adaptation; does not substitute for facilitator training.**
>
> **District:** Riverbend Unified School District (from config) | **School:** Cesar Chavez Middle School
> **Framework:** IIRP Real Justice model (district adopted, from config) | **RP Coordinator:** Ms. Holloway, ext. 142
> **Facilitator training level:** Intermediate (Tier 2 conferences) | **Drafted:** 2026-05-12 | **Conference date:** 2026-05-15, 2:45–3:35 PM
> **Setting:** Counselor's conference room (private, round-table seating, water available, tissue box, regulation cards out) | **Time allocated:** 50 min
> **Stage banner scope limit:** This script is the joint-conference stage only. Pre-conference prep scripts for each party were run separately on 2026-05-08 (Student A), 2026-05-09 (Student B), and 2026-05-09 (Student B's caregiver).
>
> ---
>
> **Consent and readiness check** *(facilitator completes for each party at the door, before entering the circle)*
>
> | Party | Pre-conference prep complete? | Voluntary consent to proceed today? | Pass option understood? | Mandated-reporter scope explained? |
> |---|---|---|---|---|
> | Student A (person who caused harm) | ☐ Yes ☐ No | ☐ Yes ☐ No | ☐ Yes ☐ No | ☐ Yes ☐ No |
> | Student B (person harmed) | ☐ Yes ☐ No | ☐ Yes ☐ No | ☐ Yes ☐ No | ☐ Yes ☐ No |
> | Student B's caregiver (supporter) | ☐ Yes ☐ No | ☐ Yes ☐ No | ☐ Yes ☐ No | ☐ Yes ☐ No |
> | Student A's caregiver (supporter) | ☐ Yes ☐ No | ☐ Yes ☐ No | ☐ Yes ☐ No | ☐ Yes ☐ No |
>
> **If any box is "No," stop. Do not proceed to the joint script. Return to pre-conference prep with that party, or route to the non-restorative fallback (below).**
>
> ---
>
> **Preamble — facilitator reads aloud (≈2 min)**
>
> "Thank you all for being here. Before we start I want to name a few things so we are on the same page.
>
> First, you are here voluntarily. Each of you told me individually, this week, that you wanted to come. If at any point any of you wants to stop or take a break, we stop or take a break. No questions asked.
>
> Second, what is said in this room stays in this room — with one exception. If anything I hear tells me that someone is being hurt at home, or is in danger, or is thinking about hurting themselves or someone else, I have to follow our district mandated-reporter steps and call the people whose job it is to help with that. The mandated-reporter line for Riverbend Unified is (555) 412-7700, and I will tell you before I make any call. Restorative practice does not change that responsibility.
>
> Third, we are not here to figure out punishment. The school discipline process is separate. We are here to understand what happened, who was affected, and what — if anything — could make things as right as possible from here. The agreement we may write at the end is something each of you chooses to participate in, not a contract you are forced to sign.
>
> Fourth, you can pass on any question. You can also ask me to come back to a question later. The pass is a real option, not a polite one.
>
> Fifth, we will go in this order: Student B will be invited to share first, because Student B was harmed. Then Student A. Then supporters. We will pause when we need to. We have until 3:35 PM, but if we need to stop earlier, we will stop earlier.
>
> Any questions before we begin?"
>
> *[Pause. Wait for any questions. Do not move on until each party has had the chance to ask or pass.]*
>
> ---
>
> **Question block for Student B (person harmed)** *(≈10–15 min)*
>
> *[Facilitator note: Student B is offered the floor first and may pass on any prompt. Do not fill silence. Do not paraphrase Student B's answers back to them or to the room — let the words sit.]*
>
> 1. "Student B, in your own words, what happened from your view?"
> 2. "What were you thinking or feeling at the time it was happening?"
> 3. "What have you thought about or felt since?"
> 4. "Who else do you think has been affected by what happened? How?"
> 5. "What do you need today — from this conversation, from Student A, from the adults at this school — to feel like things are moving in a better direction?"
>
> *[Pause. Give as much time as Student B needs. Do not rush. If Student B passes on a prompt, say "OK, we can come back to that or leave it. Both are fine." Do not press.]*
>
> ---
>
> **Question block for Student A (person who caused harm)** *(≈10–15 min)*
>
> *[Facilitator note: Use the restorative-questions skeleton. Do NOT ask "why did you do it" — the model is behavior-and-impact focused, not motive-probing. If Student A starts to explain motive, redirect gently: "We're going to stay with what happened and who was affected, not why. Stay with me on that."]*
>
> 1. "Student A, in your own words, what happened?"
> 2. "What were you thinking at the time?"
> 3. "What have you thought about since?"
> 4. "Now that you have heard from Student B, who do you think has been affected? How?"
> 5. "What do you think needs to happen to make things as right as possible?"
>
> *[Pause. If Student A offers a defensive or minimizing response, do not argue. Reflect once — "I hear you saying _____. Is that what you mean?" — and then return to the next question. The conference is not a cross-examination.]*
>
> ---
>
> **Question block for supporters** *(≈5–8 min)*
>
> *[Facilitator note: Each supporter speaks to their observation of impact. Supporters do NOT speak for, defend, or accuse the principal parties. If a supporter begins to do so, redirect: "I want to make sure Student A / Student B can speak for themselves. Tell me what you have seen or noticed."]*
>
> For each supporter present, in turn:
>
> 1. "What have you observed or noticed about how this has affected Student B / Student A / the people around them?"
> 2. "What support do you think Student B / Student A needs right now?"
> 3. "Is there anything you would like to add before we move to next steps?"
>
> ---
>
> **Agreement-to-repair template** *(≈8–10 min)*
>
> *[Facilitator note: The agreement is student-written. The facilitator scribes; the students name the commitments. Do NOT propose commitments yourself. Do NOT pressure Student B to accept an apology. If Student B does not want a relational repair, the agreement can be a coexistence agreement — a set of practical commitments that allow both students to be in the same space without further harm.]*
>
> **What each of us is committing to:**
>
> *Student A:* _____________________________________________________
>
> *Student B:* _____________________________________________________
>
> **Concrete actions, with who and by when:**
>
> | Action | Who | By when | How we'll know it happened |
> |---|---|---|---|
> | | | | |
> | | | | |
>
> **What the adults at this school are committing to:** _____________________________________________________
>
> **Signed (or initialed) by each party:** _____________________________________________________
>
> *[Facilitator note: Signing is optional. If a party prefers an unsigned agreement, honor that. The commitment is what matters; the signature is a ritual, not a legal requirement.]*
>
> ---
>
> **Closing — facilitator reads aloud (≈2 min)**
>
> "Before we close, I want to name one more thing. The classroom and the lunchroom and the hallways at Chavez are shared spaces. What helps everyone feel like they belong here is what we are committing to today. Student B, what would it look like for you to feel welcomed back into shared spaces this week? Student A, what would it look like for you to take responsibility for that welcome?"
>
> *[Brief responses, not a second round of questions. Then:]*
>
> "We will check in again on [date — see follow-up schedule below]. If anything comes up before then that you want to talk about, you can come to me, to Ms. Holloway, or to your counselor. Thank you for being here."
>
> ---
>
> **Follow-up checkpoint schedule**
>
> | Checkpoint | Date | Who attends | Questions |
> |---|---|---|---|
> | 1 week | 2026-05-22 | Facilitator + Student A + Student B (separately, then briefly together if both opt in) | "How is the agreement going from your view?" "Is there anything that needs to change?" "Has anything new come up?" |
> | 4 weeks | 2026-06-12 | Facilitator + both students (jointly if both opt in; separately if not) | "What part of the agreement is working? What is not?" "What support do you still need?" |
> | 8 weeks | End-of-year wrap | Facilitator + RP coordinator (Ms. Holloway) review | Internal review: did the agreement hold? Was a re-referral needed? What did we learn? |
>
> *Entries logged in the district discipline-data system (Educlimber, per config) under restorative-conference outcome code RC-AGR; not entered as a discipline event.*
>
> ---
>
> **Safeguard callouts**
>
> - **Mandated-reporter reminder:** If at any point in the conference a party shares information meeting the Riverbend Unified mandated-reporter threshold — suspected abuse, neglect, credible threat of harm to self or others — the facilitator pauses the process, names the responsibility aloud ("I have to call this in. Here is what that will look like."), and follows district protocol. Call line: (555) 412-7700. Restorative practice does not supersede mandated reporting.
> - **Title IX escalation:** If the harm involves sexual misconduct as defined by the district Title IX policy, this conference is NOT the appropriate process. Stop, route to Title IX coordinator (Ms. Brennan, ext. 108, from config). Restorative work, if any, follows the Title IX process — not in place of it.
> - **CPS escalation:** If suspected abuse or neglect surfaces, route to the CPS call line above and notify the school social worker (Mr. Olufemi, ext. 119, from config).
> - **Safety-threat escalation:** If a credible threat of harm to self or others is named, route to the school psychologist (Dr. Ahuja, ext. 121, from config) for a same-day risk screen. The agreement-to-repair pauses until the screen is complete.
> - **Language-access requirement:** Student B's family has Spanish as the home language (from config home-language inventory). A qualified interpreter from the district translation-service vendor (Lenguaje Verde, from config) is scheduled for the supporter portion. Peers and family members are NOT used as interpreters when a minor is involved.
> - **Accommodation continuity:** Student A has a 504 plan with a sensory-tool kit; the kit is available on the table. Student B's IEP includes extended processing time for verbal questions; the facilitator builds in explicit pause time after each prompt for Student B.
> - **Restraint and seclusion:** Not in scope for this script. If a behavior emerges that would require physical intervention, the building behavior team takes over under Riverbend Unified policy BP-5144.1 (district restraint-and-seclusion policy from config). Facilitators do not physically intervene.
>
> ---
>
> **Non-restorative fallback**
>
> If any of the following happen, this conference is not the right process today:
>
> - A party withdraws consent or wants to leave
> - New information surfaces that meets a mandated-reporting threshold
> - A party experiences acute dysregulation that does not respond to break / regulation supports
> - The harm turns out to be different in scope than the pre-conference described (e.g., reported as verbal but actually involved physical or sexual contact)
>
> **Routing:**
> - Counselor: Ms. Park, ext. 117 (from config) — for immediate regulation support
> - Dean / AP-on-call: Mr. Castellanos, ext. 103 (from config) — for discipline-process resumption
> - RP coordinator: Ms. Holloway, ext. 142 (from config) — for re-scheduling or formal-mediation referral
> - Title IX coordinator: Ms. Brennan, ext. 108 (from config) — for any disclosure meeting Title IX scope
>
> ---
>
> **AI-use disclosure (for facilitator's working file, not for the discipline record)**
>
> This script was drafted with AI assistance for the facilitator's review and adaptation. The facilitator is the human author of the conference; the parties are the human authors of the agreement. The script was reviewed by the facilitator against this conference's pre-conference prep notes before use. Edit history is preserved in the facilitator's working file.
