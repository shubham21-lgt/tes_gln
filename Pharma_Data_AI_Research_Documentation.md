
# Pharma Data & AI Research Documentation  
## OOS / OOT + GB – Indore Project

---

# 1. Project Overview

This document summarizes the research, metadata analysis, folder structure mapping, and data understanding activities performed for the:

**Glenmark Data & AI → Big Bets → OOS-OOT + GB - Indore**

initiative.

The objective of this work is to:

- Understand pharma manufacturing and quality datasets
- Build a metadata catalogue
- Create cross-system relationships
- Identify data lineage
- Prepare structured + unstructured data for analytics and AI use cases
- Enable OOS/OOT investigation intelligence
- Build an AI-ready pharma knowledge repository

---

# 2. High-Level Folder Structure

```text
Glenmark Data & AI
└── Projects
    └── Big Bets
        └── OOS-OOT + GB - Indore
            └── Data Received From Indore
                ├── APQR
                ├── Baseline Data
                ├── BPR
                ├── CPV
                ├── Deviation
                ├── Incident
                ├── Investigations
                ├── LIMS report
                ├── Machine list OSD Manufacturing
                ├── MFG Plant Layout
                ├── OOS OOT SOP
                ├── RM SFG FG Specification
                ├── SAP_t_codes
                └── Yield Data
```

---

# 3. Major Data Domains Identified

| Domain | Purpose |
|---|---|
| APQR | Annual Product Quality Review |
| BPR | Batch Production Records |
| CPV | Continued Process Verification |
| OOS | Out of Specification |
| OOT | Out of Trend |
| LIMS | Laboratory Information Management System |
| SAP | ERP & manufacturing master data |
| PAS-X | MES / manufacturing execution |
| Trackwise | Quality event management |
| Incident | Investigation tracking |
| Deviation | Process deviation tracking |
| SOP | Standard operating procedures |
| Yield Data | Manufacturing efficiency analysis |

---

# 4. Understanding Yield Data

Yield Data means how much final product was successfully produced compared to expected production.

Example:
- Raw material input = 100 kg
- Final tablets produced = 92 kg
- Yield = 92%

Used for:
- process efficiency
- loss analysis
- machine performance
- batch optimization
- deviation investigation

---

# 5. Metadata Catalogue Design

The metadata catalogue includes:
- file-level metadata
- field-level metadata
- source system mapping
- joins
- data types
- AI model usage
- business meaning

---

# 6. Recommended Excel Workbook Structure

## Sheet 1 — Master Document Inventory
Contains:
- file name
- folder path
- source system
- file type
- owner
- business domain

## Sheet 2 — Metadata Catalogue

## Sheet 3 — Relationship Mapping

## Sheet 4 — Data Lineage

## Sheet 5 — OOS/OOT Mapping

## Sheet 6 — CPP/CQA/CMA Mapping

## Sheet 7 — AI Readiness Assessment

---

# 7. Important Relationships Identified

```text
SAP
 └── Process Order
      └── PAS-X
           └── BPR
                └── Batch Number
                     └── LIMS
                          └── OOS/OOT
                               └── Trackwise
                                    └── Investigation
```

---

# 8. Suggested Next Analysis

- Data lineage mapping
- Batch genealogy
- OOS pattern analysis
- Yield vs OOS analysis
- Machine correlation analysis
- AI-ready document preparation

---

# 9. AI / GenAI Opportunities

| Use Case | Description |
|---|---|
| RCA Assistant | Root cause recommendation |
| SOP Chatbot | SOP search assistant |
| Batch Intelligence | Batch traceability |
| Investigation Summarizer | Auto-summary from PDFs |
| Knowledge Graph | Relationship understanding |
| OOS Prediction | Predict risk batches |
| Process Optimization | Yield improvement |

---

# 10. Final Conclusion

The work performed has evolved into:
- Pharma Data Architecture
- Manufacturing Intelligence Framework
- Metadata Governance Platform
- AI-ready Knowledge Repository

The next major milestone should focus on:
- relationship mapping
- lineage
- batch genealogy
- AI use-case preparation
- structured + unstructured integration

##
Glenmark Data & AI
└── Projects
    └── Big Bets
        └── OOS-OOT + GB - Indore
            └── Data Received From Indore
                │
                ├── APQR
                │   └── APQR Lacosamide Tab (US)
                │       ├── Summary Report.pdf
                │       ├── Annexure - V (A).pdf
                │       ├── Annexure - V (B).pdf
                │       ├── Annexure - V (C).pdf
                │       ├── Annexure - V (D).pdf
                │       ├── Annexure - VI (A).pdf
                │       ├── Annexure - VI (B).pdf
                │       ├── Annexure - VI (C).pdf
                │       ├── Annexure - VI (D).pdf
                │       └── Lacosamide Tablets USP
                │
                ├── Baseline Data
                │   ├── LER Tracker (2023 to 2026).xlsx
                │   ├── OOS-Trackwise-Raw-Data.xlsx
                │   ├── OOT-Trackwise-Raw-Data.xlsx
                │   └── Product-Wise-Batches.xlsx
                │
                ├── BPR
                │   └── Lacosamide BPR
                │       ├── 17260123 MFG CL.pdf
                │       ├── 17260142 MFG CL.pdf
                │       ├── 17260142 PKG CL.pdf
                │       ├── 17260142 pkg PRINTOUT_001.pdf
                │       ├── Lacosamide 100mg MFG.pdf
                │       ├── Lacosamide 100mg PKG BPR.pdf
                │       ├── Lacosamide 50mg MFG.pdf
                │       └── Lacosamide 50mg PKG BPR.pdf
                │
                ├── CPV
                │   ├── CPV Lacosamide Tablets USP 100 mg
                │   ├── CPV Lacosamide Tablets USP 50 mg
                │   ├── CPV Perindopril Tert-Butylamine Tablets
                │   └── CPV Nebivolol Tablets 5 mg
                │
                ├── Deviation
                │   └── Deviation list 2025.xlsx
                │
                ├── Incident
                │   ├── 318867_Incident Investigation Report.pdf
                │   ├── Incident Detail.xlsx
                │   └── Incident Tracker (2023 to 2026).xlsx
                │
                ├── Investigations
                │   └── Investigation report
                │       ├── Investigation report track.xlsx
                │       ├── LACOSAMIDE TAB 50MG.pdf
                │       ├── Lacosamide Tablets_OOS Investigation Summary.pdf
                │       ├── Lacosamide Tablets USP 50 mg Phase II.pdf
                │       ├── OOS 1B Report Lacosamide Tablets.pdf
                │       ├── OOS 1B Report Product Name Perindopril.pdf
                │       ├── OOS Summary Perindopril Tert-Butylamine.pdf
                │       ├── OOS111120250172-Perindopril.pdf
                │       └── PERINDOPRIL TERT-BUTYLAMINE.pdf
                │
                ├── LIMS report
                │
                ├── Machine list OSD Manufacturing
                │   ├── Copy of May Mfg and Pkg Plan Final.xlsx
                │   ├── Instrument List.xlsx
                │   ├── Machine list OSD Manufacturing-old version.xlsx
                │   └── Machine list OSD Manufacturing.xlsx
                │
                ├── MFG Plant Layout
                │
                ├── OOS OOT SOP
                │   └── SOP
                │       ├── GSOP020.04 Investigation of Out of Specification.pdf
                │       ├── GSOP021.02 Investigation of Out of Trend.pdf
                │       └── Investigation report.xlsx
                │
                ├── RM SFG FG Specification
                ├── SAP_t_codes
                └── Yield Data