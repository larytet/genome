# genome

## Links 

*  List of tools https://github.com/pratas/rebico/blob/master/src/install.sh
*  http://www2.informatik.hu-berlin.de/~wandelt/blockcompression/ABRC_0.2.zip
*  https://github.com/sfu-compbio/scalce
*  https://bitbucket.org/mhowison/seqdb


## Literature 

*  "Data compression for sequencing data" has a summary of compressions software.

## Some ideas

*  Support configuration profile according to the price of the storage, data delivery, usage, typical reseacrh flow/tasks. The sysyem can adapt the compression algrothms to the profile and reduce the costs and/or improve performance of specific tasks
*  Database dedicated for storing and accessing the genome. For example, "projections" (a term from Vertica) can be generated for fast lookup of specific seqences in the genome. 
*  A custom database which leverages distributed storage and awareness of the data properties. For example, we know that the "object" is between 50GB to 300GB. We know number of objects. We know a structure of objects. We can try to save SINEs, LINEs etc with index and partially reconstruct the recorded genomes from such a table.
