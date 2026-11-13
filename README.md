# Kolmogorov–Arnold Networks for Computer Vision: A Systematic Review

Supplementary data for the systematic review **"Kolmogorov–Arnold Networks for Computer Vision: A Systematic Review of Reliability, Design, Robustness, and Interpretability"**.

The review looks at how Kolmogorov–Arnold Network (KAN) components behave in computer vision across four research questions:

| RQ | Focus |
|---|---|
| RQ1 | Reliability and reproducibility of comparative experiments |
| RQ2 | KAN design choices (basis function, grid, depth, integration pattern), accuracy, cost and training stability |
| RQ3 | Robustness, distribution shift and uncertainty |
| RQ4 | Interpretability and how well it is substantiated |

This repository holds the study-level records behind every count, figure and table in the paper. Anyone can trace an aggregate number back to the individual studies, the reviewer judgments and the passages extracted from the source papers.

## At a glance

| Item | Value |
|---|---|
| Search window | 1 January 2024 to 26 June 2026 |
| Sources | Scopus (474), Web of Science (284), IEEE Xplore (120), ACM Digital Library (68), arXiv (710) |
| Records identified | 1,656 |
| Duplicates removed | 320 |
| Records screened | 1,336 |
| Full texts assessed | 321 (8 not retrieved) |
| Studies included | **104** |
| Study by RQ judgments | 295 (RQ1 = 104, RQ2 = 104, RQ3 = 49, RQ4 = 38) |
| Reviewers | 3 independent reviewers (R1, R2, R3) plus recorded consensus |
| Reporting guideline | PRISMA 2020 |

## Repository contents

```
.
├── README.md
├── KAN_SLR_Supplementary_1.xlsx                    # Workbook 1: compact review data
└── KAN_SLR_Supplementary_2_Reviewer_Evidence.xlsx  # Workbook 2: reviewer audit and evidence
```

Both workbooks use the same stable study identifiers (`INC-001`, `INC-002`, ...), so a study can be followed across every sheet in both files. The manuscript's Supplementary Material lists the same identifiers next to each citation.

### Workbook 1: compact review data

`KAN_SLR_Supplementary_1.xlsx`

| Sheet | Rows | Contents |
|---|---|---|
| `README` | | Purpose, scope, code definitions and provenance |
| `01_Search_PRISMA` | | Exact search string for each database, date filters, record counts, PRISMA selection counts, and the inclusion (IC1 to IC6) and exclusion (EC1 to EC9) criteria |
| `02_Study_Index` | 104 | One row per included study: title, RQ coverage, RQ4 interpretability substantiation, TECS score and category, overall risk of bias, and short evidence summaries |
| `03_RQ_Audit` | 295 | One row per study and RQ: Direct or Supporting mapping, R1/R2/R3 audit scores, consensus score, reviewer agreement, extraction confidence, final consensus confidence, page number and supporting quotation |
| `04_TECS` | 104 | Eight theme scores (T1 to T8, each 0 to 4), RQ subtotals (0 to 8), total TECS (0 to 32), category and reviewer votes |
| `05_RoB` | 104 | Consensus judgment and R1/R2/R3 votes for each of the eight risk-of-bias domains, plus overall judgments |

### Workbook 2: reviewer audit and evidence

`KAN_SLR_Supplementary_2_Reviewer_Evidence.xlsx`

| Sheet | Rows | Contents |
|---|---|---|
| `README` | | Purpose, scope and reading notes |
| `Evidence_Master` | 295 | Full evidence record for each study and RQ: theme, mapping strength, evidence summary, page, extracted full-text passage, each reviewer's score and stated basis, agreement and consensus |
| `Thematic_R1`, `Thematic_R2`, `Thematic_R3` | 295 each | Each reviewer's independent RQ evidence-strength audit with reasoning |
| `Thematic_Alignment` | 295 | The three audit scores side by side with agreement and consensus |
| `RoB_R1`, `RoB_R2`, `RoB_R3` | 104 each | Each reviewer's independent judgment and evidence basis for all eight risk-of-bias domains, with an overall judgment and rationale |
| `RoB_Alignment` | 104 | The three risk-of-bias ratings side by side with consensus and agreement for every domain |
| `Codebook` | | Operational criteria for the evidence audit (A1 to A4) and the eight risk-of-bias domains |
| `TECS_All_Papers` | 104 | Consensus TECS theme scores, RQ subtotals, total and classification |
| `TECS_Reviewer_Scores` | 312 | Each reviewer's TECS ratings for each study |
| `TECS_Evidence` | 832 | Theme-level evidence summaries, page numbers, extracted passages and reviewer justifications for T1 to T8 |
| `TECS_Codebook` | | Definitions and scoring anchors for the eight TECS themes |

## Assessment frameworks

The review uses three separate instruments, and they measure different things. A high TECS score does not mean low risk of bias, and the reverse holds too.

**1. Evidence-strength audit (1 to 3).** For each study and RQ, three reviewers rated the extracted evidence as 1 Limited, 2 Adequate or 3 Strong. The median gives the consensus score, which maps to the final confidence category: 3 High, 2 Moderate, 1 Low. Across the 295 judgments this produced 211 High, 63 Moderate and 21 Low.

**2. Thematic Evidence Contribution Score (TECS, 0 to 32).** This score measures how much a study contributes to each theme. It does not measure study quality.

| Theme | Name | RQ |
|---|---|---|
| T1 | Comparative benchmark strength | RQ1 |
| T2 | Reproducibility and experimental reliability | RQ1 |
| T3 | KAN functional and structural design exploration | RQ2 |
| T4 | Efficiency and training stability | RQ2 |
| T5 | Adversarial robustness | RQ3 |
| T6 | Distribution shift and uncertainty | RQ3 |
| T7 | Intrinsic interpretability | RQ4 |
| T8 | Post-hoc interpretability and validation | RQ4 |

Each theme is scored 0 to 4. RQ1 = T1 + T2, RQ2 = T3 + T4, RQ3 = T5 + T6, RQ4 = T7 + T8. Categories: 0 to 7 Peripheral, 8 to 15 Supporting, 16 to 23 Substantial, 24 to 28 Strong multi-theme, 29 to 32 Exceptional.

**3. Risk of bias (eight domains).**

| Domain | Focus |
|---|---|
| RoB1 | Data and benchmark selection |
| RoB2 | Baseline fairness |
| RoB3 | Hyperparameter and design search |
| RoB4 | Statistical reliability and reproducibility |
| RoB5 | Computational-efficiency reporting |
| RoB6 | Robustness evaluation (only for RQ3-mapped studies) |
| RoB7 | Interpretability evidence (only for RQ4-mapped studies) |
| RoB8 | Selective reporting and conclusion bias |

Codes: `L` Low, `SC` Some concerns, `H` High, `NA` not applicable. Overall consensus: 20 Low, 80 Some concerns, 4 High.

## License

The data in this repository are released under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Quoted passages from the included studies remain the copyright of their original authors and publishers. They are reproduced only as short excerpts to support the evidence assessment.
