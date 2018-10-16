1. 
[root@instance-6 ~]# time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=4 -Ddfs.block.size=32m -Ddfs.replication=1 100000000 /user/VasilyMelnik/lab212
18/10/16 11:48:06 INFO client.RMProxy: Connecting to ResourceManager at instance-3.europe-north1-a.c.cloudera-218907.internal/10.166.0.4:8032
18/10/16 11:48:06 INFO terasort.TeraGen: Generating 100000000 using 4
18/10/16 11:48:06 INFO mapreduce.JobSubmitter: number of splits:4
18/10/16 11:48:06 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/10/16 11:48:07 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539689557872_0003
18/10/16 11:48:07 INFO impl.YarnClientImpl: Submitted application application_1539689557872_0003
18/10/16 11:48:07 INFO mapreduce.Job: The url to track the job: http://instance-3.europe-north1-a.c.cloudera-218907.internal:8088/proxy/application_1539689557872_0003/
18/10/16 11:48:07 INFO mapreduce.Job: Running job: job_1539689557872_0003
18/10/16 11:48:14 INFO mapreduce.Job: Job job_1539689557872_0003 running in uber mode : false
18/10/16 11:48:14 INFO mapreduce.Job:  map 0% reduce 0%
18/10/16 11:48:32 INFO mapreduce.Job:  map 33% reduce 0%
18/10/16 11:48:38 INFO mapreduce.Job:  map 54% reduce 0%
18/10/16 11:48:44 INFO mapreduce.Job:  map 75% reduce 0%
18/10/16 11:48:50 INFO mapreduce.Job:  map 98% reduce 0%
18/10/16 11:48:51 INFO mapreduce.Job:  map 100% reduce 0%
18/10/16 11:48:51 INFO mapreduce.Job: Job job_1539689557872_0003 completed successfully
18/10/16 11:48:51 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=593260
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=139586
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=139586
                Total vcore-milliseconds taken by all map tasks=139586
                Total megabyte-milliseconds taken by all map tasks=142936064
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1305
                CPU time spent (ms)=152540
                Physical memory (bytes) snapshot=1082748928
                Virtual memory (bytes) snapshot=6320308224
                Total committed heap usage (bytes)=1014497280
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    0m48.091s
user    0m5.300s
sys     0m0.306s

2.

