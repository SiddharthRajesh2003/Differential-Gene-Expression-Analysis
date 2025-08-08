# Differential Gene Expression Analysis

This folder contains an example pipeline for downstream RNA-seq analysis, focusing on differential gene expression (DEG) using R and Bioconductor packages.

## Contents

- `deg_analysis.qmd`: Quarto markdown source for the analysis workflow.
- `deg_analysis.html`: Rendered HTML output of the analysis.
- `GSE268309_FullTable_RawCounts_Validation_dataset.txt`: Raw counts validation dataset from GEO accession GSE268309.
- `deg_analysis_files/`: Supporting files for the HTML report.
  - `figure-html/`: Output figures (plots, heatmaps, etc.).
  - `libs/`: Libraries for HTML rendering (Bootstrap, Quarto, ClipboardJS).

## Workflow Overview

1. **Loading Libraries**: Uses packages such as DESeq2, ggplot2, pheatmap, biomaRt, GEOquery, and others.
2. **Data Import**: Loads raw count data and phenotype information from GEO.
3. **Preprocessing**: Handles duplicate gene IDs, normalizes counts, and prepares phenotype data.
4. **DESeq2 Analysis**: Constructs DESeq2 object, estimates size factors, runs differential expression analysis.
5. **Annotation**: Maps Ensembl gene IDs to gene symbols and other metadata using biomaRt.
6. **Visualization**: Generates PCA plots, MA plots, volcano plots, and heatmaps of top differentially expressed genes.
7. **Output**: Results are rendered in an interactive HTML report.

## How to Run

1. Open `deg_analysis.qmd` in [Visual Studio Code](deg_analysis.qmd) or Quarto-compatible editor.
2. Ensure R and required packages are installed.
3. Render the report:
   ```sh
   quarto render deg_analysis.qmd
   ```