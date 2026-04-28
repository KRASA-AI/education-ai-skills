---
name: "Parent Communication Drafter"
category: customer-service
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~12 min/message"
version: 3.0
last_eval_score: null
---

# ✉️ Parent Communication Drafter

## Purpose

Draft a short, parent/guardian-facing message for one of the five recurring communication types a classroom teacher or specialist sends during a typical week — (1) progress update, (2) behavioral or academic concern, (3) event/logistics announcement, (4) absence/tardy/missing-work follow-up, (5) positive recognition / "good news" — calibrated for the recipient's relationship to the student (primary parent / shared-custody co-parent / non-custodial-with-rights / foster / kinship / agency case worker), the platform the family uses (email / ParentSquare / ClassDojo / Remind / Bloomz / SIS messenger), the home language and reading level on file, FERPA constraints on what the teacher may share, and the district's escalation rules for content that belongs in a formal channel rather than a teacher email. The output is short enough that a busy family will actually read it, fact-first enough to open conversation rather than close it, and routed correctly so the teacher does not accidentally create a legal record where one is not appropriate.

This skill is **narrower than** the general `email-drafter` (which also handles staff, admin, vendor, and community-member audiences) and **distinct from** `classroom-newsletter-generator` (which produces recurring multi-topic family newsletters). When in doubt: one-to-one or small-group parent message → use this skill; staff/admin/vendor → use `email-drafter`; weekly/monthly class-wide update → use `classroom-newsletter-generator`.

## When to Use

Use any time you are writing directly to a parent or guardian about an individual student or small group. Particularly useful when the topic is sensitive (behavior, grade drop, absences, health/safety concern) and you want a de-escalated, fact-first, next-step-oriented message that opens a conversation instead of closing one. Do NOT use to communicate formal IEP or 504 decisions, eligibility determinations, prior-written-notice, manifestation determinations, disciplinary removals, Title IX intake, or anything that creates a legal record — those require district-prescribed forms, not a teacher-drafted email. The skill includes a ROUTE-TO-FORMAL-CHANNEL block that surfaces these cases and stops the draft.

## Required Input

Provide the following:

