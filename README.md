# README

# Acute Myeloid Leukemia Heatmap Analysis

This project analyzes RNA-seq data from acute myeloid leukemia (AML) model mice using the refine.bio platform. The goal is to create a clustered heatmap visualizing gene expression patterns across different AML subtypes and treatments.

## Software Requirements

- R (version 4.0+)
- RStudio IDE
- pheatmap package
- readr package
- dplyr package

## Project Overview

### Purpose

This analysis aims to:

1. Explore gene expression patterns across 19 AML model mice samples
2. Identify clusters of genes and samples based on RNA-seq data
3. Visualize the clustering using an annotated heatmap
4. Examine how AML subtypes (IDH2 mutant vs TET2 mutant) and treatments affect gene expression

### Data Source

The project uses pre-processed RNA-seq data from refine.bio for Shih et al., 2017 [2]. This dataset contains:

- 19 AML model mouse samples
- RNA-seq results for AML under controlled treatment conditions
- Pre-processed and quantile-normalized data

## Key Components

1. **Data Import**:

   - Reads in metadata and RNA-seq data from refine.bio
   - Ensures proper ordering of data and metadata

2. **Gene Selection**:

   - Filters top 90% most variable genes across samples

3. **Heatmap Creation**:

   - Uses pheatmap to create clustered heatmaps
   - Annotates samples with mutation type (TET2, IDH2, WT)
   - Customizes color scheme and scale

4. **Visualization**:
   - Saves annotated heatmap as PNG file
   - Provides interactive visualization options

## Usage Instructions

1. Install required R packages:

   ```
   install.packages(c("pheatmap", "readr", "dplyr"))
   ```

2. Run the R script to generate the heatmap analysis

3. View the generated PNG file in the "plots" directory

## Additional Information

- Session info and package versions used are saved in the output
- Results folder contains filtered gene expression data
- Metadata and sample information are available in separate TSV files

## References

[2] Shih et al., 2017. IDH mutations in acute myeloid leukemia genome sequencing and functional studies. Nature Medicine, 23(11), 1378–1385. https://pubmed.ncbi.nlm.nih.gov/28193779/

This README provides a comprehensive overview of the project, including software requirements, purpose, data source, key components, usage instructions, and references. It gives users a clear understanding of what the project does, how to run it, and where to find important information and outputs.

Citations:
[1] https://github.com/prabhakarlab/RCAv2/blob/master/README.md
[2] https://github.com/kevinblighe/E-MTAB-6141/blob/master/README.md
[3] https://github.com/quadbio/scRNAseq_analysis_vignette/blob/master/Tutorial.md
[4] https://github.com/interactivereport/Quickomics/blob/master/README.md
[5] https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html
[6] https://github.com/BCCHR-trainee-omics-group/StudyGroup/blob/master/workshops/2020-05-26_Heatmaps_and_PCA/Heatmaps_and_PCA.md
[7] https://github.com/NBISweden/workshop-RNAseq/blob/master/lab_eda.Rmd
[8] https://cran.r-project.org/web/packages/TOmicsVis/readme/README.html
[9] https://github.com/satijalab/seurat/issues/2486
[10] https://www.bioconductor.org/packages/release/bioc/vignettes/DESeq2/inst/doc/DESeq2.html
