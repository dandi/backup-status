# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 20, 2026 at 06:07 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 869.26 TB / 967.57 TB (89.84%) |
|         002 | 474.21 TB / 681.70 TB (69.56%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.36 PB                     | — / 957687                               |
| dandisets/    | 12.92 GB / 6.43 GB (200.74%)    | 11813 / 9980 (118.37%)                   |
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
| `0`    |         001 | 88.99 TB      |     60127 | OK          |
| `1`    |         001 | 84.01 TB      |     59973 | OK          |
| `2`    |         001 | 84.08 TB      |     59911 | OK          |
| `3`    |         001 | 82.07 TB      |     60237 | OK          |
| `4`    |         001 | 84.41 TB      |     59767 | OK          |
| `5`    |         001 | 87.51 TB      |     59510 | OK          |
| `6`    |         001 | 84.30 TB      |     59699 | OK          |
| `7`    |         001 | 80.75 TB      |     59719 | OK          |
| `8`    |         001 | 82.29 TB      |     59939 | OK          |
| `9`    |         001 | 87.39 TB      |     59732 | OK          |
| `a`    |         002 | 84.23 TB      |     59470 | OK          |
| `b`    |         002 | 84.66 TB      |     59993 | OK          |
| `c`    |         002 | 83.69 TB      |     59994 | OK          |
| `d`    |         002 | 84.11 TB      |     59464 | OK          |
| `e`    |         002 | 88.47 TB      |     60241 | OK          |
| `f`    |         002 | 87.06 TB      |     59911 | OK          |