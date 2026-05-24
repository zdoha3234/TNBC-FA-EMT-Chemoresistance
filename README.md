# TNBC-FA-EMT-Chemoresistance
Single-cell and bulk transcriptomic analysis identifying the FA-EMT epithelial subset as a driver of chemotherapy resistance in TNBC
# Single-Cell Analysis Identifies a Residual Fatty Acid–EMT Subset Driving Chemotherapy Resistance in TNBC

## Overview
This repository contains the complete analytical pipeline for the manuscript:

> **"Single-Cell Analysis Identifies a Residual Fatty Acid–EMT Subset Driving 
> Chemotherapy Resistance in Triple-Negative Breast Cancer via MIF and MK 
> Ligand–Receptor Signaling"**
> 
> *Cancers* (2026) — Special Issue: Molecular Insights into Drug Resistance in Cancer

## Repository Structure
## Data Availability

All data used in this study are publicly available:

### Single-Cell RNA-seq Data

| Dataset | Accession | Sensitive (S) | Resistant (R) | Description |
|---------|-----------|---------------|---------------|-------------|
| scRNA-seq atlas | [GSE176078](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE176078) | 3 (Chemo_non_TNBC) | 2 (Chemo_TNBC) | Wu et al. 2021 human breast cancer atlas — NAC-treated patients only |

> **Classification:** Chemo_non_TNBC (*n* = 3) = chemotherapy-sensitive (S);  
> Chemo_TNBC (*n* = 2) = chemotherapy-resistant (R)

### Bulk Transcriptomic Validation Cohorts

| Dataset | Accession | Total | Sensitive (S) | Resistant (R) | Description |
|---------|-----------|-------|---------------|---------------|-------------|
| GSE25066 | [GSE25066](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE25066) | 170 | 57 | 113 | NAC-treated TNBC — Hatzis et al. 2011 |
| GSE58812 | [GSE58812](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE58812) | 107 | 76 | 31 | TNBC subtype cohort — Lehmann et al. 2016 |
| **Total** | | **277** | **133** | **144** | |

> **Classification:** Sensitive (S) = pathological complete response (pCR);  
> Resistant (R) = residual disease (RD) |

## Software Requirements

```r
R version 4.3.2
Seurat v4.3.0
CellChat v1.6.1
clusterProfiler v4.6.0
GSVA v1.46.0
limma
survival + survminer
ggplot2, dplyr, patchwork
```

## Analysis Pipeline

| Script | Figure | Description |
|--------|--------|-------------|
| s1_data_processing.Rmd | Figure 1A–E | QC, normalization, UMAP, cell type composition |
| s2_DGE.Rmd | Figure 1F–I, Supp Fig 1–2 | Differential expression, GO enrichment |
| s3_sub_clustering.Rmd | Figure 1J–K, 3A–L | Sub-clustering, subtype annotation |
| s4_cellchat_interaction.Rmd | Figure 4A–F | Ligand–receptor interaction analysis |
| s5_bulk_validation.Rmd | Figure 2A–E | GSVA scoring, survival analysis |

## Citation

If you use this code, please cite:

> Doha Z. et al. Single-Cell Analysis Identifies a Residual Fatty Acid–EMT Subset 
> Driving Chemotherapy Resistance in Triple-Negative Breast Cancer via MIF and MK 
> Ligand–Receptor Signaling. *Cancers* 2026.

## Contact

For questions about the code or analysis, please open a GitHub Issue or contact 
the corresponding author.
