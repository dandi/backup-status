# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 26, 2026 at 06:07 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 747.21 TB / 967.57 TB (77.23%) |
|         002 | 492.49 TB / 681.70 TB (72.24%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.38 PB                     | — / 960908                               |
| dandisets/    | 13.14 GB / 6.66 GB (197.34%)    | 11898 / 10060 (118.27%)                  |
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
| `0`    |         001 | 91.10 TB      |     60335 | OK          |
| `1`    |         001 | 85.58 TB      |     60195 | OK          |
| `2`    |         001 | 85.54 TB      |     60105 | OK          |
| `3`    |         001 | 83.94 TB      |     60437 | OK          |
| `4`    |         001 | 85.58 TB      |     59978 | OK          |
| `5`    |         001 | 88.87 TB      |     59694 | OK          |
| `6`    |         001 | 87.18 TB      |     59902 | OK          |
| `7`    |         001 | 82.10 TB      |     59887 | OK          |
| `8`    |         001 | 83.44 TB      |     60142 | OK          |
| `9`    |         001 | 88.84 TB      |     59920 | OK          |
| `a`    |         002 | 85.34 TB      |     59659 | OK          |
| `b`    |         002 | 86.27 TB      |     60201 | OK          |
| `c`    |         002 | 85.29 TB      |     60215 | OK          |
| `d`    |         002 | 85.98 TB      |     59678 | OK          |
| `e`    |         002 | 90.16 TB      |     60433 | OK          |
| `f`    |         002 | 88.92 TB      |     60127 | OK          |