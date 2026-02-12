---
description: Optimize a CV/resume for a specific job description
allowed-tools: Read, Write, Edit, Bash, Glob, Grep, Task, TodoWrite
argument-hint: [cv-file-path]
---

Optimize a CV/resume to maximize interview chances for a specific job.

## Setup

1. Load the cv-optimization skill by reading `${CLAUDE_PLUGIN_ROOT}/skills/cv-optimization/SKILL.md`.
2. Read all three reference files:
   - `${CLAUDE_PLUGIN_ROOT}/skills/cv-optimization/references/section-guidelines.md`
   - `${CLAUDE_PLUGIN_ROOT}/skills/cv-optimization/references/ats-checklist.md`
   - `${CLAUDE_PLUGIN_ROOT}/skills/cv-optimization/references/keyword-strategy.md`

## Input Collection

### CV Input
If a file path was provided as an argument (`$ARGUMENTS`), read that file.
If no argument was provided, ask the user to upload or point to their CV file. Accept PDF, DOCX, or Markdown formats.

For PDF files, use the pdf skill to extract text.
For DOCX files, use the docx skill to extract text.
For Markdown files, read directly.

### Job Description Input
Ask the user to paste the full job description. Tell them:
"Please paste the complete job description for the role you're targeting. Include everything — title, responsibilities, qualifications, and any 'nice to have' sections."

Wait for the user to provide the job description before proceeding.

## Analysis & Optimization

Follow the workflow defined in the cv-optimization skill:

1. **Parse the CV** — Extract all content and identify every section dynamically.
2. **Analyze the JD** — Extract required qualifications, preferred qualifications, key responsibilities, technical skills, soft skills, industry terminology, action verbs, and culture signals.
3. **Gap analysis** — Map CV content against JD requirements. Identify strong matches, partial matches, gaps, and irrelevant content.
4. **Section-by-section optimization** — Rewrite each section following the section guidelines reference. Preserve the user's authentic experience while aligning language, keywords, and emphasis to the JD.
5. **ATS compliance check** — Verify against every item in the ATS checklist.
6. **Human tone review** — Ensure the final text sounds natural, specific, and like something the user would confidently say in an interview.

## Important Rules

- NEVER fabricate experience, skills, certifications, or metrics. Only reframe what exists.
- NEVER add skills the user hasn't demonstrated or claimed.
- When quantifying achievements, if exact numbers aren't available, flag them as "[verify number]" so the user can fill in accurate data.
- Keep the user's original section structure unless restructuring clearly benefits them.
- Preserve all truthful content — optimize wording, don't delete real experience.

## Output

### Default: DOCX
Use the docx skill to generate a professionally formatted Word document with:
- Clean, ATS-friendly formatting (single column, standard fonts, proper heading styles)
- Consistent spacing and margins
- Standard bullet characters
- The user's name as the document title

Save to the workspace folder with the filename: `[UserName]_Resume_Optimized.docx`

### If user requests PDF
Use the pdf skill to generate a clean, text-selectable PDF with the same formatting standards.
Save as: `[UserName]_Resume_Optimized.pdf`

## Summary Report

After generating the output file, present to the user:

1. **Changes Summary** — Bullet list of the most significant changes made, organized by section
2. **Keywords Added** — List of JD keywords that were incorporated and where they appear
3. **Verification Needed** — Any metrics, numbers, or claims marked with [verify] that the user should confirm
4. **Remaining Gaps** — JD requirements that could not be addressed without fabrication, with suggestions on how the user might address them (e.g., in a cover letter, through upskilling)
5. **Before/After Score** — A rough keyword match score (percentage of Tier 1 JD keywords now present in the CV) before and after optimization

Link the output file so the user can open it immediately.
