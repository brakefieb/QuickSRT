# QuickSRT: Quick Access to Spatially Resolved Transcriptomics (SRT) Datasets

## SRT Studies:

- `14204217` – Triple Negative Breast Cancers
- `14620362` – Kidney and Lung Cancer with Tertiary Lymphoid Structures
- `4739739`: Human Breast Cancers
- `7760264` – Colorectal Cancer Consensus Molecular Subtypes 
- `DLPFC`: Dorsolateral Prefrontal Cortex  
- `GSE175540`: Tertiary Lymphoid Structure  
- `GSE193460`: Mouse Model of Lung Adenocarcinoma  
- `GSE213688`: Cellular Plasticity in Human Breast Cancer Subtypes  
- `HER2-Positive`: Human Epidermal Growth Factor Receptor 2-Positive Breast Cancer  
- `MOB`: Mouse Olfactory Bulb  

---

## SRT Data Structure:

Each study's samples have the following files:

- `data/SCE_sampleID.h5ad` (HDF5 AnnData):
  - `sce`: SingleCellExperiment
    - `assay(sce, "counts")`: Gene-x-spot count matrix  
      - Batch-corrected count matrix for study `14204217`
    - `reducedDims(sce)$S`: Spatial coordinate matrix
    - `colData(sce)$z`: Annotations

- `images/HE_sampleID.jpg` or `.png`:  
  - Hematoxylin and Eosin (H&E)-stained histological image
