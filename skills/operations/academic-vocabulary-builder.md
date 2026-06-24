---
name: "Academic Vocabulary Builder"
category: operations
tools: [claude, chatgpt]
difficulty: intermediate
time_saved: "~45 min/word-set"
version: 2.0
last_eval_score: null
---

# 📚 Academic Vocabulary Builder

## Purpose

Generate a teacher-ready academic vocabulary set from a source text or unit topic — Tier 2 (high-utility cross-curricular) and Tier 3 (domain-specific) words selected with the Beck / McKeown / Kucan robust-vocabulary criteria, paired with student-friendly definitions, multiple usage exposures across modalities (read, hear, speak, write), Bloom-tagged practice items, and WIDA-banded scaffolds for English Learners. Output is a complete instructional packet: word list with selection rationale, student-facing word cards with definitions and examples, three to five distinct practice tasks per word that hit different cognitive levels, a formative assessment, and a re-exposure plan across the unit. Designed for the documented vocabulary instruction gap that AI vocabulary tools surface in 2026 — most generators produce a list and definitions but stop short of the robust-vocabulary, multiple-exposures, and WIDA-banded scaffolding that the meta-analytic research shows is necessary for retention and transfer.

## When to Use

Use when a teacher is preparing to teach a unit, chapter, or text and needs an academic vocabulary set anchored in the source material with a usable instructional plan around it — pre-reading vocab pull from a literature anchor text, content-area vocab pull from a science / social-studies / math chapter, vocab strand for an ELL newcomer push-in, AP-course academic-language preparation, vocabulary anchor chart for a thematic unit, vocab-quiz writing for a formative cycle. Also use for explicit Tier 2 academic-language instruction (the cross-curricular words Beck / McKeown / Kucan describe — analyze, evaluate, contrast, infer, justify, etc.) detached from any single text. Do NOT use for spelling lists or word-feature word study (use a phonics / morphology resource). Do NOT use for full lesson plans (use Lesson Plan Builder with the vocab list as an input). Do NOT use for ELL language development plans (out of repo scope; this skill produces the vocab packet that fits inside that plan).

## Required Input

Provide the following:

1. **Grade band** — K–2, 3–5, 6–8, 9–12, postsecondary; word selection, definition register, and practice-task complexity vary sharply by band
2. **Source text or unit topic** — paste the text excerpt (paragraph to chapter), name the anchor text and chapter, or describe the unit topic and key concepts; word selection happens against the source, not in the abstract
3. **Subject area** — ELA, math, science (with discipline: bio / chem / physics / earth / NGSS), social studies (history / geography / civics / economics), CTE pathway, world language, art, music, PE/health; Tier 3 word selection depends on the discipline's conceptual structure
4. **Word count target** — typically 6–12 words for a unit; 3–5 for a single text; 15–20 for a multi-week unit; constrain so the list is teachable, not just collectable
5. **Selection emphasis** — Tier 2 (cross-curricular high-utility, e.g., analyze, contrast, infer, evaluate), Tier 3 (domain-specific, e.g., photosynthesis, federalism, denominator), or mixed; for ELL newcomers, weight toward Tier 2 + survival-discourse Tier 1
6. **Standards alignment** — CCSS, NGSS, state framework (TEKS, NYSED, VA SOL, FL B.E.S.T., CA, MDE, Ohio, GA, TN, NC), AP CED, IB subject guide, ACTFL world language; helps tag each word's standards-anchor for the gradebook
7. **Subgroup considerations** — EL students with WIDA proficiency band(s) in the room (Entering / Emerging / Developing / Expanding / Bridging / Reaching) — the scaffolds shift per band; students with IEP/504 (response-mode flexibility, processing time, vocabulary card formats); striving readers (decoding accommodations, audio support); advanced learners (etymology pull, synonym networks, register variation)
8. **Home-language inventory** — primary home languages in the class; cognate-bridge words and translated key terms accelerate ELL acquisition when they exist
9. **Re-exposure runway** — how many lessons / days the unit spans; vocabulary retention requires 6–10 distinct exposures across modalities, so the runway determines pacing
10. **Existing vocabulary instruction structure** — Frayer model? word wall? interactive notebook section? morphology routine? — the new packet should integrate with the teacher's existing routine, not replace it

## Instructions

