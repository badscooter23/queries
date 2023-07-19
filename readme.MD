This repo contains pre-generated query stream files for a few different scale factors.

|Sacle Factor|Directory Name|
|:-----------|:--------------|
|100 GB|sf100_queries|
|1 TB (1000 GB)|sf1000_queries|
|3 TB (3000 GB)|sf3000_queries|
10 TB (1000 GB)|sf10000_queries|


For each scale, there are four query stream files, named <b>query_N.sql</b>. 

The queries are in a pre-determined (pseudo random) order per the TPC-DS spec. 
The query stream files were generated using the TPC-DS query generatory (dsdgen) and the queries were 
generated using the default random seed. 
