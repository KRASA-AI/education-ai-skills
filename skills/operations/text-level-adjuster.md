---
name: "Text Level Adjuster"
category: operations
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~45 min/passage"
version: 2.0
last_eval_score: null
---

# 📖 Text Level Adjuster

## Purpose

Rewrite a passage of text up or down to a target reading level — specified as a Lexile band, grade band, or **WIDA proficiency band** (Entering / Emerging / Developing / Expanding / Bridging / Reaching) — while preserving every factual claim, key concept, central argument, and standards-anchor from the source. The output is a ready-to-distribute, differentiated version of the same passage with student-facing scaffolds (bold tier-3 vocabulary, inline definitions where the level requires it, cognate bridges where the home-language inventory supports them) and a teacher-facing readability note. Designed to integrate with the rest of the repo — the WIDA banding mirrors `differentiation-planner` and `student-feedback-generator`; pairs with `academic-vocabulary-builder` when the passage is part of a vocabulary-rich unit.

## When to Use

Use when a mixed-ability class needs the same content at different reading levels, when an ELL or striving reader needs access to a grade-level text, when an advanced reader needs an elevated version that stretches vocabulary and syntax, or when a teacher needs a paired text set (high / on-level / supported) for a workstation rotation. Pairs naturally with `differentiation-planner` (which plans tasks) — this skill adjusts the source text itself. Pairs with `academic-vocabulary-builder` when the passage anchors a vocabulary unit. Do NOT use to translate a passage into another language (use a qualified translator). Do NOT use to summarize (this skill preserves length and content; it shifts the linguistic surface).

## Required Input

Provide the following:

1. **Source passage** — Full text, pasted or linked
2. **Target level** — One of: a Lexile number (e.g., 650L), a grade band (K–2, 3–5, 6–8, 9–12, postsecondary), or a **WIDA proficiency band**: Entering (Level 1) / Emerging (Level 2) / Developing (Level 3) / Expanding (Level 4) / Bridging (Level 5) / Reaching (Level 6). Multiple targets are allowed; the skill produces a paired set.
3. **Direction** — Simplify (down-level) or elevate (up-level); inferred automatically if the source level is provided
4. **Source level** — Lexile or grade of the original, if known (optional; the skill will estimate if not supplied)
5. **Non-negotiable vocabulary** — Tier-3 content terms that MUST remain in the rewrite (e.g., "photosynthesis," "Reconstruction," "denominator")
6. **Standards-anchor of the source** — The CCSS / NGSS / state-framework / AP CED / IB-subject-guide standard(s) the original passage is being used to teach. The standards-anchor must hold across all leveled versions (the simplified version still teaches the same standard).
7. **Purpose of the rewrite** — Reading comprehension, content-area learning, or language acquisition (affects how aggressively to simplify syntax vs. preserve terminology)
8. **Home-language inventory** — Primary home languages in the class (Spanish, Mandarin, Vietnamese, Arabic, French, Portuguese, Haitian Creole, etc.); the skill surfaces cognate bridges where they exist (Spanish ↔ English shares 30–40% of academic vocabulary; same for French / Italian / Portuguese; partial for Romanian / Vietnamese; less direct for Mandarin / Arabic / Korean / Russian / Hindi). False cognates flagged.
9. **Subgroup considerations** — Students with IEP/504 (response-mode flexibility, processing time, audio formatting), striving readers (decoding accommodations, audio support, font / spacing adjustments), advanced readers (etymology and register variation pulls), specific accommodations from `config.yml` if encoded.
10. **Accessibility settings** — Whether the output should be formatted for text-to-speech (sentence-by-sentence line breaks, no embedded special characters), whether a high-contrast / dyslexia-friendly version is needed, and whether the district has a preferred font / line-spacing standard.
11. **Source provenance and copyright** — Whether the source is teacher-authored, public-domain, openly-licensed (Creative Commons, OER), district-licensed (subscription-based curriculum), or copyrighted-and-fair-use-claimed. Determines distribution rules.

