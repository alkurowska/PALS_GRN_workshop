# PALS Summer School Workshop

## Integration of Epigenomics to Infer Gene Regulatory Networks

**Instructor:** Aleksandra Kurowska

---

# Workshop Overview

This workshop introduces a complete computational workflow for reconstructing gene regulatory networks (GRNs) from paired bulk RNA-seq and ATAC-seq datasets. Participants will learn how to integrate chromatin accessibility, gene expression, histone modifications, transcription factor binding information, and footprinting results to identify candidate regulatory interactions and build cell-type-specific GRNs.

The workflow follows the analytical framework developed for the reconstruction of regulatory programs during human B-cell differentiation and can be readily adapted to other biological systems.

To ensure that all participants can complete the workflow within the workshop timeframe, computationally intensive analyses such as transcription factor footprinting are provided as precomputed results. The workshop focuses on the biological interpretation and integration of these data layers to reconstruct regulatory networks.

---

# Study Background

The analytical workflow presented here follows the strategy described in:

Planell N. et al. *Uncovering the regulatory landscape of early human B cell lymphopoiesis and its implications in the pathogenesis of B-ALL*. Science Advances. 2025;11:eadw3110.

The workshop provides a simplified but biologically faithful implementation of the original pipeline and illustrates how multiple layers of epigenomic and transcriptomic information can be integrated to identify candidate cis-regulatory elements, infer transcription factor activity, and reconstruct cell-type-specific gene regulatory networks.

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
* Analyze GRN topology using graph theory approaches.

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
ComplexHeatmap
circlize
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

# References

Núria Planell et al., Uncovering the regulatory landscape of early human B cell lymphopoiesis and its implications in the pathogenesis of B-ALL. Sci. Adv. 11, eadw3110 (2025). doi:10.1126/sciadv.adw3110
