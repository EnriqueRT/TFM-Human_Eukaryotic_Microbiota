# Human Gut Eukaryotic Microbiota Project

This repository contains all the programs and scripts used to generate the results of this project. The aim of this study is to explore a common group of eukaryotic taxa (core) in the microbiota of healthy individuals across different human populations worldwide. To this end, a collection of 33 public studies and meta-studies has been compiled, including the Human Microbiome Project (HMP) and Metagenomics of the Human Intestinal Tract (MetaHIT). 

## Software

- Omics Dataset Curation Toolkit (v.1.0)
- Fastp (v.0.23.2)
- Bowtie2 (v.2.5.1)
- Samtools (v.1.16.1)
- FastQC (v.0.12.1)
- MultiQC (v.1.14)
- EukDetect (v.1.3)
- Snakemake (v.5.3.0)
- R (v.4.2.2)
- Python3 (>= 3.10)

## Python libraries

- matplotlib
- argparse
- fnmatch
- seaborn
- pandas
- numpy

## R libraries

- curatedMetagenomicData
- ComplexHeatmap
- RColorBrewer
- gridExtra
- tidyverse
- reshape2
- ggplot2
- dplyr
- readr
- DT

## Repository content

### Correlation-Prevalence_Study

- The `matrix_correlation.ipynb` script has been used to generate the genus-genus correlation matrix.
- The `eukdetec_prevalence_genus_study.rmd` script has been used to generate the genus level prevalence heatmaps
- The `eukdetec_prevalence_species_heatmap_study.Rmd` script has been used to generate the species level prevalence heatmaps
- The `eukdetec_prevalence_species_stackedplot_study.Rmd` script has been used to generate three stacked bar charts with the individual level prevalences

### EukDetect

| Parameter | Description | 
|   :---    |    :---     |
| `-h, --help` | Show help message and exit. | 
| `-i, --fastq_directory` | Valor 2   | 
| `-l, --library_layout`   | Valor 5   |
| `-r, --read_length`   | Valor 5   |
| `-o1, --output_dir_eukdetect`   | Valor 5   |
| `-o2, --output_dir_configfile`   | Valor 5   |

### Projects

The most relevant information on the curating and processing of all 33 studies has been included in this folder. Each project contains the same information:  

- The `multiqc_stats` directory contains three tables with the statistics of the reads:

   *  `counts_track_table.tsv` is a table where the rows correspond to the samples and the columns to the reads for each sample of the three QC steps. 

   *  `percentages_track_table.tsv` is a table with the same structure, adding for each sample the percentages of readings left over with respect to the total in each of the steps with fastp and bowtie. 

   *  `qc_stats_table.xls` is a table that shows overall statistics of reads per project, the length of the shortest and longest reads, the total number of reads, the average number of reads per sample and percentages associated with the average loss of reads per sample.

- The `Metadata_Final.xls` table contains the individual metadata.

- The three HTML documents: `multiqc_report_bowtie.html`, `multiqc_report_fastp.html` and `multiqc_report_raw.html` contain the statistics provided by MultiQC for each QC step (raw, Fastp and Bowtie2), respectively.

- The `samples_description.odt` document contains a brief description of the sample curing process.


### Quality_Control



### Sequencing_Depth_Filter

