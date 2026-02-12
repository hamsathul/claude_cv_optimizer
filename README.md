# Resume Optimizer

Optimize your CV or resume for a specific job description. The plugin analyzes each section of your CV against the target job's requirements and rewrites it to maximize your chances of getting an interview — while keeping the content ATS-friendly and naturally human-sounding.

## What It Does

- Accepts your CV in **PDF**, **DOCX**, or **Markdown** format
- Asks for the target job description
- Analyzes every section against the job requirements
- Rewrites and optimizes your CV with aligned keywords and stronger phrasing
- Outputs a polished **DOCX** (default) or **PDF**
- Provides a summary of changes, keywords added, and any gaps to address

## Usage

Run the command:

```
/optimize-cv path/to/your-cv.pdf
```

Or simply run `/optimize-cv` and you'll be prompted to provide your CV and the job description.

## Components

### Command: `/optimize-cv`
The main workflow. Reads your CV, collects the job description, performs a full analysis, and generates an optimized document.

### Skill: `cv-optimization`
Domain knowledge that powers the optimization — ATS best practices, section-by-section rewriting guidelines, and keyword placement strategies. This skill also activates automatically when you discuss CV or resume optimization in conversation.

## Key Features

- **Dynamic section detection** — works with any CV layout, not just a fixed template
- **Keyword gap analysis** — identifies which job description requirements are covered and which aren't
- **ATS compliance verification** — checks formatting, structure, and keyword placement against ATS parsing rules
- **Human tone preservation** — optimized text sounds natural and interview-ready, not robotic
- **No fabrication** — the plugin reframes your real experience but never invents credentials or metrics

## Setup

No external services or API keys required. The plugin works entirely with local files.
