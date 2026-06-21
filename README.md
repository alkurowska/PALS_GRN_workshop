# PALS Summer School Workshop

## Integration of Epigenomics to Infer Gene Regulatory Networks

**Instructor:** Aleksandra Kurowska

---

# Workshop Overview

This workshop introduces a complete computational workflow for reconstructing gene regulatory networks (GRNs) from paired bulk RNA-seq and ATAC-seq datasets. Participants will learn how to integrate chromatin accessibility, gene expression, histone modifications, transcription factor binding information, and footprinting results to identify candidate regulatory interactions and build cell-type-specific GRNs.

The workflow follows the analytical framework developed for the reconstruction of regulatory programs during human B-cell differentiation and can be readily adapted to other biological systems.

---

# Study Background

The analytical workflow presented here follows the strategy described in:

Planell N. et al. *Uncovering the regulatory landscape of early human B cell lymphopoiesis and its implications in the pathogenesis of B-ALL*. Science Advances. 2025;11:eadw3110.

---

# Learning Objectives

By the end of the workshop participants will be able to:

* Perform differential chromatin accessibility analysis.
* Perform differential gene expression analysis.
* Integrate ATAC-seq and RNA-seq datasets.
* Identify candidate cis-regulatory elements (CREs).
* Validate CREs using public histone mark datasets.
* Link promoters and enhancers to target genes.
* Incorporate transcription factor footprinting information.
* Build TF–OCR–gene regulatory networks.
* Generate cell-type-specific GRNs.
---

# Required Software

## R Packages

```r
tidyverse
limma
GenomicRanges
rtracklayer
reshape2
igraph
ggplot2
chromVAR
motifmatchr
JASPAR2022
BSgenome.Hsapiens.UCSC.hg38
```

## Additional Tools

The workshop uses precomputed footprint datasets.

The original footprinting analysis was performed using:

```bash
HINT-ATAC
Wellington
```

These analyses require substantial computational resources and were originally executed on an HPC cluster. Therefore, participants will use pre-generated footprint BED files during the workshop rather than running footprinting themselves.

---

# Workshop Structure

The workshop follows the biological flow of regulatory information:

```text
Chromatin accessibility (ATAC-seq)
            ↓
Differential OCRs
            ↓
Gene expression (RNA-seq)
            ↓
Differentially expressed genes
            ↓
Histone-supported regulatory elements
            ↓
Promoter OCR–gene links
            ↓
Enhancer OCR–gene links
            ↓
Candidate cis-regulatory elements
            ↓
Footprint-supported TF assignment
            ↓
TF–OCR–gene interactions
            ↓
Cell-type-specific GRNs
            ↓
Network topology analysis
            ↓
Master regulator discovery
```
---
