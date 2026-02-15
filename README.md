# Parsing-VCF-and-Categorizing-Variants
This contains the code written for the MSc Bioinformatics course - Biological Computing in Python.
this program takes a vcf file, a gff file, and a genome fasta file. for every variant listed in the vcf file, it uses the genome fasta files (sequence(s)), and the genome annotation file (gff), to calculate if the variant is non-coding, synonymous, or non-synonymous, and reports this information and other relevant data in an output file. it also creates a barplot of each variant type, and a log file showing progress of the program.

usage – python3 script.py vcfFile.vcf gffFile.gff fastaFile.fasta

for detailed instructions - python3 script.py --help

Description of Input Files

The VCF file is a file that contains information about all the variants found in a sequencing experiment. It is created by a variant caller algorithm.
The genome FASTA file is a FASTA format file containing the genomic reference sequence(s) of the given organism.
The GFF file is the genome annotation file containing metadata regarding the sequences.
Description of Output Files There are three output files –

The main output file is a tab-delimited file containing information about the classification of the variants in the vcf file. It has the following columns –
a. Chrom - the ID of the region of the genome on which the variant exists b. Pos – the location of the variant on the genomic sequence
c. Ref – the base that exists in the reference sequence at the location of the variant d. Alt – the variant base
e. Type – the category in which the variant lies – non-coding, synonymous, or non-synonymous
f. Transcript – the ID of the transcript in which the variant exists (for cases of multiple transcripts, there’s multiple rows of data)
g. Protein Location – the location of the variant in the protein of the respective transcript
h. Ref AA – the amino acid in the reference protein at the location where the variant has been found. i. Alt AA – (if there is a change in the amino acid) the new (variant) amino acid located at the position of the variant.
A bar plot that shows the proportion of the three categories of variants.
A log file listing the input files received, the output file names and locations, the number of low-quality records found, and any errors handled during runtime.
