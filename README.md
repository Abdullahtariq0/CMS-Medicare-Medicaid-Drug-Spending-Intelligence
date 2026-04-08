# CMS Medicare & Medicaid Drug Spending Intelligence
### Part D, Part B & Medicaid Drug Spending (2019–2023) — by The Data Developers

[![Snowflake Marketplace](https://img.shields.io/badge/Available%20on-Snowflake%20Marketplace-29B5E8?style=flat&logo=snowflake)](https://app.snowflake.com/marketplace)
[![Data Source](https://img.shields.io/badge/Source-CMS%20Drug%20Spending-blue)](https://data.cms.gov/summary-statistics-on-use-and-payments/medicare-medicaid-spending-by-drug)
[![License](https://img.shields.io/badge/License-Commercial-green)](https://www.thedatadevelopers.com)
[![Coverage](https://img.shields.io/badge/Coverage-Medicare%20%26%20Medicaid%202019--2023-orange)](https://data.cms.gov)

---

## Overview

The **CMS Medicare & Medicaid Drug Spending Intelligence** dataset by **The Data Developers** delivers the definitive official source for US government drug expenditure — structured, normalized, and query-ready directly in your Snowflake environment.

Published annually, these datasets cover Medicare Part D, Medicare Part B, and Medicaid drug spending with granular metrics on total spending, dosage units, claims volume, beneficiary counts, average cost per claim, year-over-year price change, and 4-year compound annual growth rate — for every drug reimbursed under each program.

Four fully structured tables give market access teams, pricing analysts, health economists, payer strategy professionals, and government affairs teams the intelligence they need to track drug price trends, benchmark competitor spending, analyze market dynamics, and support formulary decisions — entirely in SQL.

---

## Scale & Coverage

| Metric | Value |
|--------|-------|
| Medicare Part D Drug Records | 14,309 |
| Medicaid Drug Records | 16,938 |
| Medicare Part B HCPCS Drug Codes | 734 |
| Part B Discarded Drug Records | 824 |
| Years of Spending Data | 2019 — 2023 (5 years) |
| Programs Covered | Medicare Part D, Part B, Medicaid |
| Tables | 4 |
| Update Frequency | Annual |

---

## Database Structure

**Schema:** `DRUG_SPENDING`

All 4 tables share a common structure — drug name and manufacturer as the primary identifiers, with annual spending metrics spanning 2019–2023 as wide columns.

---

## Table Reference

### PART_D_SPENDING
**Medicare Part D Drug Spending by Brand and Manufacturer**

One row per brand name + manufacturer combination. Covers all drugs prescribed under Medicare Part D (self-administered outpatient drugs) with 5 years of annual spending metrics.

| Column | Description |
|--------|-------------|
| `BRND_NAME` | Brand name of the drug |
| `GNRC_NAME` | Generic name of the drug |
| `TOT_MFTR` | Total number of manufacturers |
| `MFTR_NAME` | Manufacturer name — use 'Overall' for drug-level totals |
| `TOT_SPNDNG_2019` | Total spending 2019 |
| `TOT_DSG_UNTS_2019` | Total dosage units dispensed 2019 |
| `TOT_CLMS_2019` | Total claims 2019 |
| `TOT_BENES_2019` | Total beneficiaries 2019 |
| `AVG_SPND_PER_DSG_UNT_WGHTD_2019` | Weighted average spending per dosage unit 2019 |
| `AVG_SPND_PER_CLM_2019` | Average spending per claim 2019 |
| `AVG_SPND_PER_BENE_2019` | Average spending per beneficiary 2019 |
| `OUTLIER_FLAG_2019` | Outlier flag 2019 (1 = high cost outlier) |
| `TOT_SPNDNG_2020` | Total spending 2020 |
| `TOT_DSG_UNTS_2020` | Total dosage units 2020 |
| `TOT_CLMS_2020` | Total claims 2020 |
| `TOT_BENES_2020` | Total beneficiaries 2020 |
| `AVG_SPND_PER_DSG_UNT_WGHTD_2020` | Weighted avg spending per dosage unit 2020 |
| `AVG_SPND_PER_CLM_2020` | Average spending per claim 2020 |
| `AVG_SPND_PER_BENE_2020` | Average spending per beneficiary 2020 |
| `OUTLIER_FLAG_2020` | Outlier flag 2020 |
| `TOT_SPNDNG_2021` | Total spending 2021 |
| `TOT_DSG_UNTS_2021` | Total dosage units 2021 |
| `TOT_CLMS_2021` | Total claims 2021 |
| `TOT_BENES_2021` | Total beneficiaries 2021 |
| `AVG_SPND_PER_DSG_UNT_WGHTD_2021` | Weighted avg spending per dosage unit 2021 |
| `AVG_SPND_PER_CLM_2021` | Average spending per claim 2021 |
| `AVG_SPND_PER_BENE_2021` | Average spending per beneficiary 2021 |
| `OUTLIER_FLAG_2021` | Outlier flag 2021 |
| `TOT_SPNDNG_2022` | Total spending 2022 |
| `TOT_DSG_UNTS_2022` | Total dosage units 2022 |
| `TOT_CLMS_2022` | Total claims 2022 |
| `TOT_BENES_2022` | Total beneficiaries 2022 |
| `AVG_SPND_PER_DSG_UNT_WGHTD_2022` | Weighted avg spending per dosage unit 2022 |
| `AVG_SPND_PER_CLM_2022` | Average spending per claim 2022 |
| `AVG_SPND_PER_BENE_2022` | Average spending per beneficiary 2022 |
| `OUTLIER_FLAG_2022` | Outlier flag 2022 |
| `TOT_SPNDNG_2023` | Total spending 2023 |
| `TOT_DSG_UNTS_2023` | Total dosage units 2023 |
| `TOT_CLMS_2023` | Total claims 2023 |
| `TOT_BENES_2023` | Total beneficiaries 2023 |
| `AVG_SPND_PER_DSG_UNT_WGHTD_2023` | Weighted avg spending per dosage unit 2023 |
| `AVG_SPND_PER_CLM_2023` | Average spending per claim 2023 |
| `AVG_SPND_PER_BENE_2023` | Average spending per beneficiary 2023 |
| `OUTLIER_FLAG_2023` | Outlier flag 2023 |
| `CHG_AVG_SPND_PER_DSG_UNT_22_23` | Year-over-year price change 2022→2023 (decimal) |
| `CAGR_AVG_SPND_PER_DSG_UNT_19_23` | 4-year CAGR of avg spending per dosage unit 2019→2023 |

---

### PART_B_SPENDING
**Medicare Part B Drug Spending at HCPCS Level**

One row per HCPCS drug code. Covers physician-administered drugs billed under Medicare Part B (infusions, injections, biologics administered in clinical settings) with 5 years of annual spending metrics plus the 2023 Average Sales Price.

| Column | Description |
|--------|-------------|
| `HCPCS_CD` | HCPCS procedure code — primary identifier for Part B drugs |
| `HCPCS_DESC` | HCPCS code description |
| `BRND_NAME` | Brand name |
| `GNRC_NAME` | Generic name |
| `TOT_SPNDNG_2019` | Total spending 2019 |
| `TOT_DSG_UNTS_2019` | Total dosage units 2019 |
| `TOT_CLMS_2019` | Total claims 2019 |
| `TOT_BENES_2019` | Total beneficiaries 2019 |
| `AVG_SPNDNG_PER_DSG_UNT_2019` | Average spending per dosage unit 2019 |
| `AVG_SPNDNG_PER_CLM_2019` | Average spending per claim 2019 |
| `AVG_SPNDNG_PER_BENE_2019` | Average spending per beneficiary 2019 |
| `OUTLIER_FLAG_2019` | Outlier flag 2019 |
| `TOT_SPNDNG_2020` — `OUTLIER_FLAG_2023` | Same metrics for 2020, 2021, 2022, 2023 |
| `AVG_DY23_ASP_PRICE` | 2023 Average Sales Price (ASP) — used for Medicare reimbursement rate setting |
| `CHG_AVG_SPNDNG_PER_DSG_UNT_22_23` | YoY price change 2022→2023 |
| `CAGR_AVG_SPND_PER_DSG_UNT_19_23` | 4-year CAGR 2019→2023 |

---

### MEDICAID_SPENDING
**Medicaid Drug Spending by Brand and Manufacturer**

One row per brand name + manufacturer combination. Covers all drugs reimbursed under state Medicaid programs with 5 years of annual spending metrics. Note: Medicaid does not include beneficiary counts due to state reporting variation.

| Column | Description |
|--------|-------------|
| `BRND_NAME` | Brand name |
| `GNRC_NAME` | Generic name |
| `TOT_MFTR` | Total number of manufacturers |
| `MFTR_NAME` | Manufacturer name — use 'Overall' for drug-level totals |
| `TOT_SPNDNG_2019` | Total Medicaid spending 2019 |
| `TOT_DSG_UNTS_2019` | Total dosage units 2019 |
| `TOT_CLMS_2019` | Total claims 2019 |
| `AVG_SPND_PER_DSG_UNT_WGHTD_2019` | Weighted avg spending per dosage unit 2019 |
| `AVG_SPND_PER_CLM_2019` | Average spending per claim 2019 |
| `OUTLIER_FLAG_2019` | Outlier flag 2019 |
| `TOT_SPNDNG_2020` — `OUTLIER_FLAG_2023` | Same metrics for 2020, 2021, 2022, 2023 |
| `CHG_AVG_SPND_PER_DSG_UNT_22_23` | YoY price change 2022→2023 |
| `CAGR_AVG_SPND_PER_DSG_UNT_19_23` | 4-year CAGR 2019→2023 |

---

### PART_B_DISCARDED
**Medicare Part B Discarded Drug Units**

One row per HCPCS drug code. Documents the split between administered and discarded drug units for Medicare Part B drugs — enabling waste analysis and cost efficiency benchmarking.

| Column | Description |
|--------|-------------|
| `HCPCS_CD` | HCPCS procedure code — join to PART_B_SPENDING |
| `BRND_NAME` | Brand name |
| `GNRC_NAME` | Generic name |
| `TOT_MDCR_ALOWD_AMT` | Total Medicare allowed amount (administered + discarded) |
| `TOT_MDCR_ALOWD_ADMNRD_AMT` | Medicare allowed amount for administered units only |
| `TOT_MDCR_ALOWD_DSCRD_AMT` | Medicare allowed amount for discarded units |
| `PCT_ADMNRD_UNITS` | Percentage of units administered (decimal) |
| `PCT_DSCRD_UNITS` | Percentage of units discarded/wasted (decimal) |

---

## Data Model

```
PART_D_SPENDING
  BRND_NAME + MFTR_NAME (compound key)
  Wide format: 2019-2023 metrics as columns
  Filter MFTR_NAME = 'Overall' for drug-level totals

MEDICAID_SPENDING
  BRND_NAME + MFTR_NAME (compound key)
  Wide format: 2019-2023 metrics as columns
  Filter MFTR_NAME = 'Overall' for drug-level totals

PART_B_SPENDING
  HCPCS_CD (primary key) ──────────────────────► PART_B_DISCARDED
  Wide format: 2019-2023 metrics as columns        HCPCS_CD (join key)
  Includes ASP price for 2023

Cross-program join:
  PART_D_SPENDING.BRND_NAME ◄──► MEDICAID_SPENDING.BRND_NAME
  (join on GNRC_NAME for generic equivalence)
```

---

## Key Concepts

**MFTR_NAME = 'Overall'**
Each drug appears multiple times in PART_D_SPENDING and MEDICAID_SPENDING — once per manufacturer and once with `MFTR_NAME = 'Overall'` representing the drug-level aggregate. For drug-level analysis always filter `WHERE MFTR_NAME = 'Overall'`. For manufacturer-level analysis filter to a specific manufacturer name.

**Wide Format Structure**
Unlike transactional datasets, CMS drug spending data is published in wide format — each row covers multiple years as separate columns (e.g. `TOT_SPNDNG_2019`, `TOT_SPNDNG_2020`, etc.). This makes year-over-year trend analysis straightforward without joins.

**CAGR and YoY Columns**
`CAGR_AVG_SPND_PER_DSG_UNT_19_23` is the 4-year compound annual growth rate of the average spending per dosage unit from 2019 to 2023 — stored as a decimal (e.g. 0.08 = 8% CAGR). `CHG_AVG_SPND_PER_DSG_UNT_22_23` is the 1-year change from 2022 to 2023, also as a decimal. Multiply by 100 for percentage display.

**Outlier Flag**
`OUTLIER_FLAG = 1` indicates a drug with unusually high spending relative to its utilization — typically ultra-high-cost specialty drugs. Use this flag to separate standard drugs from outlier analysis.

**Average Sales Price (ASP)**
`AVG_DY23_ASP_PRICE` in PART_B_SPENDING is the 2023 Average Sales Price — the CMS-calculated price used to set Medicare Part B reimbursement rates at 106% of ASP. This is a critical reference price for market access and pricing strategy teams.

**Part B vs Part D**
Part D covers self-administered drugs (pills, patches, inhalers). Part B covers physician-administered drugs (infusions, injections, biologics). These are separate markets with different reimbursement mechanics — compare them to understand the full government drug spending landscape for any drug.

---

## Use Cases

**Drug Price Trend Analysis**
Track 5-year price trajectories across Medicare and Medicaid simultaneously — identifying drugs with accelerating price growth, declining prices, or outlier cost patterns using CAGR and YoY metrics.

**Market Access & Payer Strategy**
Understand the real-world government reimbursement landscape for any drug — total spending, claims volume, beneficiary reach, and cost per claim across Medicare Part D, Part B, and Medicaid.

**Competitive Spending Intelligence**
Compare government spending on your drug vs competitor drugs in the same therapeutic class — identifying where competitors are gaining or losing reimbursement share across government payers.

**Part B Waste & Efficiency Analysis**
Join PART_B_SPENDING with PART_B_DISCARDED to identify drugs with high discard rates — quantifying the dollar value of waste and benchmarking against program averages for formulary and packaging decisions.

**IRA Drug Price Negotiation Intelligence**
The Inflation Reduction Act targets high-spend Medicare drugs for price negotiation. This dataset identifies the highest-spend, highest-CAGR drugs in Part D and Part B — exactly the profiles CMS uses to select negotiation candidates.

**Formulary Management**
Health plans and pharmacy benefit managers use CMS spending data to benchmark drug costs, model formulary impact, and support formulary tier placement decisions across Medicare and Medicaid populations.


---

## About The Data Developers

The Data Developers is a biomedical data intelligence company providing structured, query-ready life sciences datasets on Snowflake Marketplace and Google Cloud Marketplace.

**Website:** [thedatadevelopers.com](https://www.thedatadevelopers.com)
**Contact:** support.marketplace@thedatadevelopers.com