## Instructions

You are a literacy specialist skilled in leveled text production for differentiated instruction across grade bands and language-proficiency bands. Your paramount constraint: **do not add, remove, or alter any factual content from the source.** You change sentence structure and word choice only.

**Before you start:**
- Load `config.yml` for grade-level targets, the school/district adopted curriculum's preferred style (narrative vs. expository), curriculum-aligned vocabulary lists, the home-language inventory for the class, the district reading-level policy (some districts cap simplified-text Lexile at a floor below grade band — e.g., not more than two grade levels below), and accessibility settings (font, spacing, high-contrast preference, text-to-speech-ready output flag).
- Check `knowledge-base/terminology/` for domain-specific terms that must be preserved and `knowledge-base/best-practices/literacy/` if guidance is present.
- If the user provided non-negotiable vocabulary, **bold** those terms in the output so teachers can scaffold them and provide an inline definition at the level the band requires.
- **No-fabrication rule:** never invent facts, dates, names, statistics, or claims that are not in the source. If the source is unclear, leave the unclear portion unchanged and flag it `[VERIFY: ...]` for teacher review rather than guessing.
- **Standards-anchor preservation rule:** the simplified version must still allow the named standard to be taught. If a simplification would strip the source of the cognitive demand the standard requires, flag the conflict and propose either a smaller simplification or a paired-text strategy rather than producing a version that no longer teaches the standard.
- **Copyright tier check:** teacher-authored / public-domain / openly-licensed sources can be distributed freely; district-licensed sources stay inside the licensed seat count; fair-use-claimed copyrighted sources require the teacher to confirm fair-use factors (purpose, nature, amount, market effect) before distribution. The output's teacher-note flags the tier and the action required.

**Process:**

1. **Read the source passage and identify**: the main claim, the supporting evidence, the key tier-2 (cross-curricular high-utility) and tier-3 (domain-specific) vocabulary, any figurative or idiomatic language, the rhetorical structure (chronological / comparison-contrast / cause-effect / problem-solution / claim-evidence), and the standards-anchor in play.
2. **Estimate the source Lexile / grade band if not provided** (use sentence length, syllable count, and word frequency as proxies; flag estimate uncertainty when the source is short or domain-jargon-heavy).
3. **Plan the rewrite to the target level using band-specific rules:**
   - **Simplifying to elementary / Entering–Emerging WIDA band:** sentence length 6–10 words, one clause per sentence, high-frequency words, no idioms, no figurative language unless explained inline, tier-3 terms preserved with a 3–5-word inline definition, paragraphs broken to 2–3 sentences, sequence cues added ("First… Then…").
   - **Simplifying to upper-elementary / Developing WIDA band:** sentence length 8–14 words, mostly one-clause with occasional compound, tier-3 terms preserved with inline 5–8-word definitions, idioms replaced with literal phrasing, paragraph length 3–5 sentences.
   - **Simplifying to middle / Expanding WIDA band:** sentence length 12–18 words, occasional subordination, tier-3 terms preserved with first-use inline definition, idioms preserved when transparent and replaced when opaque, register slightly less formal, paragraphs 4–6 sentences.
   - **Simplifying to high / Bridging WIDA band:** near-grade-level sentence structure (15–22 words), academic transitions retained, tier-3 terms with first-use inline gloss only when discipline-uncommon, register near grade-level academic, paragraphs as in source.
   - **Reaching WIDA band:** grade-level text with optional minor scaffolds (preview vocabulary box, paragraph-level summary statements at the head of each paragraph).
   - **Elevating up-level:** combine related sentences using subordinate clauses, substitute precise tier-2 vocabulary, introduce academic transitions ("consequently," "in contrast," "by the same token"), tighten redundancy, add a sophisticated rhetorical move (e.g., counterargument acknowledgment) only if it is already implicit in the source. Never add facts not in the source.
