# GWAS-QC

**A User-Friendly Quality Control Platform for Genome-Wide Association Studies**

GWAS-QC is a powerful, GUI-based resource designed to aid researchers in performing quality control (QC) of genome-wide genotype data. It is specifically designed for researchers without formal bioinformatics training, providing a comprehensive set of features to effectively analyze vast amounts of genomic data without the need for command-line expertise.

# Download-GWAS--QC_v1
[![Download](https://img.shields.io/badge/Download-GWAS--QC_v1.0-blue?style=for-the-badge&logo=windows)](https://github.com/alxv/gwasqc/releases/tag/gwasqc)

To download the software, click the **Download Button** and you would be able to locate the gwasqc.exe file under asset section.
As this is an early release intended for evaluation purposes only, we kindly ask that you do not share, copy, modify, or distribute the software or any of its components. All contents remain the intellectual property of the developers at **University of Liverpool and is protected by copyright**.

## Table of Contents
* [Overview](https://www.google.com/search?q=%23overview)
* [Key Features](https://www.google.com/search?q=%23key-features)
* [Installation](https://www.google.com/search?q=%23installation)
* [Getting Started](https://www.google.com/search?q=%23getting-started)
* [File Requirements](https://www.google.com/search?q=%23file-requirements)
* [Project Setup](https://www.google.com/search?q=%23project-setup)
* [Sample QC (SQC)](https://www.google.com/search?q=%23sample-qc-sqc)
* [Variant QC (VQC)](https://www.google.com/search?q=%23variant-qc-vqc)
* [Data Export](https://www.google.com/search?q=%23data-export)
* [Authors](https://www.google.com/search?q=%23authors)

## Overview

GWAS-QC stands for **Genome-Wide Association Studies - Quality Control**. It streamlines the bioinformatic pipeline into an intuitive graphical user interface (GUI), allowing users to visualize data, identify outliers, and clean datasets efficiently.

## Key Features

The software performs a wide range of essential QC checks:

**Gender Check:** Verifies the reported gender of each individual against their genetic data.

**Sample Call Rate:** Calculates the proportion of successfully genotyped variants per individual.

**Heterozygosity:** Identifies individuals with unusually high or low heterozygosity rates.

**Cryptic Relatedness:** Estimates the probability of genetic relatedness between pairs of individuals.

**Ethnicity Inference:** Infers the genetic ancestry of each individual.

**Sample Outlier Removal:** Removes samples that deviate from the rest of the dataset based on genetic characteristics.

**SNP Missingness:** Calculates the proportion of individuals with missing genotype information for a given variant.

**Minor Allele Frequency (MAF):** Calculates the frequency of the less common allele for each SNP.

**Hardy-Weinberg Equilibrium (HWE):** Checks for deviation of observed allele and genotype frequencies from expected values.

**Differential Missingness:** Checks for differences in missing genotype information between cases and controls.

## Installation
**Compatibility:** Windows (PC/Laptop) or Mac (Virtual Machine).
**Important:** Do **NOT** install on network drives.
1. Download the `GWASQC` software.
2. Double-click the `gwasqc.exe` file to begin installation.
3. Follow the on-screen instructions. A user manual is available for detailed steps.

## Getting Started

### File Requirements
**Input Format:** The software strictly accepts genotype data in binary PLINK format: `.bed`, `.bim`, and `.fam` files.
**Converter Tool:** A built-in "Converter" function is available to convert `MAP/PED` or `VCF` files into binary PLINK format.
**Dummy Data:** A dummy dataset (`dummy.bed`, `dummy.bim`, etc.) is provided to help users explore the application features.

### Project Setup

1. Launch the application via the desktop icon.
2. Navigate to the **Project setup** tab.
3. Enter a project name.
*Note:* Must be alphanumeric only (no special characters or whitespace) and preferably fewer than 5 characters.
4. Click **"Assign name"** and proceed to the **"Analysis"** tab when prompted.

## Sample QC (SQC)

The Sample QC workflow consists of several sequential steps handled through dedicated tabs:

1. **Data Import:** Upload your `.bed`, `.bim`, and `.fam` files.

2. **Preparation:** Select your uploaded BED file and run the overview to count variants and samples.

3. **Sex Check:*** Identifies discordant sex information.
* Displays F-statistics (Male > 0.8, Female < 0.2).
**Optional Update:** You can update sex information by uploading a tab-delimited text file (Index, ID, Updated Sex) via the **"SQC-Sex update"** tab.

4. **Sample Call Rate:**
* Calculates call rates with an interactive plot.
* Adjust the threshold slider to filter samples (default line is at 95%).

5. **Heterozygosity:**
* Identifies outliers based on deviations from the mean heterozygosity rate (default  SD).

6. **Cryptic Relatedness:**
* Analyzes IBD (Identity By Descent) to find related individuals.
* Thresholds:  (twins/duplicates),  (1st degree),  (2nd degree),  (3rd degree).

7. **Ethnicity:**
* Select at least three sub-populations to run analysis and visualize ancestry.
8. **Remove Sample Outliers (Optional):**
* Upload a tab-delimited text file of Sample IDs to remove specific individuals before Variant QC.

## Variant QC (VQC)

Once Sample QC is complete, proceed to Variant QC checks:

1. **SNP Missingness:** Set a threshold (range 0-0.4) to remove variants with high missingness.

2. **Minor Allele Frequency (MAF):** Filter SNPs based on MAF threshold (range 0-0.1).

3. **Hardy-Weinberg Equilibrium (HWE):**
* Requires a phenotype file (Case/Control) if performing case-control comparison.

* Set a p-value threshold to filter variants deviating from HWE.

4. **Differential Missingness (Optional):**
* Specifically for case-control comparisons to check for biased missingness between groups.

## Data Export

1. Navigate to the **Export results** tab.

2. Copy the full path of your desired local output folder.
**Crucial:** Ensure backslashes `\` are changed to forward slashes `/` when pasting the path.

3. Select the category of files you wish to export (e.g., "Binary_PLINK_file_sex_updated").

4. Click **"Save ZIP Here"** to download the processed files to your specified folder.

## Authors
* **Alexandar Vincent-paulraj**
* **J. Eunice Zhang**
* **Prof. SIR Munir Pirmohamed**

* **University of Liverpool**
