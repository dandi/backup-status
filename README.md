# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 22, 2026 at 06:02 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 686.77 TB / 967.57 TB (70.98%) |
|         002 | 461.43 TB / 681.70 TB (67.69%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.36 PB                     | — / 958480                               |
| dandisets/    | 13.12 GB / 6.64 GB (197.69%)    | 11838 / 10005 (118.32%)                  |
| README.md     | 2.14 KB / 2.14 KB (100.00%)     | 1 / 1 (100.00%)                          |
| index.html    | 3.09 KB / 3.09 KB (100.00%)     | 1 / 1 (100.00%)                          |
| ros3test.hdf5 | 4.01 KB / 4.01 KB (100.00%)     | 1 / 1 (100.00%)                          |
| ros3test.nwb  | 177.73 KB / 177.73 KB (100.00%) | 1 / 1 (100.00%)                          |

[^1]: Reported percentage may exceed 100% due to delayed garbage collection.

The mirror's blobs/ is not walked, so it has no local figures: see Blob Heads for what each head should take and whether it is on its assigned partition.



## Blob Partition Separation

Blobs are distributed across partitions based on the first hex digit of each blob's head hash.

|   Partition | Head Hash Digits (hex)                           |
| ----------: | :----------------------------------------------- |
|         001 | `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9` |
|         002 | `a`, `b`, `c`, `d`, `e`, `f`                     |



## Blob Heads

Size and object count in the bucket of each head (first hex digit of the blob ID), and whether its sub-directories are on its assigned partition only.

| Head   |   Partition | Bucket Size   |   Objects | Placement   |
| :----- | ----------: | :------------ | --------: | :---------- |
| `0`    |         001 | 89.47 TB      |     60185 | OK          |
| `1`    |         001 | 84.46 TB      |     60033 | OK          |
| `2`    |         001 | 84.28 TB      |     59952 | OK          |
| `3`    |         001 | 82.34 TB      |     60287 | OK          |
| `4`    |         001 | 84.62 TB      |     59816 | OK          |
| `5`    |         001 | 87.82 TB      |     59562 | OK          |
| `6`    |         001 | 84.82 TB      |     59744 | OK          |
| `7`    |         001 | 81.06 TB      |     59763 | OK          |
| `8`    |         001 | 82.46 TB      |     59992 | OK          |
| `9`    |         001 | 87.76 TB      |     59776 | OK          |
| `a`    |         002 | 84.61 TB      |     59521 | OK          |
| `b`    |         002 | 85.24 TB      |     60036 | OK          |
| `c`    |         002 | 83.96 TB      |     60051 | OK          |
| `d`    |         002 | 84.62 TB      |     59518 | OK          |
| `e`    |         002 | 88.93 TB      |     60287 | OK          |
| `f`    |         002 | 87.44 TB      |     59957 | OK          |