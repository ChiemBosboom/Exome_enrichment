# Enhanced Isoform Discovery in the ALS Motor Cortex Using Exome-Enriched Long-Read Sequencing

This repository contains the R and shell scripts used to perform the data processing, analysis, and figure generation for our study comparing standard and exome-enriched long-read RNA sequencing.

## Abstract

Single-nucleus long-read RNA sequencing is a powerful tool for characterizing
cell-type-specific isoform diversity, which is critical for understanding splicing dys-
regulation in neurodegenerative diseases like Amyotrophic Lateral Sclerosis (ALS).
However, its application to postmortem brain tissue is hampered by a high propor-
tion of intronic reads from unspliced pre-mRNA, which severely limits the effective
sequencing depth of full-length transcripts. This problem is addressed by exome
enrichment, which utilizes probes to specifically bind and capture cDNAs that over-
lap known exons . This study provides a systematic evaluation of exome-enriched
long-read sequencing (ExoLR) against standard long-read sequencing (LR) in single
nuclei from postmortem ALS motor cortex. We demonstrate that ExoLR dramati-
cally improves on-target efficiency, with 89% of reads mapping to exons compared
to 26% for LR. This resulted in more than double the final on-target reads and over
three times the read support for high-confidence, full-length isoforms. While ExoLR
successfully captured isoforms in key ALS genes, we also identified significant biases.
Given the specificity of the exome probes for protein-coding exons, the capture of
non-coding RNAs was predictably low. Furthermore, we observed an unexpected
capture bias against longer genes. Our findings validate exome enrichment as a
highly effective strategy to enhance isoform discovery in challenging tissues but
underscore the need to consider its inherent biases when designing future studies.

## Analysis Pipeline & Repository Contents

The analysis is organized into several R Markdown (`.Rmd`) scripts that perform distinct steps of the workflow.

1.  **`iso_seq.Rmd`**
    *   Full Iso-Seq workflow

2.  **`FLAIR.Rmd`**
    *   Isoform calling with FLAIR2 and SQANTI3 QC

3.  **`count_matrix.Rmd`**
    *   Making single-cell count matrix

4.  **`counts.Rmd`**
    *   Differential expression analysis with DESeq2

5.  **`consensus.Rmd`**
    *   Variant calling with Deepvariant
