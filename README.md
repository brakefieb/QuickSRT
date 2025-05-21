# QuickSRT: Quick Access to Spatially Resolved Transcriptomics (SRT) Datasets

## SRT Studies:

- `DLPFC`: Dorsolateral Prefrontal Cortex
- `HER2-Positive`: Human Epidermal Growth Factor Receptor 2-Positive Breast Cancer
- `MOB`: Mouse Olfactory Bulb

---

## SRT Data Structure:

Each study's samples have the following files:

- `data/SCE_sampleID.h5ad` (HDF5 AnnData):
  - `sce`: SingleCellExperiment
    - `assay(sce, "counts")`: Gene-x-spot count matrix
    - `reducedDims(sce)$S`: Spatial coordinate matrix
    - `colData(sce)$z`: Annotations 

- `images/HE_sampleID.jpg` or `.png`:  
  - Hematoxylin and Eosin (H&E)-stained histological image
