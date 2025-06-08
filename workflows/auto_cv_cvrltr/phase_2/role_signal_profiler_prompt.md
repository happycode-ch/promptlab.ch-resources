# Role Signal Profiler (No Resume Comparison)

## Purpose
Extract common hiring signals from a set of job descriptions for a specific job type. This is used to build a reusable "role knowledge base" that can later be compared to a modular resume, but this prompt does **not** include any candidate-specific analysis.

---

## Instructions

You will paste:

1. A **batch of job descriptions** (ideally 3–10), all related to the same role type (e.g., ICT Supporter, Data Analyst, BI Developer).

---

## Prompt

Please act as an expert in:

- Technical hiring and job market analysis
- ATS keyword optimization and hiring signal detection
- Swiss and EU job market norms

TASKS:

1. Parse all job descriptions and extract key hiring signals in the following categories:

    - Core Skills  
    - Tools / Technologies  
    - Responsibilities  
    - Strategic Objectives  
    - Soft Skills / Personality  
    - Language Requirements  
    - Certifications / Education  
    - Experience Level  
    - ATS Keywords / Search Phrases  
    - Company Environment Signals (e.g., public sector, startup, consultancy)

2. Count frequency and emphasis of each item.  
3. Return one structured JSON block called `role_signal_profile`.

---

### Output JSON Format

```json
{
  "role_type": "e.g., ICT Supporter / System Administrator",
  "skills": ["Linux (6)", "PowerShell (4)", "Scripting (3)"],
  "tools": ["Azure (5)", "Elastic Stack (3)", "Active Directory (3)"],
  "responsibilities": ["Maintain infrastructure", "Monitor systems", "Support end users"],
  "objectives": ["Ensure uptime", "Automate processes", "Improve IT security"],
  "soft_skills": ["Reliable", "Structured", "Problem solver"],
  "languages": ["German (B2+)", "English (Fluent)"],
  "certifications": ["CompTIA (2)", "Microsoft Certified (1)"],
  "experience_level": "1–3 years (junior to medior)",
  "ats_keywords": ["IT support", "infrastructure monitoring", "ticketing system"],
  "company_signals": ["Public agency", "Regional SME", "Internal IT team"]
}
