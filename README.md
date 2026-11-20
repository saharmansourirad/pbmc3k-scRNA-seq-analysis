# PBMC 3k scRNA-seq Analysis

A practical single-cell RNA-seq analysis workflow using **Scanpy** and the PBMC 3k dataset, focusing on dimensionality reduction, clustering and cell-type annotation.

## Project Structure

```text
pbmc3k-scRNA-seq-analysis/
├── README.md
├── .gitignore
└── notebooks/
    └── 02_scRNA_seq_Clustering_and_Cell_Type_Annotation.ipynb
```

## Notebook

**02_scRNA_seq_Clustering_and_Cell_Type_Annotation.ipynb**

This notebook performs downstream analysis of the preprocessed PBMC 3k dataset, including:

- Scaling highly variable genes
- Principal Component Analysis (PCA)
- Nearest-neighbor graph construction
- Leiden clustering
- UMAP visualization
- Cluster marker-gene identification
- Cell-type annotation and validation using known immune-cell markers

## Input Data and Preprocessing

This notebook uses the preprocessed AnnData object (`pbmc3k_preprocessed.h5ad`) generated in the companion preprocessing repository:

[PBMC 3k scRNA-seq Preprocessing](https://github.com/saharmansourirad/pbmc3k-scRNA-seq-preprocessing)

Before running this notebook:

1. Open the preprocessing repository.
2. Run `01_scRNA_seq_QC_and_Preprocessing.ipynb` in Google Colab.
3. Download the resulting `pbmc3k_preprocessed.h5ad` file to your computer.
4. Open this repository's analysis notebook in Google Colab.
5. Upload the preprocessed file when prompted.

The intermediate `.h5ad` file is transferred between the two notebooks and is not stored in either GitHub repository.

## Dataset

The workflow uses Scanpy's built
