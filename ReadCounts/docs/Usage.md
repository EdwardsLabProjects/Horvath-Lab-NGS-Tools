# ReadCounts Usage

## Synopsis

### Graphical User Interface:

    readCounts

### Command-line:

    readCounts [options]

## Description

ReadCounts tabulates the number of reads providing evidence for variant and reference nucleotides at specific genomic loci and applies statistical tests to recognize allelic read-counts consistent with homozygous and heterozygous loci.

## Graphical User Interface

<img src="readCounts.png" alt="ReadCounts"/>

Click the help icon (question mark) at the top right of the GUI and
then an input field label for help. Multiple files can be selected in the
file-chooser using Ctrl-Click or Shift-Click. Fields can be reset to
their default values using the Reset button. Click OK to execute
readCounts.

Additional GUI option tabs are documented below.

## Options

SNVs, -s SNVS, --snvs=SNVS

> Single-nucleotide-variants (SNVs). Tabular and VCF format SNVs
> are supported. Multiple SNV files can be selected from the chooser in the graphical user interface, and on the command-line specified inside quotes, separated
> by spaces, or by using file globbing. See [Input
> Files](InputFiles.md) for more information. Required.

Read Alignment Files, -r ALIGNMENTS, --readalignments=ALIGNMENTS

> Read alignments files in indexed BAM format, with extension
> `.bam`. BAM index with extension `.bam.bai` must be located in the
> same directory. Multiple BAM files can be selected from the chooser in the graphical user interface, and on the command-line specified inside quotes,
> separated by spaces, or by using file globbing. See [Input
> Files](InputFiles.md) for more information. Required.

Alignment Filter, -f FILTER, --alignmentfilter=FILTER

> Alignment filtering strategy. See [Read Filtering](Filtering.md) for more details. Default: Basic.

Output Folder, -o OUTPUT, --output=OUTPUT

> Output file. Will be created if necessary. See [Output Files](OutputFiles.md) for more information on output files. Optional. 

--version

>Show version number and exit. 

-h, --help

>Show command-help and exit.

### Advanced
<img src="readCounts-advanced.png" alt="Advanced"/>

Min. Reads, -m MINREADS, --minreads=MINREADS

> Minimum number of good reads at each SNV locus per alignment file. Default=10.   

Max. Reads, -m MAXREADS, --maxreads=MAXREADS

> Scale read counts at high-coverage loci to ensure at
                        most this many good reads at SNV locus per alignment
                        file. Values greater than 1 indicate absolute read
                        counts, otherwise the value indicates the coverage
                        distribution percentile. Default=No maximum.


All Fields, -F, --full

> Output extra diagnostic read count fields. Default: Essential fields only. 

Unique Reads, -U, --uniquereads   

> Consider only distinct reads.  

Threads/BAM, -t TPB, --threadsperbam=TPB                   

> Each worker thread is allocated one or more BAM files. Indicate no threading with 0. Default: 0.

Read Group, -G READGROUP, --readgroup=READGROUP

> Additional read grouping based on read name/identifier strings or BAM-file RG. [Read Grouping](Grouping.md) for more details. Default: None, group reads by BAM-file only.

Quiet, -q, --quiet

> Do not show readCounts progress.
