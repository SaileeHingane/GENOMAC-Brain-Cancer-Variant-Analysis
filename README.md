# GENOMAC-Brain-Cancer-Variant-Analysis 
Brain cancer whole genome variant analysis using Galaxy, Python, and functional enrichment.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Galaxy Europe](https://img.shields.io/badge/Galaxy-Europe-orange)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626)
![WGS](https://img.shields.io/badge/NGS-WGS-success)

# GENOMAC Brain Cancer Variant Analysis

## Project Overview

This repository presents a bioinformatics workflow developed during my GENOMAC genomics internship to analyse publicly available human brain cancer whole-genome sequencing (WGS) datasets. The project demonstrates an end-to-end variant analysis pipeline, beginning with raw sequencing data acquisition and continuing through quality assessment, alignment, variant calling, variant annotation, downstream filtering, gene frequency analysis, and functional enrichment.

The workflow combines Galaxy Europe for primary NGS data processing with Python-based downstream analysis in Jupyter Notebook. Functional enrichment analysis was performed using g:Profiler to identify biological pathways and Gene Ontology (GO) terms associated with the filtered variants. This repository focuses on demonstrating a reproducible bioinformatics workflow using publicly available genomic datasets.

---

## Objectives

The objectives of this project were to:

- Demonstrate an end-to-end whole-genome sequencing (WGS) variant analysis workflow.
- Process publicly available brain cancer sequencing datasets using Galaxy Europe.
- Identify high and moderate impact genetic variants.
- Perform downstream filtering and gene frequency analysis using Python.
- Explore enriched biological pathways and Gene Ontology terms using g:Profiler.
- Demonstrate reproducible bioinformatics analysis using open-source tools and publicly available datasets.

---

## Dataset

This project analysed **10 publicly available human brain cancer whole-genome sequencing (WGS) datasets** obtained from the NCBI Sequence Read Archive (SRA). The selected datasets originated from multiple BioProjects and were generated using different Illumina sequencing platforms, providing a diverse pilot dataset for demonstrating variant analysis workflows.

The sample metadata, including BioProject accessions, SRA identifiers, sequencing platforms, and dataset information, is available in the **figures** folder.

```

### Dataset Summary

- Source: NCBI Sequence Read Archive (SRA)
- Number of samples: 10
- Data type: Human paired-end Whole Genome Sequencing (WGS)
- Disease focus: Brain cancer
- Multiple BioProjects
- Multiple sequencing platforms (Illumina NextSeq 550 and NovaSeq 6000)

---

## Bioinformatics Workflow

### Stage 1 — Data Acquisition (Galaxy Europe)

- Retrieval of publicly available WGS datasets from NCBI SRA.

### Stage 2 — Quality Assessment

- Quality assessment of raw FASTQ files using FastQC.
- Quality review before downstream processing.

### Stage 3 — Read Pre-processing

- Adapter trimming and quality filtering where required.

### Stage 4 — Read Alignment

- Alignment of sequencing reads to the human reference genome (GRCh38).

### Stage 5 — Variant Calling

- Detection of genomic variants from aligned sequencing data.

### Stage 6 — Variant Annotation

- Functional annotation of detected variants.
- Selection of high and moderate impact variants for downstream analysis.

### Stage 7 — Downstream Analysis (Python)

- Import annotated variant files.
- Filter variants.
- Merge results across samples.
- Generate gene frequency summaries.
- Extract gene lists for enrichment analysis.

### Stage 8 — Functional Enrichment

- Gene Ontology (GO) enrichment analysis.
- Pathway enrichment using g:Profiler.
- Visualisation of enriched biological pathways.

---

# Tools & Technologies

### Primary Analysis Platform
- Galaxy Europe

### Programming & Data Analysis
- Python
- Jupyter Notebook
- pandas
- matplotlib

### Functional Enrichment
- g:Profiler (g:GOSt)

---

# Repository Structure

```
GENOMAC-Brain-Cancer-Variant-Analysis/
│
├── workflow/
│   └── Workflow documentation
│
├── notebooks/
│   ├── Brain_Cancer_Variant_Analysis.ipynb
│   └── Notebook documentation
│
├── results/
│   ├── Gene summary tables
│   ├── Gene lists
│   └── g:Profiler enrichment results
│
├── figures/
│   ├── Sample metadata
│   ├── g:Profiler Manhattan plot
│   └── Top enriched pathways
│
└── README.md
```

---

# Key Results

- Analysed 10 publicly available human brain cancer whole-genome sequencing (WGS) datasets.
- Identified high and moderate impact genetic variants following annotation.
- Generated consolidated gene summaries from all analysed samples.
- Performed gene frequency analysis to identify recurrently observed genes.
- Conducted Gene Ontology (GO) and pathway enrichment analysis using g:Profiler.
- Visualised enriched biological pathways and functional categories using Python.

> **Note:** This repository demonstrates a bioinformatics workflow using publicly available datasets. The enrichment results presented here are intended for educational and workflow demonstration purposes and should be interpreted as hypothesis-generating observations requiring further biological validation.

---

# Figures

Representative figures included in this repository:

- Brain cancer WGS sample metadata
- g:Profiler Manhattan plot
- Top enriched pathways

---

# Skills Demonstrated

## Bioinformatics

- Whole-genome sequencing (WGS) analysis
- Variant calling workflow
- Variant annotation
- Functional enrichment analysis
- Gene Ontology (GO) analysis

## Computational

- Galaxy Europe
- Python programming
- Data preprocessing
- Data integration
- Data visualization
- Reproducible workflow documentation

## Biological Interpretation

- Variant filtering
- Gene frequency analysis
- Functional pathway interpretation
- Biological data summarisation

---

# References & Acknowledgements

This project was developed using publicly available datasets and open-source bioinformatics resources.

The following platforms and tools were used throughout the analysis:

- National Center for Biotechnology Information (NCBI) Sequence Read Archive (SRA) (https://www.ncbi.nlm.nih.gov/sra) 
- Galaxy Europe (https://usegalaxy.eu/user)
- g:Profiler (g:GOSt) (https://biit.cs.ut.ee/gprofiler/gost)

Special thanks to the developers and maintainers of these open-source resources for making reproducible bioinformatics research accessible.

---

## License

This repository is intended for educational and portfolio purposes.

Public sequencing datasets remain the property of their original submitters and the NCBI Sequence Read Archive.
