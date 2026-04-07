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

  - Python
    ```python
    # Install package
    pip install anndata

    # Load package
    from anndata import read_h5ad

    # Load AnnData
    adata = read_h5ad("data/SCE_sampleID.h5ad")

    # Gene-by-spot count matrix
    adata.X
    
    # Spot coordinate matrix
    adata.obsm['S']
    
    # Spot pathologist annotations
    adata.obs['z']
    ```
      
  - R
    ```R
    # Install packages
    if (!require("BiocManager", quietly = TRUE)) install.packages("BiocManager")
    BiocManager::install(c("zellkonverter", "SingleCellExperiment"))

    # Load packages
    library(zellkonverter)
    library(SingleCellExperiment)

    # Load SingleCellExperiment
    sce <- readH5AD("data/SCE_sampleID.h5ad")

    # Gene-by-spot count matrix
    assay(sce, "counts")
    
    # Spot coordinate matrix
    reducedDims(sce)$S

    # Spot pathologist annotations
    colData(sce)$z
    ```

- `images/HE_sampleID.jpg` or `.png`:  
  - Hematoxylin and Eosin (H&E)-stained histological image
