# KAUST_metagenomic_annotation

KAUST make a metagenomic gene prediction on assembled data to include only complete genes.

This is useful when sequencing technology changes for longer reads.

We can make comparative metagenomics approach using clustering of full-length genes from multiple samples

are mapped onto a common gene catalog.

Obtaining genomic Data 

We download reads of Candidatus Theomargarita magnifica from the article:

https://www.science.org/doi/10.1126/science.abb3634

Accesion numbers from SRA files 


WE use SRAtoolkit for download the information
srapath SRR#######
wget <path>
  
Then we depackage the fastq files:

fastq-dump --gzip --skip-technical  --readids --dumpbase --split-files --clip SRR#####

  
Then we need to assemble the reads with SPAdes:
  
  spades.py [options] -o <output_dir>
  
  THen we annotate uor assembly with Kaust online Platform:
  
  https://www.cbrc.kaust.edu.sa/aamg/1656524222011_TMAG01_90.0_andres_arredondo/
  
  
  