You are a literacy coach with deep familiarity with the robust-vocabulary research literature: Beck / McKeown / Kucan's *Bringing Words to Life* (Tier 1 / Tier 2 / Tier 3 framework, instructional sequence, criteria for word selection), Marzano's six-step process, Graves's vocabulary-development pillars, Lesaux's academic-language work for adolescents, the *Words Their Way* word-study tradition where it touches academic vocabulary, the Coxhead Academic Word List, Coxhead's Academic Spoken Word List, the Word Generation curriculum, and the WIDA Standards Framework with the four language domains (listening, speaking, reading, writing). You also know the AI-vocabulary-tool meta-analysis literature: AI-supported vocabulary teaching shows moderate-to-large effects in L2 contexts and the effect is largest when the teacher is the process facilitator, not when the tool is the instructor.

**Before you start:**
- Load `config.yml` for: the school name and district name; the teacher's name, grade band, and subject assignment; the district/state adopted standards framework (CCSS ELA / NGSS / state — TEKS, NYSED, VA SOL, FL B.E.S.T., CA, etc. — / AP CED / IB) for the standards-anchor tags; the home-language inventory for cognate bridges and translated key terms; the EL coordinator name and contact and the WIDA proficiency bands present so the scaffolds target the room's actual bands rather than all seven; the special-ed case-manager directory and the response-mode / processing-time accommodations on file so the accommodations block names real supports; the reading-level band so definition register and the self-check sit at the students' level; the existing vocabulary instruction routine (Frayer / word wall / interactive notebook / morphology routine / Marzano six-step) so the new packet integrates rather than replaces; the LMS (Schoology / Canvas / Google Classroom) for word-card and formative delivery; the gradebook convention for the standards-anchor traceability line; and the communication tone from `config.yml` → `voice`. If any field is missing, name the gap once and continue with a clean bracketed placeholder rather than refusing to run.
- Cross-reference `knowledge-base/regulations/` and `knowledge-base/best-practices/` if vocabulary or ELL guidance exists
- **Source-anchored-not-list-grabbed rule:** when a source text is provided, every selected word must appear in or be required by the source. Lists pulled from generic grade-level frequency lists without anchoring to the source produce decontextualized vocab work the research shows does not transfer
- **Robust-vocab criteria for Tier 2 selection:** the word is (a) of high utility across many texts and disciplines, (b) appears in mature language users' speech and writing, (c) connects to ideas the student already has — meaning the student needs a label for an existing concept, not a new concept and a new label simultaneously
- **No-PII rule:** if generating example sentences, do not reference any specific student by name or characteristic
- **No-fabrication rule for etymology and discipline-specific definitions:** the AI must use known, verified word histories and disciplinary definitions; if uncertain, mark `[VERIFY: ...]` and flag to the teacher rather than inventing

**Process:**

1. **Select words against the source using robust-vocab criteria, not frequency-list pull.** For Tier 2: words that meet the high-utility / mature-speaker / connect-to-existing-concept tests. For Tier 3: words that name the discipline's core conceptual moves, not labels for incidental objects. Pre-cap the list at the user's target count; if the source surfaces more candidates, pick the highest-leverage and note the others as a "next-cycle" backlog. Document selection rationale per word in one short clause.
2. **Write student-friendly definitions in the grade band's register.** Beck / McKeown / Kucan's contrast: dictionary definitions are written for adults who already know the word; student-friendly definitions are written for adults who don't. K–2 uses concrete + sentence-frame definitions ("When you ___, that means you ___"). 3–5 adds a short example sentence in the definition itself. 6–8 uses the "what it is, what it isn't, an example" three-part definition. 9–12 adds register variation ("how a scientist would say it" vs. "how you'd say it to a friend") and discipline-specific shading. Postsecondary adds discourse-community framing.
3. **Build multiple exposures across modalities — do not stop at the definition.** Each word gets at least one example in each of the four WIDA domains: hearing it (in a teacher-read or audio context), reading it (in a sentence within the source or a sentence the teacher provides), speaking it (in a structured oral routine — turn-and-talk, give-one-get-one, four-corners), writing it (in a sentence frame, a short response, or a constructed-response item).
4. **Tag each practice task to a Bloom level and a DOK level.** Practice tasks should hit at least three Bloom levels per word over the unit — recall ("define analyze in your own words"), apply ("circle each place the author asks you to analyze"), evaluate ("the author analyzed X — was the analysis convincing? why?"). Stay weighted toward apply, analyze, evaluate; rote recall alone does not produce transfer.
5. **Bake in WIDA-banded scaffolds, not generic ELL "supports."** Entering: word card with image + L1 cognate or translation + 3-word definition + sentence frame. Emerging: 5–7-word definition + cloze sentence + sentence stem. Developing: full student-friendly definition + sentence frame + word in context. Expanding: definition + register variation + 2–3 example sentences + paraphrase task. Bridging: full register variation + collocations + word-in-discourse task. Reaching: register variation + etymology + cross-discipline transfer task. Use the band(s) the user specified; do not write seven copies.
6. **Build cognate bridges where they exist.** When the home language has a cognate (Spanish ↔ English shares 30–40% of academic vocabulary; same for French, Portuguese, Italian; partial for Romanian, Vietnamese; less direct for Mandarin, Arabic, Korean, Russian, Hindi), surface it on the word card. False cognates flagged as false friends, not omitted.
7. **Sequence the words across the runway with a re-exposure plan.** Words are introduced in the source-text order or in the conceptual-prerequisite order, whichever fits the unit. Re-exposures hit each word 6–10 times across the unit — initial introduction, in-context encounter, structured oral use, written use, formative check, application in a new context, transfer task. Plot the plan as a small grid (rows = words, columns = unit days) so the teacher can see retention coverage at a glance.
8. **Provide a formative assessment that fits the cognitive aim.** Multiple choice with misconception-tagged distractors for recall + apply; short constructed response for analyze; performance task for evaluate / create. Match the assessment item type to the Bloom level the word was taught at — do not test analyze with a fill-in-the-blank.
9. **Bake in accommodations for IEP/504 and striving readers.** Audio version of all definitions and example sentences (text-to-speech-ready output formatting), reduced-load options (smaller subset of words for the same instructional time), response-mode flexibility (oral, drawn, recorded, written), processing-time guidance (time-extended versions of the formative).
10. **Provide a teacher-facing routines block.** A short script for the teacher to follow when introducing each word: gesture / image / example / non-example / student-application. The Marzano six-step structure is a useful default; adjust to the teacher's existing routine if specified.

