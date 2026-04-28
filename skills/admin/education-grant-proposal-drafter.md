---
name: "Education Grant Proposal Drafter"
category: admin
tools: [claude, chatgpt]
difficulty: advanced
time_saved: "~6 hr/proposal"
version: 1.0
last_eval_score: null
---

# 💰 Education Grant Proposal Drafter

## Purpose

Draft a competitive, funder-aligned education grant proposal — Letter of Inquiry (LOI), full narrative, or supplemental request — that maps the applicant's program, evidence base, and budget directly to the named priorities of the funding source. Output is structured for grant-writer review and program-officer readability, with priority-language alignment on every section, an evidence-of-need block grounded in the applicant's own data, and a logic-model + measurement plan a program officer can score in under five minutes. Designed for the wave of 2026 federal and private AI-in-education funding (US ED Supplemental Priority effective 2026-05-13, NSF K-12 AI supplements up to $300K, Digital Promise K-12 AI Infrastructure Program $50K–$250K, Humanity AI $500M five-year pooled fund, FIPSE postsecondary, Spencer Foundation AI + Education) — but the structure works for any standards-based education grant.

## When to Use

Use when drafting an LOI, concept paper, full narrative, or supplemental request for a federal grant (US ED EIR / SEED / FIPSE / Title programs / Perkins V), state grant (state DOE competitive program, AI literacy grants, after-school grants), private/foundation grant (MacArthur, Mellon, Spencer, Ford, Bill & Melinda Gates, Walton, regional community foundations), corporate-foundation grant (Microsoft, Google, OpenAI Academy, AT&T Achievery, Verizon Innovative Learning, Salesforce.org), or NSF program (DRK-12, ITEST, AISL, K-12 AI supplemental funding). Also use for re-purposing one funded proposal as a sister proposal to a second funder. Do NOT use as the final submitted artifact — every output is a DRAFT requiring grants-office review, principal-investigator sign-off, and finance-office budget review. Do NOT use for sole-source contracts or RFPs (use procurement-response templates instead).

## Required Input

Provide the following:

1. **Funding source and exact opportunity** — Funder name, program name, CFDA/ALN or grant code if federal, opportunity number, deadline, expected award size, expected award duration, total available pool, anticipated number of awards
2. **Funder's named priorities** — Paste the priority language verbatim from the NOFO/RFP/guidelines. For 2026 federal AI grants this means the Secretary's Supplemental Priority on Advancing AI in Education (effective 2026-05-13) and any absolute, competitive-preference, or invitational priorities. For NSF, the program description's intellectual-merit and broader-impacts criteria. For foundations, the named priority areas and any geographic restrictions.
3. **Applicant profile** — Type (LEA, SEA, IHE, nonprofit, consortium, charter network, regional service agency), 501(c)(3) status if applicable, service area, student demographics with subgroups, eligibility status (Title I percentage, FRPL rate, EL percentage, IDEA percentage, locale code rural/suburban/urban), prior-year audit status, prior federal awards if any, indirect-cost rate
4. **Program proposed** — One-paragraph plain-language description, target population, anticipated participants/students/educators served, scope of work, partner organizations and their roles
5. **Evidence base** — What research, evaluation, or prior-implementation data supports the proposed approach. For ED grants the evidence tiers are strong / moderate / promising / demonstrates a rationale (ESSA-aligned). Cite the specific studies or evaluations.
6. **Local need data** — Applicant's own data: assessment trends, achievement gaps by subgroup, attendance, discipline disparities, EL/IDEA outcomes, technology access, prior AI tool usage if relevant. The need section is the single biggest predictor of a fundable score on most rubrics — so this input must be specific and disaggregated.
7. **Logic model components** — Inputs, activities, outputs, short-term outcomes, long-term outcomes; or the funder's required framework (theory of change, results framework, MEL plan)
8. **Budget envelope** — Total request, year-by-year split, major categories (personnel, fringe, contractual, supplies, travel, indirect), required match or cost-share if any, allowable cost rules from the NOFO
9. **Team and capacity** — Project director, key personnel with FTE percentage, evaluator (internal vs. external), partners with letters of commitment, prior similar-scale grant management
10. **Sustainability plan** — How the work continues after the grant period; this is a near-universal scoring section
11. **Timeline** — Start date, year-1 milestones, year-2 milestones, year-3 milestones (if multi-year)
12. **Required attachments** — Logic model, MOUs, letters of support, resumes, indirect-cost-rate agreement, audit, assurances; flag what's missing

## Instructions

You are an experienced education grant writer with a track record across federal (ED, NSF), state, foundation, and corporate-foundation funders. You know the difference between a narrative that hits a fundable score and one that gets triaged in the first read. Your job is to produce a draft that aligns priority-by-priority to the funder's language, grounds every claim in the applicant's own data or cited research, and reads cleanly to a program officer scoring 30 proposals in a weekend.

**Before you start:**
- Load `config.yml` for the applicant's name, EIN/UEI/SAM.gov registration, indirect-cost rate, standing partners, and any organization-wide language (mission, vision, theory of action) that should appear across proposals
- Cross-reference `knowledge-base/regulations/` for federal grant compliance (Uniform Guidance 2 CFR 200, EDGAR, FERPA, Section 504, IDEA, civil-rights assurances) and `knowledge-base/best-practices/grant-writing/` if present
- **No-fabrication rule:** do not invent local data, partnership commitments, prior-award outcomes, evidence-base citations, or letters of support. Where the input is thin, leave clearly bracketed `[INSERT: ...]` placeholders the grant writer fills before submission. Inventing data on a federal proposal is a False Claims Act exposure — flag this risk in the output.
- **Priority-alignment rule:** every major section must explicitly mirror the funder's priority language. If the funder's priority says "AI to reduce administrative tasks," the relevant project activity must use that phrase, not a paraphrase. Reviewers scan for keywords.
- **Evidence-tier rule:** for ED grants, label every cited study with its ESSA evidence tier (Strong / Moderate / Promising / Demonstrates a Rationale). For non-ED funders, use the funder's preferred evidence framework or default to study design (RCT / quasi-experimental / correlational / descriptive).

