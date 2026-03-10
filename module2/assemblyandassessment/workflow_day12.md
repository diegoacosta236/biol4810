\# Day 12 — Galaxy QC → Trim → Assembly → QUAST



\## Sample

\- sampleID: X

\- raw data: Given (WT\_R1/WT\_R2)



\## Tools (Galaxy / usegalaxy.org)

\- FastQC: 0.74

\- fastp: 1.1.0

\- SPAdes: 4.2.0

\- QUAST: 5.3.0



\## Steps

1\. FastQC on raw reads → saved report as: X\_forward\_fastqc.html

2\. fastp trimming (default settings) → saved report as:X\_fastp\_trimming\_report.html

3\. FastQC on trimmed reads → saved report as: X\_forward\_trimmed\_fastqc.html

4\. SPAdes assembly on trimmed reads → saved contigs as: X\_assembly\_contigs.fasta

5\. QUAST evaluation on contigs → saved report as: X\_assembly\_report\_contigs.pdf



\## Notes / interpretation

\- After trimming, the amount of reads and bases decreased. The quality of the reads went up slightly as well, which could suggest that the sequences were already mostly clean.

\- The QUAST report suggests that the assembly is very contiguous as the N50 and L50 values would correspond with that. The number of contigs above, or equal to, 1000 bp is 60, which is not too high as well.

