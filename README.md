# Type 2 Diabetes Clinical Trials in India: Landscape Analysis

A beginner-friendly clinical research project by **Murshidha M**, biotechnology graduate, currently learning ICH-GCP.

## Question

What does clinical research on Type 2 diabetes in India look like? Who runs the trials, how far have they progressed, and when did they start?

## Key findings

- **585** registered Type 2 diabetes trials have at least one site in India.
- **74%** (435) are completed; 55 are recruiting or not yet recruiting; 38 were terminated or withdrawn.
- **65%** of trials with a stated phase (251 of 389) are Phase 3.
- **Seven pharmaceutical companies ran 51%** of all trials (298). Novo Nordisk alone ran 110.
- Trial starts peaked in 2006-2010 (204 trials), dipped to 90 in 2016-2020 and rose to 127 in 2021-2025.

Read the full report with charts: `Type_2_Diabetes_Clinical_Trials_India_Landscape_Report.pdf`

## Files in this repository

| File | What it is |
|---|---|
| `Type_2_Diabetes_Clinical_Trials_India_Landscape_Report.pdf` | The 4-page report with four charts and findings |
| `T2D_India_Trials_Analysis_2.2.xlsx` | Excel workbook: cleaned data, pivot tables, charts and findings |
| `T2D_India_trials_clean.csv` | Cleaned dataset (585 trials, 18 columns) |

## Data

- **Source:** [ClinicalTrials.gov](https://clinicaltrials.gov), U.S. National Library of Medicine. Please see the site's terms and conditions for data use.
- **Search:** condition "type 2 diabetes", location India.
- **Downloaded:** 1 November 2026.

### Cleaning steps

1. The download had 611 rows. 26 were broken fragments of the Locations text, so they were removed, leaving 585 trials with unique NCT numbers.
2. The Locations column was dropped because it was broken by line breaks.
3. A `Start Year` column was added from the start date (6 trials have no start date, so year analysis covers 579 trials).
4. Blank phases are labelled `NOT APPLICABLE / NOT STATED`.
5. The `Start Date` column keeps the original mixed date formats; use `Start Year` for analysis.

## Method

Counts were made with Excel pivot tables by study status, phase, sponsor and start year, then charted and interpreted.

## Limitations

- "India" means at least one trial site in India. Many trials are global, so sponsor counts show who runs trials that include Indian sites.
- Sponsor is the lead sponsor only; collaborators are not counted.
- Trials registered only in other registries, such as India's own national registry, are not included.
- 196 trials list no phase: 102 interventional, 93 observational and 1 expanded access. Many are likely non-drug studies.
- Start years in 2026 may include planned trials.
- The data shows what exists, not why. For example, the 2006-2010 peak may partly reflect registration rules of that period.

## Next steps

- Repeat the analysis for other diseases.
- Study why trials were terminated or withdrawn.
- Repeat the counts in Python (pandas).

## About

Analysis and interpretation by Murshidha M. Built with guidance from an AI assistant (Claude).
