# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 21, 2026 at 06:03 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 871.49 TB / 967.57 TB (90.07%) |
|         002 | 475.77 TB / 681.70 TB (69.79%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.36 PB                     | — / 958035                               |
| dandisets/    | 13.12 GB / 6.63 GB (197.73%)    | 11828 / 9995 (118.34%)                   |
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
| `0`    |         001 | 89.18 TB      |     60149 | OK          |
| `1`    |         001 | 84.14 TB      |     59999 | OK          |
| `2`    |         001 | 84.12 TB      |     59926 | OK          |
| `3`    |         001 | 82.20 TB      |     60260 | OK          |
| `4`    |         001 | 84.47 TB      |     59789 | OK          |
| `5`    |         001 | 87.59 TB      |     59532 | OK          |
| `6`    |         001 | 84.47 TB      |     59718 | OK          |
| `7`    |         001 | 80.96 TB      |     59738 | OK          |
| `8`    |         001 | 82.36 TB      |     59966 | OK          |
| `9`    |         001 | 87.63 TB      |     59755 | OK          |
| `a`    |         002 | 84.38 TB      |     59488 | OK          |
| `b`    |         002 | 84.98 TB      |     60013 | OK          |
| `c`    |         002 | 83.82 TB      |     60019 | OK          |
| `d`    |         002 | 84.27 TB      |     59487 | OK          |
| `e`    |         002 | 88.60 TB      |     60264 | OK          |
| `f`    |         002 | 87.19 TB      |     59932 | OK          |