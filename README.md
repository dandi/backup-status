# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 23, 2026 at 06:03 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 699.58 TB / 967.57 TB (72.30%) |
|         002 | 462.88 TB / 681.70 TB (67.90%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.38 PB                     | — / 959115                               |
| dandisets/    | 13.12 GB / 6.64 GB (197.65%)    | 11858 / 10020 (118.34%)                  |
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
| `0`    |         001 | 90.66 TB      |     60232 | OK          |
| `1`    |         001 | 85.18 TB      |     60069 | OK          |
| `2`    |         001 | 85.22 TB      |     59993 | OK          |
| `3`    |         001 | 83.61 TB      |     60332 | OK          |
| `4`    |         001 | 85.11 TB      |     59855 | OK          |
| `5`    |         001 | 88.43 TB      |     59597 | OK          |
| `6`    |         001 | 86.74 TB      |     59791 | OK          |
| `7`    |         001 | 81.73 TB      |     59795 | OK          |
| `8`    |         001 | 82.97 TB      |     60026 | OK          |
| `9`    |         001 | 88.35 TB      |     59809 | OK          |
| `a`    |         002 | 84.99 TB      |     59563 | OK          |
| `b`    |         002 | 85.81 TB      |     60075 | OK          |
| `c`    |         002 | 84.94 TB      |     60106 | OK          |
| `d`    |         002 | 85.54 TB      |     59556 | OK          |
| `e`    |         002 | 89.64 TB      |     60322 | OK          |
| `f`    |         002 | 88.44 TB      |     59994 | OK          |