# QuickSRT: Quick Access to Spatially Resolved Transcriptomics (SRT) Datasets

## SRT Studies:

- `14204217[BC_TNBC_ST]` – Triple Negative Breast Cancers
- `14620362[KC_TLS_10x | LC_TLS_10x]` – Kidney and Lung Cancer with Tertiary Lymphoid Structures
- `4739739[BC_NP_10x]`: Human Breast Cancers
- `7760264[CRC_CMS_10x]` – Colorectal Cancer Consensus Molecular Subtypes 
- `DLPFC[DLPFC_10x]`: Dorsolateral Prefrontal Cortex  
- `GSE175540[RCC_TLS_10x]`: Tertiary Lymphoid Structure  
- `GSE193460`: Mouse Model of Lung Adenocarcinoma  
- `GSE213688[BC_HP_10x]`: Cellular Plasticity in Human Breast Cancer Subtypes  
- `HER2-Positive[BC_HER2+_ST]`: Human Epidermal Growth Factor Receptor 2-Positive Breast Cancer  
- `MOB[MOB_ST]`: Mouse Olfactory Bulb  

---

## SRT Data Structure:

Each study's samples have the following files:

- `data/SCE_sampleID.h5ad` (HDF5 AnnData):
  - `sce`: SingleCellExperiment (R) / `adata`: AnnData (Python)
    - `assay(sce, "counts")` / `adata.X`: Gene-by-spot count matrix  
      - Batch-corrected count matrix for study `14204217`
    - `reducedDims(sce)$S` / `adata.obsm['S']`: Spatial coordinate matrix
    - `colData(sce)$z` / `adata.obs['z']`: Annotations

- `images/HE_sampleID.jpg` or `.png`:  
  - Hematoxylin and Eosin (H&E)-stained histological image
