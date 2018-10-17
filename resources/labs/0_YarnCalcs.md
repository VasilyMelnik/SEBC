1. 
Start with at least 8 GB for your operating system
The HDFS DataNode uses a minimum of 1 core and about 1 GB of memory
We are going to use YARN and Impala: so 
We asuume that we use cluster for batch workloads:
 "For mostly batch workloads, you might allocate YARN 60%, Impala 30%"

So the result is:
	Memory	vcores
OS	8	1
NodeManager	1	1
DataNode	1	1
Impalad	38,4	4
CM Agent	1	1
HBase	1	1
Solr	1	1
YARN resources	76,6	10


2. 
Workload factor affects mapreduce.job.maps and mapreduce.job.reduces in Gateway settings
It limits the number of mappers in case of big number of cpu. 
So if our workload consists of big batch jobs, we set higher workload factor. 

 