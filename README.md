# GENOMAC-Brain-Cancer-Variant-Analysis
Brain cancer whole genome variant analysis using Galaxy, Python, and functional enrichment.

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
