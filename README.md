# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: September 26, 2026 at 11:30 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 793.10 TB / 967.57 TB (81.97%) |
|         002 | 418.34 TB / 681.70 TB (61.37%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | 1.21 PB / 1.24 PB (97.59%)      | 577306 / 644273 (89.61%)                 |
| dandisets/    | 10.50 GB / 4.02 GB (261.14%)    | 11143 / 9325 (119.50%)                   |
| README.md     | 2.14 KB / 2.14 KB (100.00%)     | 1 / 1 (100.00%)                          |
| index.html    | 3.09 KB / 3.09 KB (100.00%)     | 1 / 1 (100.00%)                          |
| ros3test.hdf5 | 4.01 KB / 4.01 KB (100.00%)     | 1 / 1 (100.00%)                          |
| ros3test.nwb  | 177.73 KB / 177.73 KB (100.00%) | 1 / 1 (100.00%)                          |

[^1]: Reported percentage may exceed 100% due to delayed garbage collection.



## Blob Partition Separation

Blobs are distributed across partitions based on the first hex digit of each blob's head hash.

|   Partition | Head Hash Digits (hex)                           |
| ----------: | :----------------------------------------------- |
|         001 | `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9` |
|         002 | `a`, `b`, `c`, `d`, `e`, `f`                     |