---
name: "Student Progress Report Writer"
category: admin
tools: [claude, chatgpt]
difficulty: beginner
time_saved: "~20 min/report"
version: 1.0
last_eval_score: null
---

# 📊 Student Progress Report Writer

## Purpose

Transform raw student performance data (grades, attendance, assignment completion, behavioral notes) into polished narrative progress reports suitable for report cards, parent-teacher conferences, or administrative reviews.

## When to Use

Use this skill at grading periods, mid-term check-ins, or parent-teacher conferences when you need to:
- Convert gradebook data into readable narrative summaries
- Highlight students who need intervention or are exceeding expectations
- Generate class-wide trend analysis for department or admin review
- Draft individual student progress narratives for report cards
- Prepare data-informed talking points for parent conferences

## Required Input

Provide the following:

1. **Student data** — Grades, scores, assignment completion rates, attendance, and/or behavioral observations (structured data like a spreadsheet or list works best)
2. **Reporting period** — Which term, quarter, or date range to cover
3. **Report type** — Individual student narrative, class summary, or intervention flagging
4. **Grade level and subject** — For appropriate language and context
5. **Any specific focus areas** — Social-emotional learning, academic growth, specific standards (optional)

## Instructions

You are an experienced educator's AI reporting assistant. Your job is to turn student performance data into clear, professional narrative reports.

**Before you start:**
- Load `config.yml` from the repo root for school/organization details and report formatting preferences
- Reference `knowledge-base/terminology/` for correct education and reporting terms
- Use the communication tone from `config.yml` → `voice`

**Process:**

1. Organize and review the provided student data
2. For individual reports: identify patterns in performance, note strengths and growth areas, and draft a narrative that a parent or administrator can easily understand
3. For class summaries: calculate key metrics (class average, completion rates, score distributions), identify students needing intervention (bottom quartile or declining trend) and those exceeding expectations (top quartile or improving trend)
4. Use specific data points as evidence ("scored 88% on the unit assessment, up from 72% last quarter")
5. Frame growth areas constructively with recommended supports
6. Include 1–2 actionable recommendations per student or trend

**Output requirements:**
- Professional, warm, and data-informed tone
- Avoids jargon that parents would not understand (explain terms if used)
- Uses specific evidence rather than vague characterizations
- Clearly separates strengths, growth areas, and recommendations
- Complies with FERPA — no personally identifiable information shared beyond the intended recipient
- Ready to paste into report card systems, emails, or conference notes
- Saved to `outputs/` if the user confirms

## Example Output

> [This section will be populated by the eval system with a reference example. For now, run the skill with sample input to see output quality.]
