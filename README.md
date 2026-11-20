# PBMC 3k scRNA-seq Analysis

A practical single-cell RNA-seq analysis workflow using **Scanpy** and the PBMC 3k dataset.

## Project structure

```text
pbmc3k-scRNA-seq-analysis/
├── README.md
├── .gitignore
└── notebooks/
    ├── 01_scRNA_seq_QC_and_Preprocessing.ipynb
    └── 02_scRNA_seq_Clustering_and_Cell_Type_Annotation.ipynb
```

## Notebooks

1. **01_scRNA_seq_QC_and_Preprocessing.ipynb** — loads the PBMC 3k dataset, explores quality-control metrics, filters cells and genes, preserves raw counts, normalizes and log-transforms expression values, and identifies highly variable genes.
2. **02_scRNA_seq_Clustering_and_Cell_Type_Annotation.ipynb** — scales highly variable genes, performs PCA, constructs the neighborhood graph, applies Leiden clustering, visualizes cells with UMAP, identifies cluster marker genes and compares known immune-cell markers to support cell-type annotation.
3. **Differential expression analysis** — planned as a separate notebook after that stage of the analysis is completed. It is not included yet.

## How to run in Google Colab

Run the notebooks in order:

1. Open Notebook 1 in Google Colab and run its cells from top to bottom. The notebook saves `pbmc3k_preprocessed.h5ad` and downloads it to your computer.
2. Open Notebook 2 in Google Colab. When prompted, upload the `pbmc3k_preprocessed.h5ad` file downloaded from Notebook 1.
3. Continue the analysis in Notebook 2.

The intermediate `.h5ad` file is transferred between notebooks rather than committed to this repository.

## Dataset

The workflow uses Scanpy's built-in PBMC 3k dataset (`scanpy.datasets.pbmc3k`). The dataset contains peripheral blood mononuclear cells from a healthy donor and is commonly used for learning and demonstrating single-cell RNA-seq analysis.

## Main tools

- Python
- Scanpy
- AnnData
- NumPy
- Pandas
- Matplotlib
- Leiden clustering

## Notes

- This is an exploratory analysis of the PBMC 3k dataset. Cluster labels are provisional until they are checked against marker expression and relevant biological evidence.
- The PBMC 3k dataset represents a single sample. Cluster-wise marker ranking is useful for exploration, but it should not be interpreted as donor-aware differential expression between biological conditions.
- The notebooks are organized as a learning workflow. Further analyses, including differential expression, will be added as they are completed.
