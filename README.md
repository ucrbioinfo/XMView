# XMView
A Multiple Alignment XMap Viewer with Genetic Map Integration 

XMView, a software tool that visualizes the alignment of assembled contigs against two optical maps. Optionally, a genetic map can be uploaded as separate track.  Both of these features can help users to discover chimeric contigs.  

Binaries are available here for Linux, macOS, Windows.  Source code will be coming soon.

XMView takes the following inputs:
Up to two optical maps from Refaligner, and an optional BLAST output file of mapped SNPs.

The BLAST file is a tab-delimited text file you produce that contains map coordinates.
It is used to display the map coordinates as LG:cM underneath your sequence assemblies/contigs.
This information is also used when you click on the "Spreadsheet" button.
<pre>
#snp     contig       contig_start  contig_end   LG   cM
1_0003   Contig12345  79100         79200        7    12.3
2_1234   Contig2      232322        232400       1    101.2
...
</pre>
The header is optional, and can be anything, but must start with a pound sign "#".
The contig column is for the normal contig names from your assembly.  This is
not the index assigned by Refaligner.

XMView does not filter on e-score, so you should do that, perhaps with a cutoff of 1e-50.
XMView only uses the lines that have map coordinates.


Steve Wanamaker
Close Lab
Department of Botany and Plant Sciences
University of California, Riverside
stevew@ucr.edu
