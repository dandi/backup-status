# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: October 24, 2026 at 06:10 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 794.44 TB / 967.57 TB (82.11%) |
|         002 | 416.05 TB / 681.70 TB (61.03%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | 1.21 PB / 1.26 PB (95.90%)      | 577306 / 878492 (65.72%)                 |
| dandisets/    | 12.50 GB / 6.05 GB (206.81%)    | 11503 / 9690 (118.71%)                   |
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