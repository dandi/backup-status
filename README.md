# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 25, 2026 at 06:03 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 735.76 TB / 967.57 TB (76.04%) |
|         002 | 485.88 TB / 681.70 TB (71.27%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.38 PB                     | — / 960475                               |
| dandisets/    | 13.14 GB / 6.66 GB (197.39%)    | 11888 / 10050 (118.29%)                  |
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
| `0`    |         001 | 90.96 TB      |     60307 | OK          |
| `1`    |         001 | 85.47 TB      |     60161 | OK          |
| `2`    |         001 | 85.42 TB      |     60077 | OK          |
| `3`    |         001 | 83.83 TB      |     60414 | OK          |
| `4`    |         001 | 85.40 TB      |     59943 | OK          |
| `5`    |         001 | 88.74 TB      |     59671 | OK          |
| `6`    |         001 | 87.07 TB      |     59875 | OK          |
| `7`    |         001 | 82.04 TB      |     59868 | OK          |
| `8`    |         001 | 83.33 TB      |     60114 | OK          |
| `9`    |         001 | 88.74 TB      |     59900 | OK          |
| `a`    |         002 | 85.24 TB      |     59638 | OK          |
| `b`    |         002 | 86.15 TB      |     60172 | OK          |
| `c`    |         002 | 85.15 TB      |     60188 | OK          |
| `d`    |         002 | 85.90 TB      |     59655 | OK          |
| `e`    |         002 | 90.02 TB      |     60406 | OK          |
| `f`    |         002 | 88.76 TB      |     60086 | OK          |