# Healthcare Patient Analytics — Tableau Dashboard Project

## Project Overview
A five-dashboard Tableau analysis of a public healthcare dataset, 
examining patient demographics, admissions patterns, financial 
performance, and data quality. This project demonstrates end-to-end 
analytics workflow including data cleaning, quality assessment, 
exploratory analysis, and stakeholder-ready visualization.

## Business Questions
- What patient and operational characteristics drive healthcare costs?
- Are there meaningful patterns in admissions volume and timing?
- What data quality issues exist and how should they be handled?

## Dataset
- Source: Kaggle — Healthcare Dataset
- Raw Records: 55,500
- Records after Deduplication: [paste your number here]
- Fields: 15 columns covering patient demographics, clinical data, 
  operational data, and financial data
- Note: Dataset is synthetically generated with deliberate 
  distributional balance across most variables

## Tools Used
- Microsoft Excel (data cleaning, calculated fields)
- Tableau Public (dashboard development)
- GitHub (documentation and version control)

## Data Quality Findings
A systematic data quality audit was conducted prior to analysis:

1. **Duplicate Records:** ~500 duplicate rows identified and 
   removed prior to analysis
2. **Patient Identifier:** Dataset lacks a true Patient ID field. 
   A composite identifier was constructed using Name + Age + Gender 
   to improve patient matching reliability
3. **Synthetic Data Characteristics:** Near-uniform distributions 
   confirmed across Gender, Blood Type, Insurance Provider, Medical 
   Condition, Medication, Billing Amount, and Length of Stay — 
   consistent with synthetic data generation
4. **Readmission Analysis:** 30-day readmission analysis conducted 
   using composite Patient_ID. Only 9 readmission events identified 
   across 55,000+ records — statistically insufficient for pattern 
   analysis. Documented as a dataset limitation rather than 
   presenting misleading results

## Dashboard Structure

### Dashboard 1 — Executive Summary
High level KPIs including total patients, total admissions, 
average length of stay, and average billing amount

### Dashboard 2 — Patient Demographics
Patient population analysis by age, gender, blood type, 
insurance provider, and billing by age group

### Dashboard 3 — Admissions & Operations
Admissions volume trends, seasonal patterns, length of stay 
by admission type, and top hospitals by volume

### Dashboard 4 — Financial Analysis
Billing analysis by insurance provider, medical condition, 
admission type, and length of stay by condition

### Dashboard 5 — Data Quality & Methodology
Duplicate record analysis, Patient ID frequency distribution, 
dataset characteristics summary, and readmission methodology notes

## Key Findings

1. **Age as Primary Cost Driver:** Despite uniform patient 
   distribution across age groups, patients aged 65+ generate 
   500M+ in total billing — nearly 60% more than the 18-35 cohort 
   and double the 36-65 group. Age is the single most significant 
   cost differentiator in this dataset

2. **Length of Stay:** Average 15-day inpatient stay suggests a 
   patient population with complex or chronic conditions

3. **Average Billing:** $25,000 average billing per admission 
   with no significant variation across insurance providers, 
   medical conditions, or admission types — consistent with 
   synthetic data generation

4. **Seasonal Admissions Pattern:** February consistently records 
   the lowest admission volume across all years, suggesting 
   predictable capacity planning opportunities

5. **Uniform Clinical Variables:** Medical condition, medication, 
   test results, and length of stay show near-uniform distribution 
   across all categories. Age remains the only significant cost 
   differentiator identified through systematic analysis

## Data Limitations
- Patient identity relies on composite key (Name + Age + Gender) 
  rather than a true unique identifier
- Synthetic data generation limits clinical and operational 
  insight depth
- Readmission analysis requires longitudinal patient encounter 
  history not present in this dataset
- Real-world healthcare analytics would leverage true Patient_ID, 
  ICD-10 diagnosis codes, DRG classifications, and payer 
  contract details

## Tableau Public Dashboard
[Insert your Tableau Public URL here]

## Relevance to Healthcare Analytics
This project reflects analytical approaches applied during a 
graduate analytics engagement with MultiCare Health Systems, 
where predictive modeling was used to identify emergency revisit 
risk in senior patients — representing approximately $500,000 
in annual Medicare penalty impact.
