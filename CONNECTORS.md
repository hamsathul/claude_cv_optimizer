# Connectors

## How customization points work

Plugin files use `~~category` as a placeholder for values that vary by organization or region. During plugin setup (via the **Manage** button), these placeholders are replaced with your actual values.

## Connectors for this plugin

| Category | Placeholder | Default | Description |
|----------|-------------|---------|-------------|
| Resume style | `~~resume_style` | US Resume | Regional format convention: US Resume (1-2 pages, no photo), UK CV, European CV (Europass), or Middle East CV |
| Default language | `~~default_language` | English | Language the optimized CV will be written in |
| Include photo | `~~include_photo` | No | Whether to include a photo placeholder — required in some regions (Middle East, parts of Europe), discouraged in US/UK |
| Date format | `~~date_format` | MMM YYYY | Date format used in work experience (e.g., "Jan 2023", "01/2023", "January 2023") |
| Default output format | `~~default_output_format` | DOCX | Preferred output file format: DOCX or PDF |
| Include personal details | `~~include_personal_details` | Minimal | Level of personal info: Minimal (name, email, phone, city), Standard (adds nationality, visa status), Full (adds DOB, marital status — common in Middle East/Asia) |
| Page limit | `~~page_limit` | 2 | Maximum number of pages for the optimized CV |
