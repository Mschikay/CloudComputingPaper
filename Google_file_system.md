# GFS
#### 2.7.2 implications 
1. Appending is far more efficient and more resilient to applicaiton failures than random writers.

2. Checkpointing allows writers to restart incrementally and keeps readers from processing successfully written data that is still incomplete from the application's perspective.
### 3.3 atomic records append
1. it does not guarantee all replicas bytewise identical. It only guarantee the data is written at least once as an atomic unit.

5.2 Data Integrity
chunkserver uses checksumming to detect corruption. 