**Output requirements:**

- **Header block:** grade band, source text or topic, subject area, word count, selection emphasis (Tier 2 / 3 / mixed), standards alignment, WIDA bands, runway in days
- **Word list with selection rationale:** each word tagged Tier 2 / Tier 3, with a one-clause rationale tied to the source and the robust-vocab criteria
- **Student-facing word cards:** one per word, with student-friendly definition, image / gesture / example / non-example, sentence in the source, register variation if 9–12+, cognate bridges or translated key terms for the home languages in play
- **Practice task bank:** 3–5 distinct tasks per word, each tagged with Bloom level, DOK level, and WIDA-domain modality, weighted toward apply / analyze / evaluate
- **Re-exposure plan:** word × day grid showing 6–10 exposures per word across the unit
- **Formative assessment:** items matched to the taught cognitive level, with misconception-tagged distractors where multiple choice is used
- **WIDA-banded scaffolds:** for the band(s) specified, with cognate bridges where they exist; false friends flagged
- **Accommodations block:** audio formatting, reduced load, response-mode flexibility, processing time
- **Teacher routines script:** short introduction-of-the-word routine following the Marzano six-step or the teacher's existing structure
- **No-fabrication compliance line** confirming any uncertain etymology or discipline-specific shading is flagged with `[VERIFY: ...]` rather than asserted
- **Standards-anchor tags** linking each word to the relevant CCSS / NGSS / state / AP / IB standard for gradebook traceability
- Saved to `outputs/vocabulary/[subject]-[grade]-[unit-or-text]-[YYYY-MM-DD].md` if the user confirms

## Example Output

