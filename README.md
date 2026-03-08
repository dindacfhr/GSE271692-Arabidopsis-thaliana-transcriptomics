# GSE271692 – Arabidopsis thaliana Transcriptomics Analysis 🌿

## Overview

This repository contains a bioinformatics analysis of the **GSE271692 transcriptome dataset** from the NCBI Gene Expression Omnibus (GEO). The study investigates **gene expression changes in *Arabidopsis thaliana*** under **abscisic acid (ABA) treatment** compared to control conditions using **Murashige and Skoog (MS) medium**.

The dataset includes multiple genotypes of *Arabidopsis thaliana*:

* Wild type (WT)
* **mbd1 knockout**
* **pyl5 knockout**
* **mbd1/pyl5 double knockout**

These genes are associated with **epigenetic regulation and ABA signaling**, making this dataset valuable for understanding the molecular response of plants to abiotic stress.

The analysis focuses on identifying **differentially expressed genes (DEGs)** and interpreting their biological significance using **Gene Ontology (GO) enrichment analysis**.

---

# Dataset Information

* **Dataset ID:** GSE271692
* **Database:** NCBI Gene Expression Omnibus (GEO)
* **Platform:** Affymetrix Arabidopsis ATH1 Genome Array (GPL198)
* **Organism:** *Arabidopsis thaliana*

Samples were grouped into two main treatment conditions:

| Group | Description                          | Number of Samples |
| ----- | ------------------------------------ | ----------------- |
| MS    | Murashige and Skoog medium (control) | 10                |
| ABA   | Abscisic acid treatment              | 10                |

---

# Analysis Workflow

The transcriptomics analysis was conducted using **R** and several bioinformatics packages.

The overall workflow is shown below:

```
GEO Dataset (GSE271692)
        ↓
Quality Control
(Boxplot & Density Plot)
        ↓
Dimensionality Reduction
(UMAP Clustering)
        ↓
Differential Expression Analysis
(MS vs ABA)
        ↓
Visualization
(Volcano Plot & Heatmap)
        ↓
Functional Enrichment
(Gene Ontology Analysis)
```

---

# Methods

## 1. Quality Assessment

Quality control of gene expression data was performed using:

* **Boxplot** – to evaluate distribution consistency across samples
* **Density plot** – to verify normalization and expression distribution

These plots ensure that the expression values are comparable between samples.

---

## 2. Sample Clustering

To explore the similarity between samples, **UMAP (Uniform Manifold Approximation and Projection)** was used to reduce the high-dimensional gene expression data into two dimensions.

UMAP clustering helps visualize whether samples group according to biological conditions (MS vs ABA).

---

## 3. Differential Gene Expression Analysis

Differential expression analysis was conducted to identify genes significantly regulated by ABA treatment.

Criteria used for DEG identification:

* **Adjusted p-value < 0.05**
* Log2 fold change used to determine upregulated and downregulated genes.

The results were visualized using:

* **Volcano plot**
* **Heatmap of Top 50 DEGs**

---

## 4. Functional Enrichment Analysis

To interpret the biological significance of the DEGs, **Gene Ontology (GO) enrichment analysis** was performed.

Three GO categories were analyzed:

* **Biological Process (BP)** – biological pathways and processes
* **Molecular Function (MF)** – biochemical activities of gene products
* **Cellular Component (CC)** – cellular localization of proteins

---

# Key Findings

The analysis revealed several important insights:

### 1. Transcriptome response to ABA

ABA treatment resulted in significant changes in gene expression across the transcriptome of *Arabidopsis thaliana*.

### 2. Clear clustering between conditions

UMAP analysis showed clear separation between **MS control samples** and **ABA-treated samples**, indicating strong transcriptional responses to ABA.

### 3. Differentially expressed genes

A subset of genes exhibited significant upregulation or downregulation in response to ABA treatment.

These genes likely participate in:

* Stress response pathways
* Hormone signaling
* Metabolic regulation

### 4. Enriched biological processes

GO enrichment analysis indicated that many DEGs are involved in:

* Response to water deprivation
* Response to cold and freezing
* Seed dormancy and germination
* Lipid and nutrient storage
* Oxidoreductase activity
* Membrane transport processes

These functions are strongly associated with **ABA-mediated stress adaptation mechanisms in plants**.

---

# Biological Significance

The results suggest that **ABA signaling significantly modulates gene expression networks** associated with:

* Abiotic stress responses
* Redox metabolism
* Chloroplast-related processes
* Seed development and dormancy

The interaction between **epigenetic regulation (MBD1)** and **ABA perception (PYL5)** may influence transcriptional regulation and plant adaptation to environmental stress.

---

# Tools and Packages

The analysis was performed using **R** and the following packages:

* GEOquery
* limma
* ggplot2
* pheatmap
* umap
* clusterProfiler
* org.At.tair.db
* ath1121501.db
* AnnotationDbi

---

# Repository Structure

```
GSE271692-Arabidopsis-thaliana-transcriptomics
│
├── data/
│   └── GEO dataset information
│
├── scripts/
│   └── R scripts for transcriptome analysis
│
├── figures/
│   ├── boxplot.png
│   ├── density_plot.png
│   ├── umap_plot.png
│   ├── volcano_plot.png
│   └── heatmap_top50.png
│
├── results/
│   └── DEG and enrichment results
│
└── README.md
```

---

# References

Ashburner et al. (2000). Gene Ontology: Tool for the unification of biology. *Nature Genetics*.

Conesa et al. (2016). A survey of best practices for RNA-seq data analysis. *Genome Biology*.

Cutler et al. (2010). Abscisic acid: Emergence of a core signaling network. *Annual Review of Plant Biology*.

Meinke et al. (1998). Arabidopsis thaliana: A model plant for genome analysis. *Science*.

Yoshida et al. (2014). ABA-dependent and ABA-independent signaling in response to osmotic stress in plants.

---

# Author

**Dinda Cinta Fahira**
OmicsLite – Capstone Project

Bioinformatics analysis of plant transcriptomics using GEO datasets.
