Step 1)

Run FastQC on raw reads

Tool: FastQC

Version: Galaxy Version 0.74 + galaxy1

Parameters: Default

Files downloaded: forward\_report.html

\* Per tile has an X, Per Base is cautious, Sequence Length Distribution is Cautious



Step 2)

FastP trimming/filtering

Tool: FastP

Version: Galaxy Version 1.1.0+galaxy0

Parameters: Single-end -> Paired Collection, otherwise Default

Files downloaded: fastp\_report.html



Step 3) 

FastQC on trimmed reads (after FastP)

Tool: FastQC

Version: Galaxy Version 0.74 + galaxy1

Parameters: Single-end -> Paired Collection, otherwise Default

Files downloaded: fastp\_report.html



Step 4)

SPAdes assembly on trimmed reads

Tool: SPAdes

Version: Galaxy Version 4.2.0+galaxy0

Parameters: Default

File downloaded: contigs file



Step 5)

Check the quality of assembled genome using Quast

Tool: Quast

Version: Galaxy Version 5.3.0+galaxy1

Parameters: Selected contigs for 'Contigs/scaffolds file', included PDF report

File downloaded: PDF report



Step 6)

Filter assembly to reduce smaller contigs

Tool: Filter FASTA

Version: Galaxy Version 2.3

Parameters: Criteria for filtering on the sequences -> min. length: 500 bp, Selected the Contigs

File downloaded: filtered.fasta file



Step 7)

Check genome information

Tool: CheckM2

Version: Galaxy Version 1.1.0+galaxy0

Parameters: Default

File downloaded: PDF report



Step 8)

Annotate the filtered assembly

Tool: Prokka

Version: Galaxy Version 1.14.6+galaxy1

Parameters: Force compliance -> YES

Files downloaded: .faa, .ffn, .gbk, .gff3, .txt



Step 9)

Blast the 16S sequence to get species ID

Tool: BLAST

Version: Web

Parameters: Default

\* Got Acinetobacter baumannii

\* Downloaded two different fasta files for ANI comparison



Step 10) 

Compare two different species/strains

Tool: ANI (EZBioCloud)

Version: Web

Parameters: Default



Step 11)

Finding out what AMR genes the organism has

Tool: CARD/RGI

Version: RGI 6.0.5/CARD 4.0.1

Parameters: Default



Step 12) 

Check AMR genes on another website to crossreference

Tool: ResFinder

Version: 4.7.2

Parameters: Default



Step 13)

Check if the organism has human pathogen capabilities

Tool: PathogenFinder

Version: 0.6.0

Parameters: Default



Step 14)

Find virulence factors through a database

Tool: ABRicate (Galaxy)

Version: ABRicate 1.0.1/ VFDB 2024-Dec-15

Parameters: Default

Files downloaded: tabular file

\* 0 hits



Step 15)

Check biosynthetic gene clusters

Tool: antiSMASH

Version: 8.0.4

Parameters: Default



Step 16)

Check gene island findings

Tool: IslandViewer4

Version: Web

Parameters: Default



Step 17)

Check for CRISPR arrays + Cas genes

Tool: CRISPRCasFinder

Version: Web

Parameters: Default

\* No hits



