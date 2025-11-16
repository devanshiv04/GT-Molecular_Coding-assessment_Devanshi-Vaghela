# GT-Molecular_Coding-assessment_Devanshi-Vaghela
TP53 ctDNA Variant Calling and Interpretation Pipeline

This repository contains a reproducible pipeline for analyzing circulating tumor DNA (ctDNA) focused on TP53 mutations. It includes quality control, alignment, variant calling, filtering, and clinical interpretation using open-source tools like BCFtools and Samtools. The project was developed and executed in Google Colab, with all relevant data and scripts organized for portability and reuse.

## 📚 Data Source
The raw sequencing data and reference materials used in this project were obtained from publicly available resources associated with published research. 
Citation: Lim, Y., Kim, S., Kang, JK. et al. Circulating tumor DNA sequencing in colorectal cancer patients treated with first-line chemotherapy with anti-EGFR. Sci Rep 11, 16333 (2021). https://doi.org/10.1038/s41598-021-95345-4

All data were used strictly for educational and non-commercial purposes to demonstrate variant calling and clinical interpretation workflows. No patient-identifiable information is included, and raw FASTQ files have been excluded from this repository to respect data size and privacy constraints.

## 🧪 Pipeline Overview
1. **Quality Control**  
   - FastQC and MultiQC for raw FASTQ files

2. **Alignment**  
   - BWA-MEM alignment to TP53 reference genome  
   - Samtools for sorting and indexing

3. **Variant Calling**  
   - BCFtools mpileup and call  
   - Filtering with `QUAL > 20` and `DP > 10`

4. **Interpretation**  
   - VCF parsing and annotation  
   - Variant Allele Frequency (VAF) calculation  
   - Cross-referencing with TP53 hotspots from ClinVar and COSMIC

## 🔍 Key Tools Used
- `Samtools`  
- `BCFtools`  
- `FastQC`  
- `MultiQC`  
- `Python (pandas, matplotlib)`  
- `Google Colab` for compute and storage

## 📊 Visualization Ideas
- Mutation summary dashboard with VAF and clinical annotations  
- TP53 lollipop plot showing hotspot mutations  
- Pre vs post-treatment VAF comparison  
- Timeline of mutation dynamics  
- Interactive notebook or Streamlit dashboard

## 🧠 Interpretation Goals
- Identify clinically relevant TP53 mutations  
- Track clonal evolution across treatment  
- Support translational insights for precision oncology

