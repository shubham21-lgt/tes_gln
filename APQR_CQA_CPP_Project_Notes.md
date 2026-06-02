# Pharmaceutical APQR / CQA / CPP / In-Process Mapping Project Notes

## Project Background

Senior shared a template and requested:

> Create a common sheet for mapping parameters against batch number.

Purpose:
- Consolidate data from multiple APQR/BPR/CQA/CPP/CMA/In-process documents.
- Create one master batch-level dataset.
- Maintain specification limits in the first row for reference.
- Enable trend analysis, root-cause analysis, reporting, and future analytics/AI use cases.

---

# Email Instructions Received

You can refer to the attached template for creating a common sheet for mapping of parameters against batch number.

Use actual:
- CQA
- CPP
- CMA
- In-process checks

References:
- CQA → Specification for In-process, SFG & FG
- In-process → BPR
- CMA → Specification for individual RM
- CPP → BPR

Maintain specification limits for each parameter in the first row.

---

# Understanding of Data Sources

## CQA (Critical Quality Attributes)

Examples:
- Blend Assay
- Blend Uniformity
- Content Uniformity
- FP Assay
- RS
- Impurity
- LOD

Example values seen:

| Batch No | Assay | LOD |
|-----------|---------|---------|
| 17230522 | 96.1 | 0.7 |
| 17230542 | 99.0 | 0.7 |

---

## CPP (Critical Process Parameters)

Examples:
- Spray Rate
- Blending Time
- Compression Force
- Turret Speed
- Feeder Speed

Example:

| Batch No | Blending Speed | Blending Time | Compression Force |
|-----------|-----------------|-----------------|--------------------|
| 17230522 | 12 | 5 | 4.7-5.1 |
| 17230542 | 12 | 5 | 5.0-5.4 |

---

## In-Process Checks

Examples:
- Tablet Weight
- Thickness
- Diameter
- Hardness
- Friability
- Disintegration Time

Example:

| Batch No | Thickness | Diameter | Hardness |
|-----------|------------|------------|------------|
| 17230522 | 2.39 | 5.00 | 25-52 |
| 17230542 | 2.45 | 5.06 | 26-54 |

---

## CMA (Critical Material Attributes)

Source:
- Raw Material Specifications
- Individual RM Specifications

Examples may include:
- Appearance
- Identification
- Assay
- Impurities
- Moisture related attributes

---

# What Is the Input?

Multiple documents:

- APQR Annexures
- BPR
- CQA sheets
- CPP sheets
- In-process sheets
- CMA sheets
- RM specifications

Examples from screenshots:

- Annexure I(A)
- Annexure IV(A)
- Annexure VI(A)
- Annexure VII(A)

---

# What Is the Expected Output?

One consolidated master sheet.

Example:

| Batch No | Blend Assay | Blend LOD | Thickness | Diameter | Hardness | Blending Speed | Compression Force |
|-----------|------------|------------|------------|------------|------------|------------|------------|
| 17230522 | 96.1 | 0.7 | 2.39 | 5.00 | 25-52 | 12 | 4.7-5.1 |
| 17230542 | 99.0 | 0.7 | 2.45 | 5.06 | 26-54 | 12 | 5.0-5.4 |

Batch Number is the common key.

---

# Why This Dataset Is Being Created

To answer questions such as:

## Example 1

Why did a batch have lower assay?

Compare:
- Blend Assay
- Blend Time
- Compression Force
- Hardness

## Example 2

Why did impurity increase?

Compare:
- Raw material attributes
- CPP values
- In-process values
- CQA results

---

# Template Interpretation

Template columns observed:

- Batch Number
- Blend Assay
- Blend Uniformity
- Content Uniformity
- FP Assay
- RS
- Impurity
- LOD
- Spray Rate
- Blending Time
- Compression Force
- Turret Speed
- Feeder Speed
- Tablet Weight
- Tablet Thickness
- Tablet Hardness
- Friability
- Disintegration Time

These columns are intended to be populated from different source documents.

---

# Recommended Approach

