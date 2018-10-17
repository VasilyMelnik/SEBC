[root@instance-6 ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=4 -Ddfs.block.size=32m -Ddfs.replication=1 5000000 /user/VasilyMelnik/tmp3
18/10/16 13:26:10 INFO client.RMProxy: Connecting to ResourceManager at instance-3.europe-north1-a.c.cloudera-218907.internal/10.166.0.4:8032
18/10/16 13:26:11 INFO terasort.TeraGen: Generating 5000000 using 4
18/10/16 13:26:11 INFO mapreduce.JobSubmitter: number of splits:4
18/10/16 13:26:11 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/10/16 13:26:11 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539693794393_0001
18/10/16 13:26:12 INFO impl.YarnClientImpl: Submitted application application_1539693794393_0001
18/10/16 13:26:12 INFO mapreduce.Job: The url to track the job: http://instance-3.europe-north1-a.c.cloudera-218907.internal:8088/proxy/application_1539693794393_0001/
18/10/16 13:26:12 INFO mapreduce.Job: Running job: job_1539693794393_0001
18/10/16 13:26:19 INFO mapreduce.Job: Job job_1539693794393_0001 running in uber mode : false
18/10/16 13:26:19 INFO mapreduce.Job:  map 0% reduce 0%
18/10/16 13:26:29 INFO mapreduce.Job:  map 100% reduce 0%
18/10/16 13:26:30 INFO mapreduce.Job: Job job_1539693794393_0001 completed successfully
18/10/16 13:26:30 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=601848
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=337
                HDFS: Number of bytes written=500000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=30362
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=30362
                Total vcore-milliseconds taken by all map tasks=30362
                Total megabyte-milliseconds taken by all map tasks=31090688
        Map-Reduce Framework
                Map input records=5000000
                Map output records=5000000
                Input split bytes=337
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=489
                CPU time spent (ms)=16120
                Physical memory (bytes) snapshot=1421287424
                Virtual memory (bytes) snapshot=6337835008
                Total committed heap usage (bytes)=1674051584
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=10735710707299981
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=500000000

[root@instance-6 ~]# hadoop fs -du -s -h /user/VasilyMelnik/tmp3
476.8 M  476.8 M  /user/VasilyMelnik/tmp3

hadoop distcp -skipcrccheck -update /user/VasilyMelnik/tmp3 hdfs://35.228.150.213:8020/user/VasilyMelnik/target6
