# Trerasort command

	[root@instance-14 ~]# kinit raffles
	Password for raffles@VASILYMENIK.SG:
	[root@instance-14 ~]# time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=4\
	>  -Ddfs.block.size=32m -Ddfs.replication=1 /user/raffles/tgen512/  /user/raffles/tsort512_result/
	18/10/19 09:14:17 INFO terasort.TeraSort: starting
	18/10/19 09:14:19 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@VASILYMENIK.SG, renewer=yarn, realUser=, issueDate=1539940458993, maxDate=1540545258993, sequenceNumber=1, masterKeyId=2 on 10.132.0.2:8020
	18/10/19 09:14:19 INFO security.TokenCache: Got dt for hdfs://instance-13.europe-west1-b.c.cloudera-218907.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.132.0.2:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@VASILYMENIK.SG, renewer=yarn, realUser=, issueDate=1539940458993, maxDate=1540545258993, sequenceNumber=1, masterKeyId=2)
	18/10/19 09:14:19 INFO input.FileInputFormat: Total input paths to process : 6
	Spent 421ms computing base-splits.
	Spent 3ms computing TeraScheduler splits.
	Computing input splits took 425ms
	Sampling 10 splits of 156
	Making 6 from 100000 sampled records
	Computing parititions took 984ms
	Spent 1412ms computing partitions.
	18/10/19 09:14:20 INFO client.RMProxy: Connecting to ResourceManager at instance-14.europe-west1-b.c.cloudera-218907.internal/10.132.0.3:8032
	18/10/19 09:14:20 INFO mapreduce.JobSubmitter: number of splits:156
	18/10/19 09:14:20 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
	18/10/19 09:14:20 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539940128732_0001
	18/10/19 09:14:20 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.132.0.2:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@VASILYMENIK.SG, renewer=yarn, realUser=, issueDate=1539940458993, maxDate=1540545258993, sequenceNumber=1, masterKeyId=2)
	18/10/19 09:14:21 INFO impl.YarnClientImpl: Submitted application application_1539940128732_0001
	18/10/19 09:14:21 INFO mapreduce.Job: The url to track the job: http://instance-14.europe-west1-b.c.cloudera-218907.internal:8088/proxy/application_1539940128732_0001/
	18/10/19 09:14:21 INFO mapreduce.Job: Running job: job_1539940128732_0001
	18/10/19 09:14:30 INFO mapreduce.Job: Job job_1539940128732_0001 running in uber mode : false
	18/10/19 09:14:30 INFO mapreduce.Job:  map 0% reduce 0%
	18/10/19 09:14:41 INFO mapreduce.Job:  map 1% reduce 0%
	18/10/19 09:14:42 INFO mapreduce.Job:  map 2% reduce 0%
	18/10/19 09:14:47 INFO mapreduce.Job:  map 4% reduce 0%
	18/10/19 09:14:50 INFO mapreduce.Job:  map 6% reduce 0%
	18/10/19 09:14:51 INFO mapreduce.Job:  map 8% reduce 0%
	18/10/19 09:14:57 INFO mapreduce.Job:  map 10% reduce 0%
	18/10/19 09:14:59 INFO mapreduce.Job:  map 12% reduce 0%
	18/10/19 09:15:02 INFO mapreduce.Job:  map 13% reduce 0%
	18/10/19 09:15:03 INFO mapreduce.Job:  map 15% reduce 0%
	18/10/19 09:15:07 INFO mapreduce.Job:  map 17% reduce 0%
	18/10/19 09:15:08 INFO mapreduce.Job:  map 18% reduce 0%
	18/10/19 09:15:09 INFO mapreduce.Job:  map 19% reduce 0%
	18/10/19 09:15:15 INFO mapreduce.Job:  map 21% reduce 0%
	18/10/19 09:15:16 INFO mapreduce.Job:  map 22% reduce 0%
	18/10/19 09:15:17 INFO mapreduce.Job:  map 25% reduce 0%
	18/10/19 09:15:22 INFO mapreduce.Job:  map 26% reduce 0%
	18/10/19 09:15:25 INFO mapreduce.Job:  map 27% reduce 0%
	18/10/19 09:15:27 INFO mapreduce.Job:  map 29% reduce 0%
	18/10/19 09:15:29 INFO mapreduce.Job:  map 30% reduce 0%
	18/10/19 09:15:30 INFO mapreduce.Job:  map 32% reduce 0%
	18/10/19 09:15:34 INFO mapreduce.Job:  map 33% reduce 0%
	18/10/19 09:15:37 INFO mapreduce.Job:  map 35% reduce 0%
	18/10/19 09:15:38 INFO mapreduce.Job:  map 36% reduce 0%
	18/10/19 09:15:42 INFO mapreduce.Job:  map 37% reduce 0%
	18/10/19 09:15:43 INFO mapreduce.Job:  map 39% reduce 0%
	18/10/19 09:15:44 INFO mapreduce.Job:  map 40% reduce 0%
	18/10/19 09:15:47 INFO mapreduce.Job:  map 42% reduce 0%
	18/10/19 09:15:52 INFO mapreduce.Job:  map 44% reduce 0%
	18/10/19 09:15:55 INFO mapreduce.Job:  map 45% reduce 0%
	18/10/19 09:15:56 INFO mapreduce.Job:  map 46% reduce 0%
	18/10/19 09:15:57 INFO mapreduce.Job:  map 47% reduce 0%
	18/10/19 09:15:58 INFO mapreduce.Job:  map 49% reduce 0%
	18/10/19 09:16:01 INFO mapreduce.Job:  map 50% reduce 0%
	18/10/19 09:16:03 INFO mapreduce.Job:  map 51% reduce 0%
	18/10/19 09:16:07 INFO mapreduce.Job:  map 52% reduce 0%
	18/10/19 09:16:08 INFO mapreduce.Job:  map 54% reduce 0%
	18/10/19 09:16:09 INFO mapreduce.Job:  map 55% reduce 0%
	18/10/19 09:16:10 INFO mapreduce.Job:  map 56% reduce 0%
	18/10/19 09:16:11 INFO mapreduce.Job:  map 57% reduce 0%
	18/10/19 09:16:18 INFO mapreduce.Job:  map 59% reduce 0%
	18/10/19 09:16:19 INFO mapreduce.Job:  map 62% reduce 0%
	18/10/19 09:16:21 INFO mapreduce.Job:  map 63% reduce 0%
	18/10/19 09:16:28 INFO mapreduce.Job:  map 67% reduce 0%
	18/10/19 09:16:31 INFO mapreduce.Job:  map 68% reduce 0%
	18/10/19 09:16:32 INFO mapreduce.Job:  map 69% reduce 0%
	18/10/19 09:16:33 INFO mapreduce.Job:  map 70% reduce 0%
	18/10/19 09:16:37 INFO mapreduce.Job:  map 72% reduce 0%
	18/10/19 09:16:38 INFO mapreduce.Job:  map 74% reduce 0%
	18/10/19 09:16:44 INFO mapreduce.Job:  map 75% reduce 0%
	18/10/19 09:16:45 INFO mapreduce.Job:  map 76% reduce 0%
	18/10/19 09:16:46 INFO mapreduce.Job:  map 77% reduce 0%
	18/10/19 09:16:47 INFO mapreduce.Job:  map 79% reduce 0%
	18/10/19 09:16:48 INFO mapreduce.Job:  map 80% reduce 0%
	18/10/19 09:16:55 INFO mapreduce.Job:  map 82% reduce 0%
	18/10/19 09:16:56 INFO mapreduce.Job:  map 84% reduce 0%
	18/10/19 09:16:57 INFO mapreduce.Job:  map 85% reduce 0%
	18/10/19 09:16:58 INFO mapreduce.Job:  map 86% reduce 0%
	18/10/19 09:16:59 INFO mapreduce.Job:  map 87% reduce 0%
	18/10/19 09:17:09 INFO mapreduce.Job:  map 88% reduce 0%
	18/10/19 09:17:10 INFO mapreduce.Job:  map 89% reduce 0%
	18/10/19 09:17:11 INFO mapreduce.Job:  map 90% reduce 0%
	18/10/19 09:17:13 INFO mapreduce.Job:  map 90% reduce 5%
	18/10/19 09:17:14 INFO mapreduce.Job:  map 90% reduce 15%
	18/10/19 09:17:16 INFO mapreduce.Job:  map 91% reduce 15%
	18/10/19 09:17:17 INFO mapreduce.Job:  map 92% reduce 25%
	18/10/19 09:17:21 INFO mapreduce.Job:  map 93% reduce 25%
	18/10/19 09:17:23 INFO mapreduce.Job:  map 94% reduce 26%
	18/10/19 09:17:28 INFO mapreduce.Job:  map 95% reduce 26%
	18/10/19 09:17:29 INFO mapreduce.Job:  map 95% reduce 10%
	18/10/19 09:17:32 INFO mapreduce.Job:  map 95% reduce 11%
	18/10/19 09:17:37 INFO mapreduce.Job:  map 96% reduce 11%
	18/10/19 09:17:39 INFO mapreduce.Job:  map 97% reduce 11%
	18/10/19 09:17:48 INFO mapreduce.Job:  map 98% reduce 11%
	18/10/19 09:17:49 INFO mapreduce.Job:  map 99% reduce 11%
	18/10/19 09:17:52 INFO mapreduce.Job:  map 100% reduce 11%
	18/10/19 09:17:56 INFO mapreduce.Job:  map 100% reduce 17%
	18/10/19 09:17:59 INFO mapreduce.Job:  map 100% reduce 23%
	18/10/19 09:18:02 INFO mapreduce.Job:  map 100% reduce 27%
	18/10/19 09:18:04 INFO mapreduce.Job:  map 100% reduce 39%
	18/10/19 09:18:05 INFO mapreduce.Job:  map 100% reduce 47%
	18/10/19 09:18:07 INFO mapreduce.Job:  map 100% reduce 64%
	18/10/19 09:18:11 INFO mapreduce.Job:  map 100% reduce 66%
	18/10/19 09:18:12 INFO mapreduce.Job:  map 100% reduce 69%
	18/10/19 09:18:13 INFO mapreduce.Job:  map 100% reduce 74%
	18/10/19 09:18:14 INFO mapreduce.Job:  map 100% reduce 83%
	18/10/19 09:18:17 INFO mapreduce.Job:  map 100% reduce 86%
	18/10/19 09:18:18 INFO mapreduce.Job:  map 100% reduce 89%
	18/10/19 09:18:19 INFO mapreduce.Job:  map 100% reduce 92%
	18/10/19 09:18:20 INFO mapreduce.Job:  map 100% reduce 95%
	18/10/19 09:18:24 INFO mapreduce.Job:  map 100% reduce 100%
	18/10/19 09:18:25 INFO mapreduce.Job: Job job_1539940128732_0001 completed successfully
	18/10/19 09:18:27 INFO mapreduce.Job: Counters: 51
			File System Counters
					FILE: Number of bytes read=2279331943
					FILE: Number of bytes written=4527484191
					FILE: Number of read operations=0
					FILE: Number of large read operations=0
					FILE: Number of write operations=0
					HDFS: Number of bytes read=5120025584
					HDFS: Number of bytes written=5120000000
					HDFS: Number of read operations=486
					HDFS: Number of large read operations=0
					HDFS: Number of write operations=12
			Job Counters
					Killed reduce tasks=3
					Launched map tasks=156
					Launched reduce tasks=9
					Data-local map tasks=153
					Rack-local map tasks=3
					Total time spent by all maps in occupied slots (ms)=1453592
					Total time spent by all reduces in occupied slots (ms)=364255
					Total time spent by all map tasks (ms)=1453592
					Total time spent by all reduce tasks (ms)=364255
					Total vcore-milliseconds taken by all map tasks=1453592
					Total vcore-milliseconds taken by all reduce tasks=364255
					Total megabyte-milliseconds taken by all map tasks=1488478208
					Total megabyte-milliseconds taken by all reduce tasks=372997120
			Map-Reduce Framework
					Map input records=51200000
					Map output records=51200000
					Map output bytes=5222400000
					Map output materialized bytes=2223494908
					Input split bytes=25584
					Combine input records=0
					Combine output records=0
					Reduce input groups=51200000
					Reduce shuffle bytes=2223494908
					Reduce input records=51200000
					Reduce output records=51200000
					Spilled Records=102400000
					Shuffled Maps =936
					Failed Shuffles=0
					Merged Map outputs=936
					GC time elapsed (ms)=23593
					CPU time spent (ms)=776590
					Physical memory (bytes) snapshot=83273965568
					Virtual memory (bytes) snapshot=256986451968
					Total committed heap usage (bytes)=91993669632
			Shuffle Errors
					BAD_ID=0
					CONNECTION=0
					IO_ERROR=0
					WRONG_LENGTH=0
					WRONG_MAP=0
					WRONG_REDUCE=0
			File Input Format Counters
					Bytes Read=5120000000
			File Output Format Counters
					Bytes Written=5120000000
	18/10/19 09:18:27 INFO terasort.TeraSort: done

	real    4m10.992s
	user    0m9.665s
	sys     0m0.674s


