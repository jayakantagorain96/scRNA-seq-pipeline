# Transcriptomics Workflows:

* 1. Bulk RNA seq/ Total RNA/ mRNA Sequencing
* 2. Single-Cell RNA Sequencing

## 1. Bulk RNA seq
### Average expression of each gene across a population of cells. It helps to identify differentially expressed genes(DEGs), gene regulation, and pathways involved in it.

## Industrial Workflow

### Wet-Lab Steps

* Sample collection & RNA extraction
* Total RNA is extracted from tissue or cell samples.
* RNA quality is checked using Bioanalyzer or TapeStation (RIN > 6.5) and spectrophotometer (A260/280 ratio).
* mRNA or total RNA library preparation
-If studying mRNA, poly-A selection is used to capture messenger RNAs.
-If studying total RNA, rRNA depletion is performed (to remove ribosomal RNA).
* RNA is fragmented, converted to cDNA, adapter-ligated, and amplified.
* Sequencing
-Libraries are sequenced on Illumina platforms (e.g., NovaSeq, NextSeq) to generate 150 bp paired-end reads.

### Bioinformatics Steps

* Quality control: FastQC, MultiQC
* Read alignment: HISAT2, STAR, or Salmon to the reference genome.
* Quantification: FeatureCounts or HTSeq for gene counts.
* DEG analysis: DESeq2 / edgeR / limma.
* Functional analysis: GO and KEGG pathway enrichment.

### Applications

* Differential gene expression in disease vs control.
* Drug response profiling.
* Functional genomics and biomarker discovery.

## 2. Single-Cell RNA Sequencing
### Comparison of the transcriptomes of individual cells.It helps to identify gene expression cell by cell, heterogenity, microenvironment interactions.

### Industrial Workflow
### Wet-Lab Steps

* Cell suspension preparation
* Single viable cells are isolated from tissue (using dissociation and FACS sorting).
* Single-cell capture & barcoding
-Industry-standard systems: 10x Genomics Chromium, BD Rhapsody, or Smart-seq2.
* Each cell’s mRNAs are captured and tagged with a unique cell barcode and UMI (Unique Molecular Identifier).
* Library preparation & sequencing
-Reverse transcription → cDNA → sequencing library.
-Sequenced on Illumina platforms.

### Bioinformatics Steps

* Preprocessing: CellRanger (for 10x data) – generates gene-cell matrices.
* Quality control: Filtering low-quality cells, doublets.
* Normalization & dimensionality reduction: Using Seurat or Scanpy (PCA, UMAP).
* Clustering: To identify distinct cell populations.
* Differential expression & pathway analysis: To characterize each cluster.

### Applications

* Tumor microenvironment profiling.
* Developmental biology.
* Immune cell diversity studies.


