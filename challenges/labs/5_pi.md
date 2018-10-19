# Pi command

	kinit fullerton
	Password for fullerton@VASILYMENIK.SG:
	[root@instance-15 ~]# hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar pi 16 1000
	Number of Maps  = 16
	Samples per Map = 1000
	Wrote input for Map #0
	Wrote input for Map #1
	Wrote input for Map #2
	Wrote input for Map #3
	Wrote input for Map #4
	Wrote input for Map #5
	Wrote input for Map #6
	Wrote input for Map #7
	Wrote input for Map #8
	Wrote input for Map #9
	Wrote input for Map #10
	Wrote input for Map #11
	Wrote input for Map #12
	Wrote input for Map #13
	Wrote input for Map #14
	Wrote input for Map #15
	Starting Job
	18/10/19 09:16:59 INFO client.RMProxy: Connecting to ResourceManager at instance-14.europe-west1-b.c.cloudera-218907.internal/10.132.0.3:8032
	18/10/19 09:16:59 INFO hdfs.DFSClient: Created token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@VASILYMENIK.SG, renewer=yarn, realUser=, issueDate=1539940619423, maxDate=1540545419423, sequenceNumber=2, masterKeyId=2 on 10.132.0.2:8020
	18/10/19 09:16:59 INFO security.TokenCache: Got dt for hdfs://instance-13.europe-west1-b.c.cloudera-218907.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.132.0.2:8020, Ident: (token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@VASILYMENIK.SG, renewer=yarn, realUser=, issueDate=1539940619423, maxDate=1540545419423, sequenceNumber=2, masterKeyId=2)
	18/10/19 09:16:59 INFO input.FileInputFormat: Total input paths to process : 16
	18/10/19 09:16:59 INFO mapreduce.JobSubmitter: number of splits:16
	18/10/19 09:17:00 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539940128732_0002
	18/10/19 09:17:00 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.132.0.2:8020, Ident: (token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@VASILYMENIK.SG, renewer=yarn, realUser=, issueDate=1539940619423, maxDate=1540545419423, sequenceNumber=2, masterKeyId=2)
	18/10/19 09:17:01 INFO impl.YarnClientImpl: Submitted application application_1539940128732_0002
	18/10/19 09:17:01 INFO mapreduce.Job: The url to track the job: http://instance-14.europe-west1-b.c.cloudera-218907.internal:8088/proxy/application_1539940128732_0002/
	18/10/19 09:17:01 INFO mapreduce.Job: Running job: job_1539940128732_0002
	18/10/19 09:17:21 INFO mapreduce.Job: Job job_1539940128732_0002 running in uber mode : false
	18/10/19 09:17:21 INFO mapreduce.Job:  map 0% reduce 0%
	18/10/19 09:17:28 INFO mapreduce.Job:  map 13% reduce 0%
	18/10/19 09:17:32 INFO mapreduce.Job:  map 19% reduce 0%
	18/10/19 09:17:34 INFO mapreduce.Job:  map 38% reduce 0%
	18/10/19 09:17:35 INFO mapreduce.Job:  map 44% reduce 0%
	18/10/19 09:17:39 INFO mapreduce.Job:  map 56% reduce 0%
	18/10/19 09:17:41 INFO mapreduce.Job:  map 63% reduce 0%
	18/10/19 09:17:42 INFO mapreduce.Job:  map 69% reduce 0%
	18/10/19 09:17:43 INFO mapreduce.Job:  map 75% reduce 0%
	18/10/19 09:17:44 INFO mapreduce.Job:  map 81% reduce 0%
	18/10/19 09:17:45 INFO mapreduce.Job:  map 88% reduce 0%
	18/10/19 09:17:47 INFO mapreduce.Job:  map 94% reduce 0%
	18/10/19 09:17:48 INFO mapreduce.Job:  map 100% reduce 0%
	18/10/19 09:17:50 INFO mapreduce.Job:  map 100% reduce 100%
	18/10/19 09:17:51 INFO mapreduce.Job: Job job_1539940128732_0002 completed successfully
	18/10/19 09:17:52 INFO mapreduce.Job: Counters: 49
			File System Counters
					FILE: Number of bytes read=135
					FILE: Number of bytes written=2573189
					FILE: Number of read operations=0
					FILE: Number of large read operations=0
					FILE: Number of write operations=0
					HDFS: Number of bytes read=5030
					HDFS: Number of bytes written=215
					HDFS: Number of read operations=67
					HDFS: Number of large read operations=0
					HDFS: Number of write operations=3
			Job Counters
					Launched map tasks=16
					Launched reduce tasks=1
					Data-local map tasks=16
					Total time spent by all maps in occupied slots (ms)=78611
					Total time spent by all reduces in occupied slots (ms)=3769
					Total time spent by all map tasks (ms)=78611
					Total time spent by all reduce tasks (ms)=3769
					Total vcore-milliseconds taken by all map tasks=78611
					Total vcore-milliseconds taken by all reduce tasks=3769
					Total megabyte-milliseconds taken by all map tasks=80497664
					Total megabyte-milliseconds taken by all reduce tasks=3859456
			Map-Reduce Framework
					Map input records=16
					Map output records=32
					Map output bytes=288
					Map output materialized bytes=544
					Input split bytes=3142
					Combine input records=0
					Combine output records=0
					Reduce input groups=2
					Reduce shuffle bytes=544
					Reduce input records=32
					Reduce output records=0
					Spilled Records=64
					Shuffled Maps =16
					Failed Shuffles=0
					Merged Map outputs=16
					GC time elapsed (ms)=594
					CPU time spent (ms)=13110
					Physical memory (bytes) snapshot=7912333312
					Virtual memory (bytes) snapshot=26987540480
					Total committed heap usage (bytes)=8953266176
			Shuffle Errors
					BAD_ID=0
					CONNECTION=0
					IO_ERROR=0
					WRONG_LENGTH=0
					WRONG_MAP=0
					WRONG_REDUCE=0
			File Input Format Counters
					Bytes Read=1888
			File Output Format Counters
					Bytes Written=97
	Job Finished in 53.226 seconds
	Estimated value of Pi is 3.14250000000000000000
