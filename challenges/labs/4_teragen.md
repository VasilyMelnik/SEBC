# Teragen

	time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=6 \
	-Ddfs.block.size=32m -Ddfs.replication=1 51200000 /user/raffles/tgen512/

# Time

real    0m33.748s
user    0m5.211s
sys     0m0.364s

# LS

	[raffles@instance-13 root]$ hdfs dfs -ls /user/raffles/tgen512
	Found 7 items
	-rw-r--r--   1 raffles shops          0 2018-10-19 08:31 /user/raffles/tgen512/_SUCCESS
	-rw-r--r--   1 raffles shops  853333400 2018-10-19 08:31 /user/raffles/tgen512/part-m-00000
	-rw-r--r--   1 raffles shops  853333300 2018-10-19 08:31 /user/raffles/tgen512/part-m-00001
	-rw-r--r--   1 raffles shops  853333300 2018-10-19 08:31 /user/raffles/tgen512/part-m-00002
	-rw-r--r--   1 raffles shops  853333400 2018-10-19 08:31 /user/raffles/tgen512/part-m-00003
	-rw-r--r--   1 raffles shops  853333300 2018-10-19 08:31 /user/raffles/tgen512/part-m-00004
	-rw-r--r--   1 raffles shops  853333300 2018-10-19 08:31 /user/raffles/tgen512/part-m-00005



# Blocks number

	[root@instance-13 ~]# sudo -u hdfs hdfs fsck /user/raffles/tgen512  -blocks
	Connecting to namenode via http://instance-13.europe-west1-b.c.cloudera-218907.internal:50070/fsck?ugi=hdfs&blocks=1&path=%2Fuser%2Fraffles%2Ftgen512
	FSCK started by hdfs (auth:SIMPLE) from /10.132.0.2 for path /user/raffles/tgen512 at Fri Oct 19 08:36:31 UTC 2018
	.......Status: HEALTHY
	 Total size:    5120000000 B
	 Total dirs:    1
	 Total files:   7
	 Total symlinks:                0
	 Total blocks (validated):      156 (avg. block size 32820512 B)
	 Minimally replicated blocks:   156 (100.0 %)
	 Over-replicated blocks:        0 (0.0 %)
	 Under-replicated blocks:       0 (0.0 %)
	 Mis-replicated blocks:         0 (0.0 %)
	 Default replication factor:    3
	 Average block replication:     1.0
	 Corrupt blocks:                0
	 Missing replicas:              0 (0.0 %)
	 Number of data-nodes:          3
	 Number of racks:               1
	FSCK ended at Fri Oct 19 08:36:31 UTC 2018 in 4 milliseconds


	The filesystem under path '/user/raffles/tgen512' is HEALTHY
