# QuickSRT: Quick Access to Spatially Resolved Transcriptomics (SRT) Datasets

## SRT Studies:

- `BC_TNBC_ST` – Triple Negative Breast Cancers
- `KLC_TLS_10x` – Kidney and Lung Cancer with Tertiary Lymphoid Structures
- `BC_NP_10x`: Human Breast Cancers
- `CRC_CMS_10x` – Colorectal Cancer Consensus Molecular Subtypes 
- `DLPFC_10x`: Dorsolateral Prefrontal Cortex  
- `RCC_TLS_10x`: Tertiary Lymphoid Structure   
- `BC_HP_10x`: Cellular Plasticity in Human Breast Cancer Subtypes  
- `BC_HER2+_ST`: Human Epidermal Growth Factor Receptor 2-Positive Breast Cancer  
- `MOB_ST`: Mouse Olfactory Bulb  

---

## SRT Data Structure:

Each study's samples have the following files:

- `data/SCE_sampleID.h5ad` (HDF5 AnnData):
  - `sce`: SingleCellExperiment (R) | `adata`: AnnData (Python)
    - `assay(sce, "counts")` | `adata.X`: Gene-by-spot count matrix  
    - `reducedDims(sce)$S` | `adata.obsm['S']`: Spatial coordinate matrix
    - `colData(sce)$z` | `adata.obs['z']`: Annotations

- `images/HE_sampleID.jpg` or `.png`:  
  - Hematoxylin and Eosin (H&E)-stained histological image
