# genome 

# Introduction

The original task belongs to [Mohamed Samour](https://www.linkedin.com/in/mohamed-samour-63794235/) 

## Links 

*  List of tools https://github.com/pratas/rebico/blob/master/src/install.sh
*  http://www2.informatik.hu-berlin.de/~wandelt/blockcompression/ABRC_0.2.zip
*  https://github.com/sfu-compbio/scalce
*  https://bitbucket.org/mhowison/seqdb

## Tools

*  [TopHat](http://ccb.jhu.edu/software/tophat/index.shtml) is a fast splice junction mapper for RNA-Seq reads. It aligns RNA-Seq reads to mammalian-sized genomes using the ultra high-throughput short read aligner Bowtie, and then analyzes the mapping results to identify splice junctions between exons. See also [HISAT2](http://ccb.jhu.edu/software/hisat2/index.shtml)


### A few databases:
*  https://www.ncbi.nlm.nih.gov/sra/
*  https://cancergenome.nih.gov/
*  http://www.internationalgenome.org/

### Workflows

*  http://cole-trapnell-lab.github.io/cufflinks/manual/
*  https://bioedge.lanl.gov/edge_ui/  Government/Public effort for a web-based analysis tool (has good diagrams on landing page about workflow)

## Literature 

*  Start with "Data compression for sequencing data" - it has a summary of compressions software.

## Some ideas

*  Support configuration profile according to the price of the storage, data delivery, usage, typical reseacrh flow/tasks. The sysyem can adapt the compression algrothms to the profile and reduce the costs and/or improve performance of specific tasks
*  Database dedicated for storing and accessing the genome. For example, "projections" (a term from Vertica) can be generated for fast lookup of specific seqences in the genome. 
*  A custom database which leverages distributed storage and awareness of the data properties. For example, we know that the "object" is between 50GB to 300GB. We know number of objects. We know a structure of objects. We can try to save SINEs, LINEs etc with index and partially reconstruct the recorded genomes from such a table.


## Use cases - Database

A columnar, non-SQL database is assumed as a best fit for the task.

*  SELECT [catalogue name] [catalogue date] [recording date] [last use date] [last modification date] [pattern] [score]
*  CONVERT [from fromat] [to format]
*  FIND (genomes ...) [longest match] [first best alignment] [Nth best alignment] [overlaps]
*  INSERT/DELETE [remove pattern] [from offest to offset] [partial matches]
