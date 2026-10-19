---
name: ir-financial-html-updater
description: Update investor-relations financial HTML snippets and chart data from Excel workbooks. Use when Codex is asked to apply annual or quarterly financial highlight and homepage KPI data from .xlsx files to HTML/Vue snippets in English or Thai.
---

# IR Financial HTML Updater

## Quick Workflow

1. Read the provided workbook first; do not infer numbers from prior code.
2. Identify the relevant sheets and regions:
   - `Home`: homepage KPI counters, customer/surgery-hour circles, homepage revenue/profit charts.
   - `Financial Highlights`: chart card summary rows and detailed financial table rows.
   - `Business Overview`: supporting operational counters when the homepage links to business overview data.
3. Preserve the user's HTML structure and language. Replace only dates, periods, labels, numbers, table cells, and `window.chart` data needed by the request.
4. For quarter updates, put quarter values under `source.quarterly`, set `QoQ: true`, and keep annual values under `source.yearly`.
5. Return the updated replacement code. Flag source inconsistencies that affect the requested financial update.

## Data Extraction

Use the Spreadsheets capability or `@oai/artifact-tool` to import `.xlsx` files and inspect sheet values. Prefer full-table snapshots of the relevant sheets over manual cell guessing.

Look for both English and Thai labels in adjacent columns. Use the English label for EN snippets and the Thai label for TH snippets, but keep the same numeric source.

When a workbook contains both a small chart summary and a detailed table:

- Use summary rows for chart components and homepage chart scripts.
- Use detailed rows for the financial table.
- Preserve intentional differences between summary and detailed values.

Read `references/page-patterns.md` when handling MASTER/SKR-style pages or when a value seems ambiguous.

## HTML Update Rules

For financial highlight tables:

- Drop old years when the workbook period set has shifted.
- Keep the first column as the unit/row label column.
- Format monetary values with commas and two decimals.
- Format ratios/EPS with two decimals unless the workbook visibly uses another precision.
- Keep existing classes and component tags.

For chart scripts:

```js
QoQ: true,
source: {
  yearly: {
    period: [2023, 2024, 2025],
    dataset: [/* annual values */],
  },
  quarterly: {
    period: ['1Q/2026'],
    dataset: [/* quarter value */],
  }
}
```

For Thai pages:

- Convert Gregorian years to Buddhist Era years by adding 543.
- `1Q/2026` normally displays as `1Q/2569`.
- If the workbook's Thai period conflicts with its English period/date, report it as a likely source typo instead of silently changing the period.

For homepage KPI counters:

- Counter values live in `<counter-number :number="...">`, not only rendered text.
- Use zero-decimal values for operational counts and surgery hours.
- Update adjacent "as of" text in both languages.
