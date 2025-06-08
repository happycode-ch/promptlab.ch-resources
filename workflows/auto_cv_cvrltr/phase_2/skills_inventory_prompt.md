# Role Signal + Fit Alignment Generator

## Purpose

This meta-prompt extracts common hiring signals from a set of similar job descriptions and compares those signals to your modular resume data. The goal is to determine how well-aligned your resume is with the roles you're applying to — and to provide a tailored strategy for maximizing your interview chances.

This prompt is especially useful when applying to multiple jobs in a specific domain (e.g., Business Analyst, Data Analyst, ICT Supporter) and you want to calibrate your resume and cover letter content accordingly.

---

## Instructions

You will paste:

1. A **batch of job descriptions** (ideally 3–10), all related to the same role type.
2. Your **modular resume content** in JSON format:
   - `roles`: past roles or projects
   - `skills`: list of tools, languages, technical and soft skills
   - `philosophy`: traits, values, work style

The model will extract hiring signals and perform a structured fit evaluation.

---

## Prompt

```
I will paste several job descriptions for a specific job type I am applying to (e.g., Business Analyst, ICT Supporter, Data Analyst). Then I will paste my modular resume content as structured JSON.

Please act as an expert in:
- Technical hiring and ATS compliance
- Resume tailoring and content optimization
- Swiss and EU market hiring culture

---

### TASKS

1. Parse the job descriptions and extract key hiring signals in the following categories:
   - Core Skills
   - Tools / Technologies
   - Responsibilities
   - Business Objectives / Strategic Goals
   - Soft Skills / Attitude / Culture Fit
   - Language Requirements (e.g., German B2, English fluent)
   - Certifications / Education
   - Experience Level (e.g., medior, senior, 2–5 years)
   - ATS Keywords / system-detectable phrases
   - Company Type Signals (e.g., startup, public agency, consultancy, global firm)

2. Count and rank each item by frequency or emphasis.

3. Return a structured JSON block called `role_signal_profile`.

4. Then compare these signals with my modular resume content (`roles`, `skills`, `philosophy`), and create a fit alignment report.

5. Return a second structured JSON block called `resume_fit_evaluation` with:
   - Match % estimate for each category
   - Warnings or gaps (e.g., missing tools, language mismatch, soft skills gap)
   - Suggested resume strategy (which roles, skills, and traits to emphasize)
   - Estimated **Risk Level** for interview traction (Low, Medium, High)
   - Final summary comment with suggestions for tailoring

---

### Your Output Will Be Two JSON Objects:

#### 1. role_signal_profile

```json
{
  "role_type": "e.g., Business Analyst (Data Warehouse)",
  "skills": ["Python (6)", "SQL (5)", "Excel (4)"],
  "tools": ["Power BI (5)", "Azure (3)", "Jira (3)"],
  "responsibilities": ["Support stakeholders", "Build reports", "Improve data processes"],
  "objectives": ["Enable decision-making", "Ensure data quality", "Drive automation"],
  "soft_skills": ["Team player (6)", "Proactive (4)", "Structured communicator (3)"],
  "languages": ["German (B2+)", "English (Fluent)"],
  "certifications": ["DP-900 (2)", "Scrum (1)"],
  "experience_level": "2–5 years, medior",
  "ats_keywords": ["data-driven", "stakeholder", "reporting", "agile"],
  "company_signals": ["enterprise-scale", "cloud-native", "regulated industry"]
}
```

---

#### 2. resume_fit_evaluation

```json
{
  "fit_score": {
    "skills": "85%",
    "tools": "70%",
    "experience_level": "95%",
    "language_fit": "90%",
    "culture_tone": "60%"
  },
  "warnings": [
    "No mention of Looker Studio",
    "Azure is referenced only once in resume",
    "Some job descriptions expect fluent German; resume says B2"
  ],
  "resume_strategy": {
    "emphasize_roles": ["Swiss Post DW Project", "P42 DataOps"],
    "highlight_skills": ["SQL", "Azure", "Business Intelligence"],
    "suggested_philosophy_focus": "proactive, independent, data-savvy"
  },
  "risk_level": "Low",
  "comments": "You're well-aligned. Strengthen Azure references and clarify German proficiency if closer to C1."
}
```

---

After this prompt, I will paste:
- A batch of job descriptions
- My modular resume JSON (roles, skills, traits)

Then wait for your analysis.
```

