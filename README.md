# Genome Analysis Pipeline
This repository accompanies the MSc thesis **“Addressing Missing Heritability in Inherited Retinal Dystrophies: A Comprehensive, Phenotype-Driven Genome Analysis Pipeline for Novel Variant and Gene Discovery”** by Layla Ahmed (2025).

## 🧬 Project Overview

This project implements and validates a two-phase variant analysis pipeline combining:

- **Panel-Gene Analysis (PGA)** — phenotype-driven, targeted gene set analysis for known IRD genes.
- **Whole Genome Analysis (WGA)** — genome-wide discovery of variants (SNVs, indels, SVs) with a flexible scoring system integrating multiple in silico predictors.

This approach improves diagnostic yield by prioritizing non-coding and structural variants frequently missed by standard pipelines.

## ⚙️ Repository Contents

| File                                         | Description                                |
| -------------------------------------------- | ------------------------------------------ |
| `WGA_SNV_hg38_05.25.Rmd`                     | Whole Genome SNV analysis for hg38 builds  |
| `WGA_SV_hg38_05.25.Rmd`                      | Whole Genome SV analysis for hg38 builds   |
| `PGA_SNV_hg38_05.25.Rmd`                     | Panel-Gene SNV analysis for hg38 builds    |
| `PGA_SV_hg38_05.25.Rmd`                      | Panel-Gene SV analysis for hg38 builds     |
| `InheritanceFilter_Recessive_hg38_05.25.Rmd` | Inheritance pattern filtering for AR cases |

Each script processes variant call files and outputs prioritized candidate variants for interpretation.

## 🏷️ Key Features

✅ Integrated SNV, indel, and SV filtering\
✅ Flexible scoring using SIFT, PolyPhen2, REVEL, CADD, SpliceAI, and others\
✅ Customizable for AR and AD inheritance modes\
✅ Supports cross-variant merging for compound heterozygosity detection\
✅ Designed for GRCh38 (hg38); adaptable for GRCh37

## 🧑‍🔬 Intended Use

This pipeline is designed for research use in IRD gene discovery and diagnostic resolution of unsolved cases. Panel-gene lists should be tailored to each proband’s phenotype and clinical data.

## 📄 Requirements

- R (≥ 4.0)
- R packages: `tidyverse`, `data.table`, `vcfR`, `VariantAnnotation`, `GenomicRanges`, `plyr`, etc.
- High-quality GS data (VCF/BAM) with proper annotations

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone <YOUR_REPO_URL>
   ```
2. Edit `.Rmd` scripts to match your data paths and gene panels.
3. Run in RStudio or with `rmarkdown::render()`.
4. Review output files, merge SNV and SV results, and prioritize candidates.


## 🤝 Acknowledgements

Developed under the supervision of Dr. Ajoy Vincent & the Heon Lab, The Hospital for Sick Children, Toronto. Genome sequencing and bioinformatics: The Centre for Applied Genomics (TCAG).


Please cite this thesis if you use or adapt this pipeline:

> Ahmed L., *Addressing Missing Heritability in Inherited Retinal Dystrophies*, MSc Thesis, University of Toronto, 2025.

---

For questions or contributions, please feel free to get in touch.
