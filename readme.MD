#h2 Contents
This repo contains pre-generated query stream files for a few different <b>scale factors</b>.
The convention for TPC-DS is "sfXXXX" where XXXX is the size of the raw data set in gigabytes (GB).  

|Sacle Factor|Directory Name|
|:-----------|:--------------|
|100 GB|sf100_queries|
|1 TB (1000 GB)|sf1000_queries|
|3 TB (3000 GB)|sf3000_queries|
10 TB (1000 GB)|sf10000_queries|


For each scale, there are four query stream files, named <b>query_N.sql</b>. 

Details about the official TPD-DS benchmark can be found at https://www.tpc.org/tpcds/default5.asp.
The queries are in a pre-determined (pseudo random) order per the TPC-DS spec. 

In general, any results obtained using the query stream files contained in this repos should follow the guidelines from TPC.org for the
TPC DS benchmark which are spelled out explicitly in the license agreement for the benchmark. 


#2 NNVIDIA Spark-RAPIDS - NVIDIA Decsion Support (NDS) Benchmark

The query stream files in this repo were generated using the [nds_gen_query_stream.py](https://github.com/NVIDIA/spark-rapids-benchmarks/blob/dev/nds/nds_gen_query_stream.py)
utility

found in the [NVIDIA/spark_rapids_benchmarks](https://github.com/NVIDIA/spark-rapids-benchmarks) github repo.

nds_gen_query_stream.py is essentially a wrapper for the offiical TPC-DS query generator (dsqgen). 

The syntax for the command line is documented [here](https://github.com/NVIDIA/spark-rapids-benchmarks/tree/dev/nds#query-generation).


```text
usage: nds_gen_query_stream.py [-h] (--template TEMPLATE | --streams STREAMS)
                               template_dir scale output_dir

positional arguments:
  template_dir         directory to find query templates and dialect file.
  scale                assume a database of this scale factor.
  output_dir           generate query in directory.

optional arguments:
  -h, --help           show this help message and exit
  --template TEMPLATE  build queries from this template. Only used to generate one query from one tempalte. This argument is mutually exclusive with --streams. It
                       is often used for test purpose.
  --streams STREAMS    generate how many query streams. This argument is mutually exclusive with --template.
  --rngseed RNGSEED    seed the random generation seed.
```


