# DANDI Backup Status

Current status of S3 bucket backup of the DANDI Archive' as of 2025/08/13.

| Location             | Size                                     | Number of Objects                        |
|                      | Local / Remote (%)                       | Local / Remote (%)                      [^1] |
| -------------------- | ---------------------------------------- | ---------------------------------------- |
| blobs/               | 749.04 TB / 837.38 TB (89.45%)           | 311857 / 484191 (64.41%)                 |
| dandisets/           | 2.34 GB / 2.34 GB (99.99%)               | 6835 / 6840 (99.93%)                     |
| README.md            | 2.14 KB / 2.14 KB (100.00%)              | 1 / 1 (100.00%)                          |
| index.html           | 3.09 KB / 3.09 KB (100.00%)              | 1 / 1 (100.00%)                          |
| ros3test.hdf5        | 4.01 KB / 4.01 KB (100.00%)              | 1 / 1 (100.00%)                          |
| ros3test.nwb         | 177.73 KB / 177.73 KB (100.00%)          | 1 / 1 (100.00%)                          |

[^1]: Reported percentage may exceed 100% due to delayed garbage collection.
