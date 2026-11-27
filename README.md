# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive.

Last update: November 27, 2026 at 06:05 AM ET

## Disk Space

|   Partition | Size (Used / Total)            |
| ----------: | :----------------------------- |
|         001 | 758.76 TB / 967.57 TB (78.42%) |
|         002 | 496.43 TB / 681.70 TB (72.82%) |



## Content

| Location      | Size (Local / Remote)           | Number of Objects (Local / Remote)[^1]   |
| :------------ | :------------------------------ | :--------------------------------------- |
| blobs/        | — / 1.39 PB                     | — / 962162                               |
| dandisets/    | 13.15 GB / 6.67 GB (197.15%)    | 11903 / 10065 (118.26%)                  |
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
| `0`    |         001 | 91.21 TB      |     60408 | OK          |
| `1`    |         001 | 85.71 TB      |     60270 | OK          |
| `2`    |         001 | 85.62 TB      |     60189 | OK          |
| `3`    |         001 | 84.05 TB      |     60521 | OK          |
| `4`    |         001 | 85.72 TB      |     60059 | OK          |
| `5`    |         001 | 88.99 TB      |     59785 | OK          |
| `6`    |         001 | 87.29 TB      |     59990 | OK          |
| `7`    |         001 | 82.18 TB      |     59954 | OK          |
| `8`    |         001 | 83.60 TB      |     60221 | OK          |
| `9`    |         001 | 88.97 TB      |     59991 | OK          |
| `a`    |         002 | 85.44 TB      |     59729 | OK          |
| `b`    |         002 | 86.43 TB      |     60279 | OK          |
| `c`    |         002 | 85.41 TB      |     60290 | OK          |
| `d`    |         002 | 86.10 TB      |     59752 | OK          |
| `e`    |         002 | 90.28 TB      |     60503 | OK          |
| `f`    |         002 | 88.99 TB      |     60221 | OK          |