# METI VISIUM BLCA

**Author:** Dr. Parul Kulshreshtha  
**Date:** July 2026

## Overview

This repository reproduces the spatial transcriptomics workflow described in the METI framework using publicly available 10x Genomics Visium bladder cancer datasets.

The notebook demonstrates an end-to-end workflow, beginning with downloading raw data directly from the Gene Expression Omnibus (GEO), followed by preprocessing, quality control, spatial transcriptomic analysis, and visualization of spatial gene expression patterns on matched H&E tissue sections.

---

## Reference

Yang Y. *et al.*

**METI: Deep profiling of tumor ecosystems by integrating cell morphology and spatial transcriptomics.**

*Nature Communications* (2025).

---

## Data

Public datasets were obtained from the Gene Expression Omnibus (GEO).

**Series accession**

- **GSE268112**

**Samples**

- GSM7853987 — BLCA-B1
- GSM7853988 — BLCA-B2

Platform:

- 10x Genomics Visium Spatial Gene Expression

---

## Workflow

The notebook performs the following analyses:

1. Downloading Visium datasets directly from GEO.
2. Loading count matrices, metadata and H&E images.
3. Quality control and normalization.
4. Preparing AnnData objects for spatial analysis.
5. Detecting tissue contours using TESLA.
6. Generating tissue masks.
7. Preparing TESLA-compatible input.
8. Running TESLA spatial enhancement.
9. Validating the enhanced expression matrix.
10. Generating publication-style spatial expression maps.

---

## Marker panels

### Neutrophil (paper-defined)

- HMGB2
- IFIT1
- ISG15
- LCN2
- MX1
- S100A8
- S100A9
- SYAP1

### Negative control

B-cell markers

- CD19
- MS4A1

### Positive control

Urothelial marker

- KRT20
- UPK1A
- UPK2
- UPK3A
- KRT20
- GATA3

---

## Results

The notebook successfully reproduces:

- preprocessing of Visium bladder cancer datasets
- H&E image integration
- TESLA spatial enhancement
- neutrophil spatial meta-gene visualization
- publication-style Visium expression maps for both BLCA-B1 and BLCA-B2

Additional validation is provided using:

- positive control (KRT20)
- negative control (B-cell markers)

---

## Software

- Python 3.9
- Scanpy
- AnnData
- TESLA 1.2.2
- METI
- NumPy
- Matplotlib
- OpenCV
- Pillow

---

## Reproducibility

All analyses were independently reproduced using publicly available data without access to proprietary datasets. The workflow is fully reproducible from the original GEO submissions.
