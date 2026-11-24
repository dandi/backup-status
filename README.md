# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 24, 2026 at 06:07 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 719.15 TB / 967.57 TB (74.32%) |
|         002 | 476.22 TB / 681.70 TB (69.86%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.38 PB                     | — / 960088                               |
| dandisets/    | 13.12 GB / 6.64 GB (197.58%)    | 11868 / 10030 (118.33%)                  |
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
| `0`    |         001 | 90.79 TB      |     60283 | OK          |
| `1`    |         001 | 85.30 TB      |     60135 | OK          |
| `2`    |         001 | 85.36 TB      |     60060 | OK          |
| `3`    |         001 | 83.74 TB      |     60396 | OK          |
| `4`    |         001 | 85.22 TB      |     59913 | OK          |
| `5`    |         001 | 88.67 TB      |     59657 | OK          |
| `6`    |         001 | 86.94 TB      |     59855 | OK          |
| `7`    |         001 | 81.89 TB      |     59842 | OK          |
| `8`    |         001 | 83.14 TB      |     60083 | OK          |
| `9`    |         001 | 88.59 TB      |     59875 | OK          |
| `a`    |         002 | 85.12 TB      |     59618 | OK          |
| `b`    |         002 | 85.97 TB      |     60142 | OK          |
| `c`    |         002 | 85.04 TB      |     60166 | OK          |
| `d`    |         002 | 85.77 TB      |     59622 | OK          |
| `e`    |         002 | 89.87 TB      |     60382 | OK          |
| `f`    |         002 | 88.61 TB      |     60059 | OK          |