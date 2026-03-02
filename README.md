# QuickSRT: Quick Access to Spatially Resolved Transcriptomics (SRT) Datasets

## SRT Studies:

- `BC_HER2+_ST`: Human Epidermal Growth Factor Receptor 2-Positive Breast Cancer
- `BC_HP_10x`: Cellular Plasticity in Human Breast Cancer Subtypes
- `BC_NP_10x`: Human Breast Cancers
- `BC_TNBC_ST`: Triple Negative Breast Cancers
- `CRC_CMS_10x`: Colorectal Cancer Consensus Molecular Subtypes
- `DLPFC_10x`: Dorsolateral Prefrontal Cortex 
- `KLC_TLS_10x`: Kidney (`KC_TLS_10x`) and Lung (`LC_TLS_10x`) Cancer with Tertiary Lymphoid Structures
- `MOB_ST`: Mouse Olfactory Bulb  
- `RCC_TLS_10x`: Tertiary Lymphoid Structure      

---

## SRT Files:

Each study's samples have the following files:

- `data/SCE_sampleID.h5ad` (HDF5 AnnData):
  - `sce`: SingleCellExperiment (R) | `adata`: AnnData (Python)
    - `assay(sce, "counts")` | `adata.X`: Gene-by-spot count matrix  
    - `reducedDims(sce)$S` | `adata.obsm['S']`: Spatial coordinate matrix
    - `colData(sce)$z` | `adata.obs['z']`: Annotations

- `images/HE_sampleID.jpg` or `.png`:  
  - Hematoxylin and Eosin (H&E)-stained histological image
