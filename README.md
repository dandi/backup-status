# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 13, 2026 at 07:57 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 816.21 TB / 967.57 TB (84.36%) |
|         002 | 435.84 TB / 681.70 TB (63.93%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | 1.25 PB / 1.34 PB (93.59%)      | 646605 / 923901 (69.99%)                 |
| dandisets/    | 12.85 GB / 6.37 GB (201.68%)    | 11738 / 9910 (118.45%)                   |
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