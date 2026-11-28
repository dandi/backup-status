# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 28, 2026 at 06:03 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 770.23 TB / 967.57 TB (79.60%) |
|         002 | 496.60 TB / 681.70 TB (72.85%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.39 PB                     | — / 962385                               |
| dandisets/    | 13.16 GB / 6.67 GB (197.16%)    | 11908 / 10070 (118.25%)                  |
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
| `0`    |         001 | 91.29 TB      |     60422 | OK          |
| `1`    |         001 | 85.76 TB      |     60278 | OK          |
| `2`    |         001 | 85.73 TB      |     60211 | OK          |
| `3`    |         001 | 84.12 TB      |     60532 | OK          |
| `4`    |         001 | 85.80 TB      |     60076 | OK          |
| `5`    |         001 | 89.04 TB      |     59797 | OK          |
| `6`    |         001 | 87.34 TB      |     60001 | OK          |
| `7`    |         001 | 82.25 TB      |     59966 | OK          |
| `8`    |         001 | 83.68 TB      |     60232 | OK          |
| `9`    |         001 | 89.10 TB      |     60012 | OK          |
| `a`    |         002 | 85.51 TB      |     59743 | OK          |
| `b`    |         002 | 86.54 TB      |     60294 | OK          |
| `c`    |         002 | 85.52 TB      |     60308 | OK          |
| `d`    |         002 | 86.13 TB      |     59767 | OK          |
| `e`    |         002 | 90.36 TB      |     60514 | OK          |
| `f`    |         002 | 89.04 TB      |     60232 | OK          |