[root@instance-6 ~]# time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=4 -Ddfs.block.size=32m -Ddfs.replication=1 /user/VasilyMelnik/lab212  /user/VasilyMelnik/lab212_result
18/10/16 12:01:41 INFO terasort.TeraSort: starting
18/10/16 12:01:43 INFO input.FileInputFormat: Total input paths to process : 4
Spent 205ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 209ms
Sampling 10 splits of 300
Making 8 from 100000 sampled records
Computing parititions took 706ms
Spent 918ms computing partitions.
18/10/16 12:01:43 INFO client.RMProxy: Connecting to ResourceManager at instance-3.europe-north1-a.c.cloudera-218907.internal/10.166.0.4:8032
18/10/16 12:01:44 INFO mapreduce.JobSubmitter: number of splits:300
18/10/16 12:01:44 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/10/16 12:01:44 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539689557872_0005
18/10/16 12:01:44 INFO impl.YarnClientImpl: Submitted application application_1539689557872_0005
18/10/16 12:01:44 INFO mapreduce.Job: The url to track the job: http://instance-3.europe-north1-a.c.cloudera-218907.internal:8088/proxy/application_1539689557872_0005/
18/10/16 12:01:44 INFO mapreduce.Job: Running job: job_1539689557872_0005
18/10/16 12:01:50 INFO mapreduce.Job: Job job_1539689557872_0005 running in uber mode : false
18/10/16 12:01:50 INFO mapreduce.Job:  map 0% reduce 0%
18/10/16 12:02:00 INFO mapreduce.Job:  map 1% reduce 0%
18/10/16 12:02:02 INFO mapreduce.Job:  map 3% reduce 0%
18/10/16 12:02:10 INFO mapreduce.Job:  map 4% reduce 0%
18/10/16 12:02:11 INFO mapreduce.Job:  map 5% reduce 0%
18/10/16 12:02:14 INFO mapreduce.Job:  map 6% reduce 0%
18/10/16 12:02:20 INFO mapreduce.Job:  map 7% reduce 0%
18/10/16 12:02:21 INFO mapreduce.Job:  map 8% reduce 0%
18/10/16 12:02:22 INFO mapreduce.Job:  map 9% reduce 0%
18/10/16 12:02:29 INFO mapreduce.Job:  map 10% reduce 0%
18/10/16 12:02:30 INFO mapreduce.Job:  map 11% reduce 0%
18/10/16 12:02:35 INFO mapreduce.Job:  map 12% reduce 0%
18/10/16 12:02:38 INFO mapreduce.Job:  map 13% reduce 0%
18/10/16 12:02:39 INFO mapreduce.Job:  map 14% reduce 0%
18/10/16 12:02:44 INFO mapreduce.Job:  map 15% reduce 0%
18/10/16 12:02:47 INFO mapreduce.Job:  map 16% reduce 0%
18/10/16 12:02:48 INFO mapreduce.Job:  map 17% reduce 0%
18/10/16 12:02:54 INFO mapreduce.Job:  map 18% reduce 0%
18/10/16 12:02:56 INFO mapreduce.Job:  map 19% reduce 0%
18/10/16 12:02:58 INFO mapreduce.Job:  map 20% reduce 0%
18/10/16 12:03:03 INFO mapreduce.Job:  map 21% reduce 0%
18/10/16 12:03:05 INFO mapreduce.Job:  map 22% reduce 0%
18/10/16 12:03:06 INFO mapreduce.Job:  map 23% reduce 0%
18/10/16 12:03:12 INFO mapreduce.Job:  map 24% reduce 0%
18/10/16 12:03:14 INFO mapreduce.Job:  map 25% reduce 0%
18/10/16 12:03:19 INFO mapreduce.Job:  map 26% reduce 0%
18/10/16 12:03:21 INFO mapreduce.Job:  map 27% reduce 0%
18/10/16 12:03:23 INFO mapreduce.Job:  map 28% reduce 0%
18/10/16 12:03:26 INFO mapreduce.Job:  map 29% reduce 0%
18/10/16 12:03:32 INFO mapreduce.Job:  map 30% reduce 0%
18/10/16 12:03:33 INFO mapreduce.Job:  map 31% reduce 0%
18/10/16 12:03:36 INFO mapreduce.Job:  map 32% reduce 0%
18/10/16 12:03:40 INFO mapreduce.Job:  map 33% reduce 0%
18/10/16 12:03:43 INFO mapreduce.Job:  map 34% reduce 0%
18/10/16 12:03:47 INFO mapreduce.Job:  map 35% reduce 0%
18/10/16 12:03:49 INFO mapreduce.Job:  map 36% reduce 0%
18/10/16 12:03:53 INFO mapreduce.Job:  map 37% reduce 0%
18/10/16 12:03:55 INFO mapreduce.Job:  map 38% reduce 0%
18/10/16 12:04:00 INFO mapreduce.Job:  map 39% reduce 0%
18/10/16 12:04:02 INFO mapreduce.Job:  map 40% reduce 0%
18/10/16 12:04:07 INFO mapreduce.Job:  map 41% reduce 0%
18/10/16 12:04:09 INFO mapreduce.Job:  map 42% reduce 0%
18/10/16 12:04:12 INFO mapreduce.Job:  map 43% reduce 0%
18/10/16 12:04:16 INFO mapreduce.Job:  map 44% reduce 0%
18/10/16 12:04:19 INFO mapreduce.Job:  map 45% reduce 0%
18/10/16 12:04:22 INFO mapreduce.Job:  map 46% reduce 0%
18/10/16 12:04:24 INFO mapreduce.Job:  map 47% reduce 0%
18/10/16 12:04:30 INFO mapreduce.Job:  map 49% reduce 0%
18/10/16 12:04:35 INFO mapreduce.Job:  map 50% reduce 0%
18/10/16 12:04:37 INFO mapreduce.Job:  map 51% reduce 0%
18/10/16 12:04:39 INFO mapreduce.Job:  map 52% reduce 0%
18/10/16 12:04:44 INFO mapreduce.Job:  map 53% reduce 0%
18/10/16 12:04:47 INFO mapreduce.Job:  map 54% reduce 0%
18/10/16 12:04:50 INFO mapreduce.Job:  map 55% reduce 0%
18/10/16 12:04:53 INFO mapreduce.Job:  map 56% reduce 0%
18/10/16 12:04:57 INFO mapreduce.Job:  map 57% reduce 0%
18/10/16 12:04:58 INFO mapreduce.Job:  map 58% reduce 0%
18/10/16 12:05:03 INFO mapreduce.Job:  map 59% reduce 0%
18/10/16 12:05:05 INFO mapreduce.Job:  map 60% reduce 0%
18/10/16 12:05:09 INFO mapreduce.Job:  map 61% reduce 0%
18/10/16 12:05:12 INFO mapreduce.Job:  map 62% reduce 0%
18/10/16 12:05:15 INFO mapreduce.Job:  map 63% reduce 0%
18/10/16 12:05:18 INFO mapreduce.Job:  map 64% reduce 0%
18/10/16 12:05:22 INFO mapreduce.Job:  map 65% reduce 0%
18/10/16 12:05:24 INFO mapreduce.Job:  map 66% reduce 0%
18/10/16 12:05:26 INFO mapreduce.Job:  map 67% reduce 0%
18/10/16 12:05:32 INFO mapreduce.Job:  map 68% reduce 0%
18/10/16 12:05:33 INFO mapreduce.Job:  map 69% reduce 0%
18/10/16 12:05:39 INFO mapreduce.Job:  map 70% reduce 0%
18/10/16 12:05:40 INFO mapreduce.Job:  map 71% reduce 0%
18/10/16 12:05:42 INFO mapreduce.Job:  map 72% reduce 0%
18/10/16 12:05:47 INFO mapreduce.Job:  map 73% reduce 0%
18/10/16 12:05:50 INFO mapreduce.Job:  map 74% reduce 0%
18/10/16 12:05:53 INFO mapreduce.Job:  map 75% reduce 0%
18/10/16 12:05:56 INFO mapreduce.Job:  map 76% reduce 0%
18/10/16 12:05:59 INFO mapreduce.Job:  map 77% reduce 0%
18/10/16 12:06:01 INFO mapreduce.Job:  map 78% reduce 0%
18/10/16 12:06:06 INFO mapreduce.Job:  map 79% reduce 0%
18/10/16 12:06:08 INFO mapreduce.Job:  map 80% reduce 0%
18/10/16 12:06:11 INFO mapreduce.Job:  map 81% reduce 0%
18/10/16 12:06:15 INFO mapreduce.Job:  map 82% reduce 0%
18/10/16 12:06:19 INFO mapreduce.Job:  map 83% reduce 0%
18/10/16 12:06:22 INFO mapreduce.Job:  map 84% reduce 0%
18/10/16 12:06:31 INFO mapreduce.Job:  map 85% reduce 0%
18/10/16 12:06:32 INFO mapreduce.Job:  map 85% reduce 4%
18/10/16 12:06:33 INFO mapreduce.Job:  map 85% reduce 6%
18/10/16 12:06:36 INFO mapreduce.Job:  map 85% reduce 12%
18/10/16 12:06:38 INFO mapreduce.Job:  map 85% reduce 15%
18/10/16 12:06:39 INFO mapreduce.Job:  map 85% reduce 16%
18/10/16 12:06:40 INFO mapreduce.Job:  map 86% reduce 16%
18/10/16 12:06:42 INFO mapreduce.Job:  map 86% reduce 17%
18/10/16 12:06:44 INFO mapreduce.Job:  map 86% reduce 18%
18/10/16 12:06:46 INFO mapreduce.Job:  map 87% reduce 18%
18/10/16 12:06:52 INFO mapreduce.Job:  map 88% reduce 18%
18/10/16 12:06:58 INFO mapreduce.Job:  map 89% reduce 18%
18/10/16 12:07:02 INFO mapreduce.Job:  map 89% reduce 19%
18/10/16 12:07:04 INFO mapreduce.Job:  map 90% reduce 19%
18/10/16 12:07:10 INFO mapreduce.Job:  map 91% reduce 19%
18/10/16 12:07:16 INFO mapreduce.Job:  map 92% reduce 19%
18/10/16 12:07:22 INFO mapreduce.Job:  map 93% reduce 19%
18/10/16 12:07:28 INFO mapreduce.Job:  map 94% reduce 19%
18/10/16 12:07:32 INFO mapreduce.Job:  map 94% reduce 20%
18/10/16 12:07:34 INFO mapreduce.Job:  map 95% reduce 20%
18/10/16 12:07:40 INFO mapreduce.Job:  map 96% reduce 20%
18/10/16 12:07:46 INFO mapreduce.Job:  map 97% reduce 20%
18/10/16 12:07:52 INFO mapreduce.Job:  map 98% reduce 20%
18/10/16 12:07:58 INFO mapreduce.Job:  map 99% reduce 20%
18/10/16 12:08:00 INFO mapreduce.Job:  map 99% reduce 21%
18/10/16 12:08:03 INFO mapreduce.Job:  map 100% reduce 21%
18/10/16 12:08:05 INFO mapreduce.Job:  map 100% reduce 24%
18/10/16 12:08:06 INFO mapreduce.Job:  map 100% reduce 28%
18/10/16 12:08:08 INFO mapreduce.Job:  map 100% reduce 36%
18/10/16 12:08:09 INFO mapreduce.Job:  map 100% reduce 41%
18/10/16 12:08:11 INFO mapreduce.Job:  map 100% reduce 42%
18/10/16 12:08:12 INFO mapreduce.Job:  map 100% reduce 43%
18/10/16 12:08:14 INFO mapreduce.Job:  map 100% reduce 45%
18/10/16 12:08:15 INFO mapreduce.Job:  map 100% reduce 46%
18/10/16 12:08:17 INFO mapreduce.Job:  map 100% reduce 47%
18/10/16 12:08:18 INFO mapreduce.Job:  map 100% reduce 49%
18/10/16 12:08:19 INFO mapreduce.Job:  map 100% reduce 53%
18/10/16 12:08:20 INFO mapreduce.Job:  map 100% reduce 55%
18/10/16 12:08:21 INFO mapreduce.Job:  map 100% reduce 59%
18/10/16 12:08:22 INFO mapreduce.Job:  map 100% reduce 62%
18/10/16 12:08:23 INFO mapreduce.Job:  map 100% reduce 63%
18/10/16 12:08:24 INFO mapreduce.Job:  map 100% reduce 65%
18/10/16 12:08:25 INFO mapreduce.Job:  map 100% reduce 70%
18/10/16 12:08:26 INFO mapreduce.Job:  map 100% reduce 71%
18/10/16 12:08:27 INFO mapreduce.Job:  map 100% reduce 73%
18/10/16 12:08:29 INFO mapreduce.Job:  map 100% reduce 77%
18/10/16 12:08:30 INFO mapreduce.Job:  map 100% reduce 79%
18/10/16 12:08:31 INFO mapreduce.Job:  map 100% reduce 81%
18/10/16 12:08:33 INFO mapreduce.Job:  map 100% reduce 85%
18/10/16 12:08:35 INFO mapreduce.Job:  map 100% reduce 90%
18/10/16 12:08:37 INFO mapreduce.Job:  map 100% reduce 92%
18/10/16 12:08:39 INFO mapreduce.Job:  map 100% reduce 94%
18/10/16 12:08:41 INFO mapreduce.Job:  map 100% reduce 96%
18/10/16 12:08:45 INFO mapreduce.Job:  map 100% reduce 98%
18/10/16 12:08:47 INFO mapreduce.Job:  map 100% reduce 100%
18/10/16 12:08:48 INFO mapreduce.Job: Job job_1539689557872_0005 completed successfully
18/10/16 12:08:49 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=4442497880
                FILE: Number of bytes written=8831540399
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000050400
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=924
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=8
                Data-local map tasks=174
                Rack-local map tasks=126
                Total time spent by all maps in occupied slots (ms)=2108378
                Total time spent by all reduces in occupied slots (ms)=771416
                Total time spent by all map tasks (ms)=2108378
                Total time spent by all reduce tasks (ms)=771416
                Total vcore-milliseconds taken by all map tasks=2108378
                Total vcore-milliseconds taken by all reduce tasks=771416
                Total megabyte-milliseconds taken by all map tasks=2158979072
                Total megabyte-milliseconds taken by all reduce tasks=789929984
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4342839501
                Input split bytes=50400
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4342839501
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =2400
                Failed Shuffles=0
                Merged Map outputs=2400
                GC time elapsed (ms)=35301
                CPU time spent (ms)=1407890
                Physical memory (bytes) snapshot=155573485568
                Virtual memory (bytes) snapshot=488216002560
                Total committed heap usage (bytes)=175522185216
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
18/10/16 12:08:49 INFO terasort.TeraSort: done

real    7m8.456s
user    0m9.461s
sys     0m0.627s

