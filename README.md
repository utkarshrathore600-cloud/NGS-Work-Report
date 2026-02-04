# NGS-Work-Report
This repository contains a detailed report on RNA-Seq data analysis using Next Generation Sequencing (NGS). It covers the complete workflow including quality control, read trimming, alignment, read counting, differential gene expression analysis, and pathway visualization using standard bioinformatics tools on the Galaxy platform.
# NGS WORKSHOP REPORT

## RNA-Seq Data Analysis Workflow Using Next Generation Sequencing (NGS)

---

## Aim
The aim of this workshop was to understand and perform a complete RNA-Seq data analysis workflow using Next Generation Sequencing (NGS),
starting from raw sequencing data to final biological interpretation.

---

## Introduction
Next Generation Sequencing (NGS) is a powerful technology that enables high-throughput sequencing of nucleic acids. RNA sequencing (RNA-Seq) is one of the most widely used NGS applications for studying gene expression by sequencing complementary DNA (cDNA) generated from RNA samples.

This workshop focused on providing hands-on training in RNA-Seq data analysis using standard bioinformatics tools. The objective was to understand how raw sequencing data is processed, analyzed, and interpreted using a systematic workflow.

---

## Dataset Description
- Data Type: RNA-Seq  
- File Format: FASTQ  
- Organism: *Mus musculus* (Mouse)  
- Data Source: Zenodo repository  
- Dataset Link: https://zenodo.org/records/4249555  
- Samples: Control and treated samples
![Zenodo Dataset](images/zenododataset.png)

The RNA-Seq dataset used in this analysis was obtained from the Zenodo repository. The dataset consists of raw FASTQ files generated from mouse RNA-Seq experiments and was used throughout the workshop for practical analysis.

---

## Workflow Methodology

### Step 1: Quality Control using FASTQC
FASTQC was used to evaluate the quality of raw RNA-Seq reads. Parameters such as per-base sequence quality, GC content, sequence length distribution, and adapter contamination were examined to assess the overall quality of the data.

![FASTQC Result](images/fastqcresult.png)

---

### Step 2: Read Trimming using Trim Galore
Trim Galore was employed to remove adapter sequences and trim low-quality bases from the raw reads. This step helped improve the quality of reads for downstream analysis.

![Trim Galore Result](images/trimgaloreresult.png)

---

### Step 3: Read Alignment using Bowtie2
The trimmed reads were aligned to the reference mouse genome using Bowtie2. The alignment generated SAM/BAM files, and mapping statistics were evaluated to determine alignment efficiency.

![Bowtie2 Alignment](images/bowtiealignment.png)

---

### Step 4: Read Counting using FeatureCounts
FeatureCounts was used to assign aligned reads to specific genes. A gene count matrix was generated and used as input for differential gene expression analysis.

![FeatureCounts Output](images/featurecountresult.png)

---

### Step 5: Differential Gene Expression Analysis using DESeq2
DESeq2 was used to normalize gene count data and compare gene expression levels between control and treated samples. Differentially expressed genes were identified based on statistical significance.

![DESeq Result 1](images/deseqresult1.png)
![DESeq Result 2](images/deseqresult2.png)
![DESeq Result 3](images/deseqresult3.png)

---


### Step 6: Heatmap Visualization
Heatmaps were generated to visualize expression patterns of significantly differentially expressed genes across different samples.

![Heatmap](images/expressionheatmap.png)

---

### Step 7: KEGG Pathway Analysis
KEGG pathway analysis was performed to understand the biological pathways associated with the differentially expressed genes and to interpret their functional significance.

![KEGG Pathway](images/keggpathway.png)

---

## Results and Observations
- High-quality reads were obtained after trimming  
- A large proportion of reads aligned successfully to the reference genome  
- Several genes showed significant up-regulation and down-regulation  
- Heatmaps clearly differentiated control and treated samples  
- KEGG pathway analysis revealed biologically relevant pathways  

---

## Conclusion
The NGS workshop provided comprehensive practical exposure to RNA-Seq data analysis. The step-by-step workflow demonstrated how raw sequencing data obtained from Zenodo can be processed into biologically meaningful results using standard bioinformatics tools. This analysis is essential for understanding transcriptomic data in modern biological research.

---

## Learning Outcomes
- Understanding of NGS and RNA-Seq principles  
- Hands-on experience with RNA-Seq data analysis tools  
- Ability to analyze and interpret differential gene expression results  
- Familiarity with Galaxy-based NGS workflows

---


## References
- FASTQC Documentation  
- Trim Galore User Guide  
- Bowtie2 Manual  
- DESeq2 Bioconductor Documentation  
- Galaxy Platform Documentation  
- Zenodo Repository: Raw mouse mammary RNA-Seq data (FASTQ) – https://zenodo.org/records/4249555