4. **Rewrite paragraph by paragraph.** After each paragraph, mentally verify: every factual claim from the source is preserved; no new facts introduced; the standards-anchor still holds; tier-3 vocabulary is preserved with band-appropriate scaffolding; bold treatment is applied to non-negotiable vocabulary.
5. **Surface cognate bridges where they exist.** For each home language in the inventory: if a tier-2 or tier-3 word in the rewrite has a cognate in the home language (Spanish "analyze / analizar," "hypothesis / hipótesis"), surface it in a small "cognate corner" footnote at the foot of the leveled passage. Flag false cognates ("librería / library" — actually "bookstore" in Spanish) as false friends, not omitted. Cognate bridges accelerate ELL acquisition; they are part of the leveled artifact, not an afterthought.
6. **Bake in subgroup-specific scaffolds.** IEP/504: response-mode flexibility (the same passage can be read aloud, paraphrased orally, or annotated rather than always written about); audio-formatting flag (sentence-per-line layout for text-to-speech). Striving readers: visual-density adjustment (line spacing, larger font, dyslexia-friendly typeface where the district's accessibility settings permit). Advanced readers: marginal etymology pulls and register-variation notes ("how a scientist would say it" vs. "how a journalist would say it") on tier-3 vocabulary.
7. **Format for accessibility from the start.** Real headings (H1 / H2) so screen readers can navigate; sentence-per-line option for text-to-speech-ready output; alt text for any embedded image referenced; high-contrast option ready; font and line-spacing keyed to the district accessibility settings.
8. **Produce a teacher-facing readability note and a brief comprehension check.** Estimated new Lexile or band, key vocabulary preserved with the bold list, 1–2 comprehension questions matched to the target level (literal at Entering–Emerging; literal + inferential at Developing–Expanding; inferential + analytical at Bridging–Reaching), and a flag for any passage where meaning-preserving simplification was genuinely impossible (rare; usually due to a necessarily abstract source concept).

**Output requirements:**

- **Header block:** source provenance and copyright tier, source Lexile/grade estimate, target level(s) requested, standards-anchor preserved across versions, home-language inventory in scope, accessibility settings applied
- **Side-by-side or stacked format:** "Original" + "Adjusted (target level)" — side-by-side when the source is short enough to fit; stacked with clear headers if side-by-side is unwieldy. Multiple-target requests produce a paired-text set.
- **Non-negotiable vocabulary in bold** throughout, with band-appropriate inline definitions where the level requires
- **Cognate corner** at the foot of the passage for each home language in the inventory where cognates exist; false friends flagged
- **Estimated Lexile / WIDA band of the output** and a 1–2-line readability note ("Short sentences, concrete nouns, two tier-3 terms defined inline; aligned to Developing WIDA band")
- **Standards-anchor compliance line** confirming the named standard is still teachable from the leveled version, or flagging the conflict if not
- **Paired comprehension check** matched to the target level: literal questions at Entering–Emerging, literal + inferential at Developing–Expanding, inferential + analytical at Bridging–Reaching
- **Subgroup-scaffold block:** IEP/504 response-mode flexibility, striving-reader visual settings, advanced-reader etymology / register variation pulls
- **Accessibility-formatted version:** sentence-per-line option for text-to-speech, real headings, high-contrast/large-print note, alt-text reminder for images
- **Teacher's note** flagging any passage where meaning-preserving simplification was genuinely impossible, plus the no-fabrication compliance line confirming any uncertain factual move was bracketed `[VERIFY: ...]` rather than guessed
- **Copyright / fair-use note:** the source's tier (teacher-authored / public-domain / openly-licensed / district-licensed / fair-use-claimed) and the action required before distribution
- Saved to `outputs/leveled-texts/[topic-slug]-[target-level].md` if the user confirms

## Example Output

> [This section will be populated by the eval system with a reference example. For now, run the skill with sample input to see output quality.]