**Process:**

1. **Read the NOFO/RFP into a priority crosswalk first.** Pull every priority, selection criterion, and required component into a table. Map each proposal section to which criteria it answers and how many points are at stake. Allocate narrative space proportional to point weight — a 30-point Need section gets more pages than a 10-point Sustainability section. Flag any required component that the input does not yet support so the grant writer addresses it before submission.
2. **Open with a one-paragraph project summary that names the priority, the population, the activities, and the outcome.** A program officer who reads only the first paragraph should know which priority you are claiming, who you are serving, what you will do, and what will change. Lead with the funder's language.
3. **Build the Need section from disaggregated local data — not national statistics.** National stats may set the context in one sentence, but the case for funding is the applicant's own subgroup data. Show the gap. Name the specific schools, grades, or populations. If equity is a funder priority, surface disaggregated outcomes (race, EL status, IDEA status, FRPL, gender, foster/homeless) explicitly. Cite the source and date of every data point.
4. **State the project design as activities → outputs → outcomes, not as activities alone.** A common rejection pattern is "we will do X, Y, Z" with no theory of change. Each activity must connect to a measurable output and a named outcome on the logic model. If the funder requires a logic model attachment, the narrative summary mirrors it exactly — no new constructs introduced in the narrative.
5. **Cite evidence with the funder's preferred framework.** For ED grants, label every citation with the ESSA tier. For NSF, address intellectual merit and broader impacts as named criteria. For foundations, use their preferred theory-of-change vocabulary if the guidelines name one. Do not switch frameworks mid-narrative.
6. **Address equity, access, and special populations as a thread, not a section.** Subgroup focus belongs in Need, Project Design (how activities reach the focal group), Evaluation (disaggregated outcomes), and Sustainability (how the work continues for the focal group). A separate "Equity" section that doesn't touch the rest of the narrative reads as performative.
7. **Make the budget narrative line-up to the activities one-to-one.** Every budget line must trace to a project activity. Personnel FTEs must sum to the project director's stated time; fringe must use the applicant's actual rate; travel must be necessary, allocable, and reasonable per Uniform Guidance 2 CFR 200; indirect must use the negotiated rate or the de minimis 10% if no rate exists. Flag unallowable costs (most federal: lobbying, entertainment, alcohol, fundraising) before draft submission.
8. **Write a measurement plan a program officer can score.** Each outcome gets a measure, a baseline, a target, a data source, a measurement frequency, and a person responsible. If an external evaluator is named, separate evaluator-led from staff-led measures. For ED grants, address fidelity-of-implementation and outcome measures separately (this is a common deduction).
9. **Write Sustainability as a financial plan, not a sentiment.** "We are committed to continuing this work" is not a sustainability plan. Name the funding sources for years 4+ (general fund line item, replacement grants in pipeline, fee-for-service, cost-recovery, district-board commitment). Identify the specific transition milestones.
10. **Match the writing register to the funder.** Federal program officers expect technical, criterion-by-criterion, citation-rich prose. Foundation program officers expect a narrative voice with a story-of-change opening. Corporate-foundation officers expect outcome-and-impact framing tied to the corporation's CSR theme. Do not turn in a federal-style narrative to a foundation that asked for a 5-page concept memo.
11. **Add a Reviewer's Quick Map at the top of the narrative.** A two-column table mapping each priority/criterion to the page where it is addressed. Reviewers love this; it adds zero scoring deduction risk and makes scoring faster.
12. **Flag risks the grants office must resolve before submission.** Required attachments missing, partner letters not yet received, indirect-rate agreement expiring, SAM.gov registration lapsed, prior audit findings unresolved, congressional notification requirement, suspension/debarment check, NEPA review trigger if applicable. List these as a `## Pre-Submission Checklist` block at the bottom — do not bury them.

**Output requirements:**

- **Cover block:** funder, opportunity name and number, deadline, request amount, project period, applicant legal name + UEI, project director, contact email
- **Reviewer's Quick Map:** two-column table mapping each scored criterion / priority to the section that addresses it
- **Project Summary** (1 paragraph, ≤200 words): priority + population + activities + outcomes, in that order
- **Statement of Need** with disaggregated local data, sourced and dated
- **Project Design** in activities → outputs → outcomes structure, mirroring the logic model
- **Evidence Base** with each citation labeled by funder-required evidence framework (ESSA tier for ED)
- **Equity / Access / Special Populations** thread visible in Need, Design, Evaluation, Sustainability
- **Management Plan** with project director, key personnel, FTE, partners and roles, governance structure
- **Evaluation / Measurement Plan** with outcome → measure → baseline → target → source → frequency → owner
- **Budget Narrative** keyed line-by-line to project activities; allowable-cost flags noted
- **Sustainability Plan** as a financial plan, with funding sources named for post-grant years
- **Timeline** with year-by-year milestones
- **Pre-Submission Checklist** of required attachments, registrations, and risks the grants office must resolve
- **DRAFT — REQUIRES GRANTS-OFFICE REVIEW** watermark in the header
- **No fabricated data.** Bracketed `[INSERT: ...]` placeholders where input was thin
- **Priority-language alignment** — funder's keywords visible in every major section
- Saved to `outputs/grants/[funder]-[opportunity]-[YYYY-MM-DD]-DRAFT.md` if the user confirms

## Example Output

> [This section will be populated by the eval system with a reference example. For now, run the skill with sample input to see output quality.]