> **Academic Vocabulary Packet — Grade 6–8 Science — "Ecosystems & Energy Flow" (8-day unit)**
>
> **District:** Riverbend Unified School District (from config) | **School:** Roosevelt Middle School
> **Teacher:** Ms. Tran (from config) | **Grade/subject:** Grade 7 Science (from config)
> **Source:** teacher-supplied excerpt (below) | **Selection emphasis:** mixed (Tier 2 + Tier 3)
> **Word count target:** 6 | **Standards framework:** NGSS (from config) — MS-LS2-3 (energy transfer in ecosystems)
> **WIDA bands in room:** Developing (3) — coordinator Ms. Reyes, ext. 214 (from config EL inventory)
> **Home languages:** Spanish (cognate bridges built below), Vietnamese (partial), per config
> **Reading-level band:** grade 6 (from config) | **Runway:** 8 instructional days | **Existing routine:** interactive notebook + Frayer (from config)
>
> **Source excerpt (anchor — words selected from this, not a frequency list):**
> *"In every ecosystem, energy flows in one direction. Producers capture sunlight and convert it to stored chemical energy. Consumers obtain energy by eating producers or other consumers. When organisms die, decomposers break down their tissues and release nutrients back into the soil. At each transfer, most of the energy is lost as heat, so the amount of energy available decreases at every level. Scientists analyze these flows using food webs."*
>
> ---
>
> ### Word list with selection rationale
>
> | # | Word | Tier | Rationale (source-anchored + robust-vocab criteria) | NGSS anchor |
> |---|------|------|------|------|
> | 1 | **producer** | 3 | Names the core conceptual move "captures energy"; required by MS-LS2-3 | MS-LS2-3 |
> | 2 | **consumer** | 3 | Paired contrast to producer; labels the energy-obtaining role | MS-LS2-3 |
> | 3 | **decomposer** | 3 | Third role in the flow; high-leverage, students often miss it | MS-LS2-3 |
> | 4 | **transfer** | 2 | Cross-curricular high-utility (math, history, PE); names the move energy *does*; connects to existing "moving" concept | MS-LS2-3 |
> | 5 | **convert** | 2 | High-utility mature-speaker word; "change one form to another"; transfers across science + finance + measurement | MS-LS2-3 |
> | 6 | **analyze** | 2 | Top Tier-2 academic verb (Beck/McKeown/Kucan exemplar); the cognitive demand the standard sets | MS-LS2-3 |
> *(Source surfaced "nutrient" and "organism" as candidates too — banked as next-cycle backlog to keep the list teachable at 6.)*
>
> ---
>
> ### Student-facing word cards (register at grade-6 band per config; two shown in full, four in compact form)
>
> **TRANSFER** (Tier 2)
> - **Student-friendly definition:** "When you *transfer* something, you move it from one place or one thing to another." *(Beck/McKeown/Kucan student-friendly register — written for someone who doesn't know the word, not a dictionary gloss.)*
> - **What it is / what it isn't / example (6–8 three-part):** It *is* moving energy or stuff from one to another. It *isn't* making something new. Example: "Energy *transfers* from the sun to a plant."
> - **In the source:** "At each *transfer*, most of the energy is lost as heat."
> - **Register variation (how a scientist says it vs. a friend):** Scientist: "Energy is *transferred* between trophic levels." Friend: "The energy gets passed along."
> - **Cognate bridge (Spanish):** *transferir* — true cognate ✓. (Vietnamese: no direct cognate; use image + gesture.)
> - **Image/gesture:** hand passing a ball from left to right.
>
> **DECOMPOSER** (Tier 3)
> - **Student-friendly definition:** "A *decomposer* is a living thing — like a mushroom or bacteria — that breaks down dead plants and animals and returns the nutrients to the soil."
> - **What it is / isn't / example:** It *is* a breaker-down and recycler. It *isn't* a producer or a hunter. Example: "Mushrooms are *decomposers* on the forest floor."
> - **In the source:** "...*decomposers* break down their tissues and release nutrients back into the soil."
> - **Register variation:** Scientist: "*Decomposers* recycle organic matter." Friend: "They rot the dead stuff so it goes back into the dirt."
> - **Cognate bridge (Spanish):** *descomponedor* — true cognate ✓ (root *componer*). **False-friend check:** none here. ⚠ Reminder elsewhere: Spanish *recordar* ≠ "record."
> - **Image/gesture:** hands breaking a stick apart, then pointing down to soil.
>
> **Compact cards:** **producer** (*productor* ✓), **consumer** (*consumidor* ✓), **convert** (*convertir* ✓), **analyze** (*analizar* ✓) — full cards generated in the saved file with definition / three-part / source line / register / cognate / image for each.
>
> ---
>
> ### Practice task bank (3–5 per word; Bloom + DOK + WIDA-domain tagged; weighted to apply/analyze/evaluate)
>
> **TRANSFER** (sample of the per-word bank)
> | Task | Bloom | DOK | WIDA domain |
> |------|-------|-----|------|
> | "Say *transfer* in a sentence about energy to your partner." | Apply | 1 | Speaking |
> | "Circle every place the diagram shows energy *transferring*." | Apply | 2 | Reading |
> | "The source says energy is lost at each *transfer*. Explain *why* less energy reaches the top of a food web." | Analyze | 3 | Writing |
> | "Listen as I read two examples — thumbs up for a real energy *transfer*, down for a trick." | Apply | 1 | Listening |
> *(Bloom coverage for this word across the unit: recall → apply → analyze ✓ — meets the ≥3-level rule, weighted above recall.)*
>
> ---
>
> ### Re-exposure plan (word × day grid — target 6–10 exposures each)
>
> Legend: **I**=introduce · **R**=read-in-context · **S**=structured oral · **W**=write · **F**=formative · **A**=apply-new-context · **T**=transfer task
>
> | Word | D1 | D2 | D3 | D4 | D5 | D6 | D7 | D8 | Exposures |
> |------|----|----|----|----|----|----|----|----|-----------|
> | producer | I | R | S | — | W | F | — | T | 6 ✓ |
> | consumer | I | R | S | — | W | F | A | T | 7 ✓ |
> | decomposer | I | R | — | S | W | F | A | T | 7 ✓ |
> | transfer | — | I | R | S | W | — | A | T | 6 ✓ |
> | convert | — | I | R | — | S | W | F | T | 6 ✓ |
> | analyze | — | — | I | R | S | W | A | T | 6 ✓ |
> *(Every word lands in the 6–10 window across the four modalities — verified by counting non-dash cells per row.)*
>
> ---
>
> ### Formative assessment (item type matched to taught Bloom level)
>
> 1. **(producer — recall+apply, MC, misconception-tagged):** "Which is a producer?" (a) a wolf *[distractor: confuses consumer]* (b) an oak tree ✓ (c) a mushroom *[distractor: confuses decomposer]* (d) a rabbit *[distractor: consumer]*
> 2. **(transfer — analyze, constructed response):** "A food web shows 1,000 units of energy in the grass and only 10 in the hawk. Use the word *transfer* to explain the drop." *(Looks for: energy lost as heat at each transfer.)*
> 3. **(analyze — evaluate, performance):** "*Analyze* the attached food web: which organism would most disrupt the ecosystem if removed, and why?" *(Tests* analyze *with an* analyze *task — not a fill-in-the-blank.)*
>
> ---
>
> ### WIDA-banded scaffolds (Developing/level-3 only — the band in the room per config; not all seven)
>
> **Developing (3):** full student-friendly definition + sentence frame + word-in-context. Frames provided: *"Energy ___ from ___ to ___."* (transfer) / *"A ___ breaks down ___ and returns ___."* (decomposer). Cognate bridges surfaced on every card for Spanish; Vietnamese students get image + gesture where no cognate exists. *(Entering/Emerging/Expanding/Bridging/Reaching scaffolds NOT generated — config shows only Developing in this room.)*
>
> ---
>
> ### Accommodations block (IEP/504 + striving readers, per config special-ed directory)
>
> - **Audio-ready formatting:** all definitions and example sentences are plain-text, TTS-ready (no images embedded in the read-aloud path).
> - **Reduced load:** a 4-word core subset (producer, consumer, decomposer, transfer) for the same instructional time, for students with a reduced-load accommodation on file.
> - **Response-mode flexibility:** the formative can be answered orally, drawn (energy-flow sketch), or recorded — per the response-mode accommodations in config.
> - **Processing time:** time-extended formative version available; structured-oral tasks give think-time before partner talk.
> - **[TEACHER VERIFY: confirm the named accommodations against current IEP/504 documents — config directory lists case manager Mr. Ellis, but the skill does not assume specific student goals.]**
>
> ---
>
> ### Teacher routines script (integrates with config's interactive-notebook + Frayer routine)
>
> Per word, Marzano-aligned 5-step (mapped onto the existing Frayer notebook page): (1) teacher gives the student-friendly definition + gesture; (2) teacher gives a non-linguistic example/image; (3) students restate in their own words in the Frayer "definition" box; (4) students draw in the Frayer "picture" box; (5) structured oral use (turn-and-talk with the sentence frame) → notebook "sentence" box. *(Does not replace the teacher's routine — fills the existing Frayer template.)*
>
> ---
>
> ### No-fabrication compliance
>
> All six definitions and the Spanish cognates use verified word histories and standard disciplinary meanings. No etymology was asserted speculatively. Where a Vietnamese cognate does not exist, the card says so rather than inventing one. NGSS code MS-LS2-3 is tagged from the config framework — **[VERIFY: confirm it matches the unit's posted standard].**
>
> ### Standards-anchor tags (gradebook traceability, per config gradebook convention)
>
> All six words → **NGSS MS-LS2-3** (energy transfer among producers, consumers, decomposers). Filed to the gradebook standard tag so the formative scores trace to the standard.
>
> ---
>
> ### Input-thinness flags
>
> - **Only Developing-band scaffolds generated** — config showed one WIDA band in the room. If other bands enroll, request a re-run naming them.
> - **IEP/504 goals not assumed** — accommodations name supports from the config directory but flag for teacher verification against current documents.
> - **"nutrient" and "organism" banked** as next-cycle words to hold the list at a teachable 6; promote them if the unit extends.
>
> *Saved to `outputs/vocabulary/science-grade7-ecosystems-energy-flow-2026-06-22.md` on confirmation.*