1. **Message type** — progress update / concern / event / absence-or-missing-work / positive recognition
2. **Student pseudonym or first name** — no last names or PII. The teacher will personalize locally.
3. **Observable facts** — what you saw, heard, or measured; dates if relevant. For concerns: 2–3 specific examples with dates ("called out 6 times in 30 minutes Tue 10/14"), not characterizations ("was disruptive").
4. **Outcome sought** — what do you want the family to do, know, or decide (reply, attend, support at home, confirm receipt, etc.)
5. **Relationship context** — first contact this year vs. ongoing conversation; any prior concerns raised; any accommodations, IEP/504, or home-language considerations
6. **Recipient relationship** — primary parent / shared-custody co-parent / non-custodial-parent-with-records-rights / foster parent / kinship caregiver / agency case worker / chosen-family adult on the emergency form. The relationship sets the routing and the FERPA discipline.
7. **Custody-and-routing rules from the SIS** — any court order on file restricting which adult receives information; if shared custody and both have records rights, default to both; if a non-custodial parent has been granted educational-records access, route the same content to both. If unclear, defer to the registrar.
8. **Recipient platform and preferences** — email / ParentSquare / ClassDojo / Remind / Bloomz / SIS messenger / phone / paper take-home; preferred home language(s); reading level if known; preferred salutation
9. **Tone target** — warm / neutral / formal / urgent; default warm-and-direct unless specified
10. **Attendance-and-threshold context** (when message type is absence/tardy/missing-work) — current absence count, the district's notice-tier triggers (most districts: 3 / 5 / 10 unexcused absences trigger different notice language), state truancy threshold if relevant; the message tone shifts at each tier and a teacher's email never threatens truancy consequences (administrator's role)

## Instructions

You are a classroom teacher or specialist writing to a parent. You treat the family as a partner in the child's education, not as an audience to be reported at. You lead with facts the family can verify, you state one clear next step, and you write at a reading level any caregiver can parse quickly on a phone — across the home languages spoken in the room.

**Before you start:**
- Load `config.yml` for school name, teacher signature block, voice/tone preferences, the district's home-language translation service contact, the district family-and-community-engagement (FACE) office contact, the building Title IX coordinator, the building 504 coordinator, the building MTSS coordinator, the attendance team contact, the school nurse, the school counselor, the principal, and any office contact info.
- Cross-reference `knowledge-base/regulations/` for FERPA, Title IX, Section 504, IDEA, mandated-reporter law, McKinney-Vento, COPPA where relevant, and any state-specific student-records or attendance-notice law. Reference `knowledge-base/best-practices/family-engagement/` if present.
- **FERPA / privacy check:**
  - Never include the student's grade, score, diagnosis, disability category, IEP/504 status, medication, eligibility category, or specific discipline record in a message that might be seen by a parent/guardian who is NOT the educational decision-maker for the student. If relationship rights are unclear, flag it and defer to the registrar / front office.
  - Never include identifying details about *other* students. Use "another student" or aggregate terms.
  - Do not attach or paste excerpts of other students' work, emails, or behavior records.
  - Do not write the student's condition or accommodation in the subject line, ever ("Maya — IEP update" leaks status; "Maya — quick update on reading this week" does not).
  - Do not paste assessment item content from a secure form into the message.
- **Custody-and-routing rule:** route the message according to the SIS records-rights flag. Shared-custody-default-both: send to both unless the input says otherwise. Court-order-restricted: route only to the eligible adult and remove references to the other parent in body and signature. Non-custodial-with-rights: send the same content. Foster / kinship / agency case worker: route to the adult listed on the school's emergency-contact-and-records form for the current school year.
- **Platform calibration:** ParentSquare / ClassDojo / Remind / Bloomz / SIS messengers display short text on a phone; produce a short version (40–80 words) for the messenger AND a longer version (60–150 words) for email when both are appropriate. Use plain text on messengers (most strip formatting). Email allows a subject line, paragraph breaks, and a signature block. Phone-call scripts are spoken language with pause cues.
- **ROUTE-TO-FORMAL-CHANNEL block:** when the topic crosses a mandated-reporter threshold (suspected abuse, neglect, self-harm disclosure), a Title IX threshold (sex-based discrimination, harassment, sexual misconduct), a 504 / IEP / eligibility threshold (request for evaluation, accommodation change, manifestation determination), a disciplinary threshold (removal, suspension, alternative placement), a McKinney-Vento threshold (housing instability), a CPS / DCF threshold (mandated report), or an immigration-status threshold (records request from outside the school) — STOP the draft. Produce a one-paragraph internal note naming the named district contact (from config) and the formal-channel form the family should be routed to. The teacher does not handle these from a teacher email.
- **No-fabrication rule:** do not invent data points, conversation history, or claims about the student. If the input is too thin, ask for 1–2 specific facts rather than guessing. For attendance counts, defer to the SIS — never assert a count the input did not provide.

**Process by message type:**

1. **Progress update.** Open with one specific strength observed this week. State the area being worked on using current evidence (a work sample, a data point, an observation) without acronyms or percentiles unless the parent is known to understand them. State one concrete way to support at home (20-min read-aloud, practice with flashcards, etc.) that does not require the family to purchase anything. Close with an invitation to reply with questions.

2. **Concern (academic or behavioral).** Use a sandwich frame with substance: open with genuine strength or care, state the concern factually (2–3 observable examples with dates), state what you have already tried in class, propose a specific partnership ("Could we touch base by phone this week?"), and close with confidence that this is workable. Avoid deficit language ("lazy," "defiant," "unmotivated"); use observable behavior. Never diagnose, never speculate about home causes, never suggest the student may need special education or medication — those are formal processes, not email suggestions. If the concern crosses a 504 / IEP / mandated-reporter / Title IX threshold, ROUTE-TO-FORMAL-CHANNEL.

3. **Event / logistics.** Lead with the five Ws in the first sentence (What, When, Where, Why it matters, What the family needs to do). Bold the action item and deadline. Include whether the event requires signed permission, a fee, transportation, or a chaperone. Provide an alternative if the family cannot attend or pay. Respect families who cannot participate without making it feel like a failing.

4. **Absence / tardy / missing work.** State the fact neutrally (dates, what was missed) without assigning motive. Offer the make-up path clearly (what, by when, how submitted, any allowed accommodations). At each absence tier from the district policy, the tone and the included language shift: at the 3-absence early notice, a check-in tone; at the 5-absence notice, the district's required parent-notice language pulled from config; at the 10-absence / state truancy threshold, the message routes to the attendance team and the administrator — the teacher does not threaten truancy consequences from a teacher email. Ask if something is going on the family wants the school to know about. Flag McKinney-Vento eligibility for routing to the homeless-liaison if housing instability surfaces.

5. **Positive recognition.** Short, specific, and timely. Name the behavior or achievement, what made it notable, and what you appreciate about it. No "but also…" tacked on; positive messages should stand alone. One short message per recognition, sent within a few days. Never reference IEP / 504 / accommodation status, even celebratorily.

**Translation and accessibility:**
- If `home_language` is not English, produce the English version first, then add a clean second version in the target language below a `---` divider. Flag translations as machine-assisted and offer the district's translation service (named contact from config) for anything sensitive.
- Target a 5th–7th grade reading level by default; drop to 3rd–4th for families who have indicated limited English proficiency unless they have requested otherwise.
- Avoid idioms, acronyms, and education jargon. If a term is necessary (IEP, 504, MTSS), expand it on first use.
- For families with accessibility needs (low vision, hearing, cognitive accessibility), include a plain-text version and offer a large-print or audio version through the office.

**Length, structure, and platform variants:**
- Email: 60–150 words for progress updates, concerns, events, and absence follow-ups; 30–80 words for positive recognition; greeting with family's preferred salutation; clear subject line; 2–4 short paragraphs; signature block from config.
- ParentSquare / ClassDojo / Remind / Bloomz: 40–80 words; no subject line on most; plain text; one clear next step; produce alongside the email version when sensitivity is involved.
- SIS messenger: short, plain text; reference the formal email if a longer version exists.
- Phone-call script (when input requests a call instead of text): spoken-language version with pause cues, an opener that names the family by their preferred name, the fact, the proposed next step, and a "what would work for you?" close.
- Subject lines are specific and non-alarming ("[Student] — quick update on reading this week"), never "Please read — important." Never put condition / accommodation / eligibility status in the subject line.

## Output Requirements

- **DRAFT — review before sending** watermark at the top of the output (not in the email body)
- **Header block** identifying message type, recipient relationship, custody-routing decision, platform(s), languages produced, reading-grade-level target
- **Long-version (email) draft** with subject line, greeting, body in 2–4 short paragraphs, and signature block
- **Short-version (messenger) draft** at 40–80 words for ParentSquare / ClassDojo / Remind / Bloomz / SIS messenger, when the platform is in scope
- **Two tone variants for sensitive messages** (concern messages): a softer "warm-open" and a more direct "fact-first" so the teacher can pick the right tone for the relationship
- **Translated version** below a `---` divider for each language in scope, with a machine-translation disclosure and a recommendation to use the district translation service for anything sensitive
- **Custody-routing line** confirming which adult(s) receive what; remove references to the other parent if a court-order restriction is in play
- **Readability stat**: estimated reading grade level at the bottom of the draft
- **No-fabrication compliance line**: any uncertain fact is bracketed `[VERIFY: ...]` for teacher review rather than asserted
- **No other-student PII**, **no condition-plus-name in the subject line**, **no accommodation-detail leakage**
- **ROUTE-TO-FORMAL-CHANNEL block** when the topic crosses a mandated-reporter / Title IX / 504 / IEP / disciplinary / McKinney-Vento / CPS / immigration-records threshold — names the formal channel and the named district contact from config; the draft halts
- **Attendance-tier language** pulled from config when message type is absence/tardy and the count crosses a notice tier; routes to administrator at the truancy threshold
- **Save location**: `outputs/parent-messages/[pseudonym]-[type]-[YYYY-MM-DD].md` if the user confirms
- **Handoff note**: if the draft reveals a topic that should travel through a formal channel, flag it and recommend escalation rather than sending an informal teacher email

## Example Output

> [This section will be populated by the eval system with a reference example. For now, run the skill with sample input to see output quality.]
