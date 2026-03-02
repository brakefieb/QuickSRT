# QuickSRT: Quick Access to Spatially Resolved Transcriptomics (SRT) Datasets

## SRT Studies:

- `BC_10x`: Human Breast Cancers
- `BC_HER2+_ST`: Human Epidermal Growth Factor Receptor 2-Positive Breast Cancer
- `BC_HP_10x`: High-Plasticity Breast Cancer Subtypes
- `BC_TNBC_ST`: Triple-Negative Breast Cancer
- `CRC_CMS_10x`: Colorectal Cancer Consensus Molecular Subtypes
- `DLPFC_10x`: Human Dorsolateral Prefrontal Cortex
- `KLC_TLS_10x`: Tertiary Lymphoid Structures in Kidney (`KC_TLS_10x`) and Lung (`LC_TLS_10x`) Cancer
- `MOB_ST`: Mouse Olfactory Bulb
- `RCC_TLS_10x`: Tertiary Lymphoid Structures in Renal Cell Cancer     

---

## SRT Files:

Each study's samples have the following files:

- `data/SCE_sampleID.h5ad` (HDF5 AnnData):
  - `sce`: SingleCellExperiment (R) | `adata`: AnnData (Python)
    - `assay(sce, "counts")` | `adata.X`: Gene-by-spot count matrix  
    - `reducedDims(sce)$S` | `adata.obsm['S']`: Spot coordinate matrix
    - `colData(sce)$z` | `adata.obs['z']`: Spot pathologist annotations

- `images/HE_sampleID.jpg` or `.png`:  
  - Hematoxylin and Eosin (H&E)-stained histological image
