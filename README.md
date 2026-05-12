# Healthcare SQL Analytics Portfolio

## Project 1 — Hospital Readmission Risk Analyzer

Analyzed an 867-encounter CMS-structured inpatient dataset to identify 
30-day readmission patterns by DRG code and payer type.

**Skills demonstrated:** Window functions (LAG), CTEs, multi-table JOINs, 
GROUP BY aggregations, HAVING filters, CASE logic

**Dataset:** Synthetic inpatient data modeled on CMS structure — 500 patients, 
867 encounters, 15 DRG codes, 4 payer types

**Key findings:**
- Identified 72 confirmed 30-day readmissions (~8% rate)
- Heart failure DRGs showed highest readmission rates across all payer types
- Medicare patients had longest average LOS (6.1 days)
- Segmented top 20 high-risk patients for care coordination targeting

**Files:**
- `readmission_analysis.sql` — all 4 queries with comments
- `admissions.csv` — encounter-level dataset
- `patients.csv` — patient demographics and payer info


## Project 2 — ICD-10 Coding Accuracy Audit Pipeline

Designed and executed a SQL-based CDI audit across 800 encounter records,
ranking coder accuracy, classifying error types by frequency, and flagging
invalid/truncated ICD-10 codes against a reference table.

**Skills demonstrated:** Multi-table JOINs, CASE WHEN aggregations,
LEFT JOIN for data quality, window functions, strftime date grouping,
HAVING filters

**Key findings:**
- Overall coding error rate: ~19% across 8 coders
- CDR06 and CDR03 flagged for remediation (60–65% accuracy)
- Truncated codes were the most common error type (~35% of all errors)
- Produced monthly accuracy trend report for governance committee review