## Phase 1 – Parameter Inventory

Create:

| Parameter | Source |
|------------|---------|
| Blend Assay | CQA |
| Blend Uniformity | CQA |
| Content Uniformity | CQA |
| LOD | CQA |
| Spray Rate | CPP |
| Blending Time | CPP |
| Compression Force | CPP |
| Turret Speed | CPP |
| Thickness | In-process |
| Hardness | In-process |
| Friability | In-process |
| Disintegration Time | In-process |

---

## Phase 2 – Source Mapping

For every parameter capture:

- Parameter Name
- Category
- Source Annexure
- Specification
- Unit

Example:

### Blend Assay

Source:
- Annexure IV(A)

Specification:
- 95–105%

### LOD

Source:
- Annexure IV(A)

Specification:
- NMT 2%

### Compression Force

Source:
- Annexure VII(A)

Specification:
- 2.4–6.4 kN

---

# Diagram

APQR FILES
│
├── CQA
│   ├── Blend Assay
│   ├── LOD
│   └── Impurity
│
├── CPP
│   ├── Blend Time
│   ├── Compression Force
│   └── Turret Speed
│
└── In-Process
    ├── Hardness
    ├── Thickness
    └── Friability

                ↓

MASTER BATCH DATASET

Batch No | Assay | LOD | Force | Hardness

---

# Deliverables Expected

## Deliverable 1

Master batch-wise dataset.

## Deliverable 2

Parameter mapping sheet.

## Deliverable 3

Batch-wise populated values.

## Deliverable 4

Metadata sheet.

Example:

| Field Name | Definition | Source | Data Type |
|------------|------------|---------|-----------|
| Batch Number | Unique manufacturing batch identifier | BPR | String |
| Blend Assay | Assay result of blend | CQA | Decimal |
| Compression Force | Compression force applied | CPP | Decimal |
| Hardness | Tablet hardness | In-process | Decimal |

---

# Questions Recommended For Senior

1. What is the final objective of the sheet?
2. Which parameters are mandatory?
3. Is Batch Number the master key?
4. How many years/batches should be covered?
5. Should metadata also be maintained?
6. Should specification limits be captured?
7. Should Min and Max be stored separately?
8. Should RM/CMA data be in same sheet or separate sheet?

---

# Best Validation Statement

"My understanding is that I need to create a master batch-wise dataset where Batch Number is the key and parameters from CQA, CPP, CMA and In-process checks are consolidated into a single sheet along with specification limits and source mapping."

---

# Immediate Next Steps

## Sheet 1 – Parameter Register

| Parameter Name | Category | Source Document | Specification | Unit |

Examples:

- Blend Assay
- Blend Uniformity
- Content Uniformity
- LOD
- Blending Time
- Compression Force
- Thickness
- Hardness

---

## Sheet 2 – Master Data

| Batch Number | Blend Assay | LOD | Compression Force Min | Compression Force Max | Thickness Min | Thickness Max | Hardness Min | Hardness Max |

---

## Sheet 3 – Metadata

| Field | Definition | Source | Data Type |

---

## Sheet 4 – Source Traceability

| Parameter | Annexure | Sheet | Column |

---

# What Senior Is Likely To Check

### CQAs Identified?

- Blend Assay
- Blend Uniformity
- Content Uniformity
- FP Assay
- RS
- Impurity
- LOD

### CPPs Identified?

- Spray Rate
- Blending Time
- Compression Force
- Turret Speed
- Feeder Speed

### In-Process Checks Identified?

- Tablet Weight
- Thickness
- Diameter
- Hardness
- Friability
- Disintegration Time

### Source Traceability Available?

Every parameter should point back to:
- Annexure
- Sheet
- Source document

---

# Final Understanding

Primary objective is NOT metadata creation.

Primary objective is:

1. Build a batch-level master dataset.
2. Use Batch Number as common key.
3. Consolidate CQA, CPP, CMA and In-process data.
4. Maintain specifications.
5. Enable future analytics and trend analysis.

Metadata can then be built on top of the master dataset.
