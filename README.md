# single-cell-pbmc-representation

This project demonstrates a full single-cell RNA sequencing (scRNA-seq) analysis workflow using Peripheral Blood Mononuclear Cells (PBMC) data. It was designed as a reproducible, well-documented analysis to showcase technical competency in single-cell analysis tools and data interpretation for a prospective PhD application.

---

## 🧪 Project Overview

* **Dataset**: 10X PBMC 3k dataset (publicly available from [10x Genomics](https://www.10xgenomics.com/))
* **Goal**: Identify major immune cell populations in PBMCs using unsupervised clustering and marker gene expression.
* **Tools**: Python, Scanpy, UMAP, Leiden clustering, Matplotlib, Seaborn

---

## 📊 Analysis Workflow

1. **Data Loading**

   * Downloaded and loaded filtered gene-barcode matrix into an `AnnData` object.

2. **Quality Control (QC)**

   * Calculated total counts, number of genes per cell, and mitochondrial gene percentages.
   * Visualized QC metrics using violin plots.
   * Filtered low-quality cells.

3. **Normalization and Feature Selection**

   * Normalized expression counts per cell.
   * Identified highly variable genes.

4. **Dimensionality Reduction**

   * Performed PCA for initial structure.
   * Constructed k-nearest neighbors graph.
   * Computed UMAP embedding.

5. **Clustering**

   * Applied Leiden clustering with resolution = 0.5 to identify cell populations.

6. **Marker Gene Discovery**

   * Ranked differentially expressed genes for each cluster using `rank_genes_groups()`.
   * Visualized top markers per cluster.

7. **Manual Cell Type Annotation**

   * Annotated clusters using canonical immune markers (e.g., CD3D, CD14, NKG7).
   * Generated final labeled UMAP plot.

---

## 🖼️ Outputs

All plots are saved in the `/outputs/` folder and include:

* Violin plots of QC metrics
* UMAP with Leiden clusters
* Marker gene rankings
* UMAP annotated by cell type

---

## 📁 Repository Structure

```
├── data/                    # Automatically downloaded PBMC data
├── notebooks/              # Main analysis notebook (.ipynb)
├── outputs/                # Generated plots
├── README.md               # Project documentation
├── requirements.txt        # Environment dependencies
```

---

## 📦 Dependencies

Install Python packages using the provided `requirements.txt`:

```bash
pip install -r requirements.txt
```

---

## 🧠 Key Skills Demonstrated

* Handling AnnData and single-cell matrices
* QC and filtering in scRNA-seq data
* Dimensionality reduction and clustering
* Marker gene discovery and interpretation
* Plotting and saving outputs programmatically
* Reproducible project structure and GitHub usage

---

## 📬 Contact

**Sofiia Eremchuk**
Contact: [sofiia.eremchuk@gmail.com](mailto:sofiia.eremchuk@gmail.com)
Project repo: [GitHub/single-cell-pbmc-representation](https://github.com/sofiiaeremchuk-collab/single-cell-pbmc-representation)

---

> For project walkthrough or questions, feel free to reach out!
