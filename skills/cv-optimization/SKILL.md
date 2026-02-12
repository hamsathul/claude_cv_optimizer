---
name: cv-optimization
description: >
  This skill should be used when the user asks to "optimize my CV",
  "tailor my resume", "fix my CV for a job", "make my resume ATS-friendly",
  "improve my resume for a job description", "rewrite my CV", or needs
  guidance on resume optimization, ATS compliance, keyword matching,
  or interview-ready document preparation.
version: 0.1.0
---

# CV / Resume Optimization

Optimize a CV or resume for a specific job description. The goal is to maximize interview callback rates while keeping the document ATS-friendly and human-sounding.

## Core Principles

1. **ATS compatibility first** — Most resumes are filtered by Applicant Tracking Systems before a human ever sees them. Every optimization must pass ATS parsing.
2. **Keyword alignment** — Match the language, terminology, and phrasing used in the job description naturally throughout the CV.
3. **Human readability** — After passing ATS, a recruiter spends ~7 seconds scanning. The CV must be clear, scannable, and compelling to a human reader.
4. **Authenticity** — Never fabricate experience, skills, or qualifications. Reframe and emphasize existing experience to align with the target role.

## Workflow

### Step 1: Parse the Input CV

Read the uploaded CV (PDF, DOCX, or Markdown). Extract all content and identify sections dynamically. Common sections include but are not limited to:

- Contact Information / Header
- Professional Summary or Objective
- Work Experience / Employment History
- Skills (Technical and Soft)
- Education
- Certifications / Licenses
- Projects
- Volunteer Work
- Awards / Achievements
- Publications
- Languages

Preserve the original section structure unless restructuring is clearly beneficial.

### Step 2: Analyze the Job Description

Parse the job description provided by the user. Extract:

- **Required qualifications** — hard requirements (years of experience, specific degrees, certifications)
- **Preferred qualifications** — nice-to-haves that provide an edge
- **Key responsibilities** — what the role actually does day-to-day
- **Technical skills** — tools, technologies, platforms, methodologies mentioned
- **Soft skills** — leadership, communication, collaboration keywords
- **Industry terminology** — domain-specific language and acronyms
- **Action verbs** — verbs the JD uses repeatedly (managed, led, developed, etc.)
- **Company values / culture signals** — anything about company mission or team culture

### Step 3: Gap Analysis

Compare the CV against the JD:

- **Strong matches** — experience/skills that directly align with JD requirements
- **Partial matches** — related experience that can be reframed to better align
- **Gaps** — JD requirements not currently reflected in the CV
- **Irrelevant content** — CV content that adds no value for this specific role

For gaps, determine whether the user likely has the experience (just not highlighted) or genuinely lacks it. Never add fabricated experience.

### Step 4: Section-by-Section Optimization

Optimize each section following the detailed guidelines in `references/section-guidelines.md`.

General rules for all sections:

- Use exact keywords from the JD where they truthfully apply
- Write in active voice with strong action verbs
- Quantify achievements wherever possible (numbers, percentages, dollar amounts, team sizes)
- Remove or de-emphasize content irrelevant to the target role
- Keep bullet points concise: 1-2 lines each, leading with the action/impact
- Avoid buzzwords that add no substance ("synergy", "guru", "ninja", "rockstar")
- Spell out acronyms on first use, then use the acronym (ATS systems search for both)

### Step 5: ATS Compliance Check

Run through the ATS compliance checklist in `references/ats-checklist.md` to verify the optimized CV will parse correctly.

### Step 6: Human Tone Review

Review the entire optimized CV for natural, human-sounding language:

- Does each bullet tell a mini-story? (Action → Context → Result)
- Would the user be comfortable saying these things in an interview?
- Is the language specific and concrete rather than vague and generic?
- Does it read like a professional wrote it, not a template generator?
- Are sentences varied in structure (not all starting the same way)?

### Step 7: Output

Generate the final CV in the requested format (DOCX by default, PDF if requested).

Present a summary to the user:

- Key changes made per section
- Keywords incorporated from the JD
- Suggestions the user should verify (e.g., confirming specific metrics)
- Any gaps that could not be addressed without fabrication — suggest the user add relevant experience if they have it

## Additional Resources

- **`references/section-guidelines.md`** — detailed optimization rules for each CV section
- **`references/ats-checklist.md`** — ATS compatibility verification checklist
- **`references/keyword-strategy.md`** — keyword identification and placement strategies
