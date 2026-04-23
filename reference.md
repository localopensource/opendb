### Info obtained from https://medium.com/@aryamob44/how-database-works-under-the-hood-so-you-know-which-one-to-use-system-design-ff3436d943bd

use indexes but dont overuse them since writes will be slow and reads will be fast
hashmap = store keys in memory and values in harddrive but use append only process use compaction and merging algorithm
segmentation= breaking logs into segments of a certain size ie close a segment when it reaches a specific size and redirect subsequest writes to a new segment file
compaction > we driscard dupicate keys in the log and retain only the most recent update for each key. It is perfomed on individual segments since it is perfomed on individual segments we can then merge al the segments and write them to a new file
reads requests are served i the old segments but when compaction is done the task is transferred to the new segment.

Limitations of hash indexes
____________________________

1. Memory requirements= Must fit entirely in memory even with compaction and merging
2. Inefficiencies with range queries = Not  optimized for range queries


__________________________
|                         |
| SSTABLES AND LSM TREES  |                  |
|_________________________|
* sorts the data with respect to keys ie maintains an in-memory sorted log file that stores, writes and after reeaching a certain point sends the data to the disk in sorted order.
In order to store data in a 