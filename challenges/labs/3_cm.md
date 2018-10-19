# HDFS list

	[root@instance-13 ~]# sudo -u hdfs hadoop fs -ls /user
	Found 6 items
	drwxr-xr-x   - fullerton hotels          0 2018-10-19 08:13 /user/fullerton
	drwxrwxrwx   - mapred    hadoop          0 2018-10-19 08:09 /user/history
	drwxrwxr-t   - hive      hive            0 2018-10-19 08:10 /user/hive
	drwxrwxr-x   - hue       hue             0 2018-10-19 08:10 /user/hue
	drwxrwxr-x   - oozie     oozie           0 2018-10-19 08:11 /user/oozie
	drwxr-xr-x   - raffles   shops           0 2018-10-19 08:17 /user/raffles
	
# API output

	{
	  "items" : [ {
		"hostId" : "dde42826-b9e6-483d-a75f-5805fac9669c",
		"ipAddress" : "10.132.0.2",
		"hostname" : "instance-13.europe-west1-b.c.cloudera-218907.internal",
		"rackId" : "/default",
		"hostUrl" : "http://instance-13.europe-west1-b.c.cloudera-218907.internal:7180/cmf/hostRedirect/dde42826-b9e6-483d-a75f-5805fac9669c",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 2,
		"totalPhysMemBytes" : 15600521216
	  }, {
		"hostId" : "a3ff19e8-a438-41bb-b03e-cbeba974237f",
		"ipAddress" : "10.132.0.3",
		"hostname" : "instance-14.europe-west1-b.c.cloudera-218907.internal",
		"rackId" : "/default",
		"hostUrl" : "http://instance-13.europe-west1-b.c.cloudera-218907.internal:7180/cmf/hostRedirect/a3ff19e8-a438-41bb-b03e-cbeba974237f",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 2,
		"totalPhysMemBytes" : 15600521216
	  }, {
		"hostId" : "e9932543-7215-4b13-9d49-714165dfe2f0",
		"ipAddress" : "10.132.0.4",
		"hostname" : "instance-15.europe-west1-b.c.cloudera-218907.internal",
		"rackId" : "/default",
		"hostUrl" : "http://instance-13.europe-west1-b.c.cloudera-218907.internal:7180/cmf/hostRedirect/e9932543-7215-4b13-9d49-714165dfe2f0",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 2,
		"totalPhysMemBytes" : 15600521216
	  }, {
		"hostId" : "408e11c8-7c7e-4aa1-a901-0f98f2819f81",
		"ipAddress" : "10.132.0.5",
		"hostname" : "instance-16.europe-west1-b.c.cloudera-218907.internal",
		"rackId" : "/default",
		"hostUrl" : "http://instance-13.europe-west1-b.c.cloudera-218907.internal:7180/cmf/hostRedirect/408e11c8-7c7e-4aa1-a901-0f98f2819f81",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 2,
		"totalPhysMemBytes" : 15600521216
	  }, {
		"hostId" : "26ae1cbe-501c-49fb-88ac-143eb98f1b66",
		"ipAddress" : "10.132.0.6",
		"hostname" : "instance-17.europe-west1-b.c.cloudera-218907.internal",
		"rackId" : "/default",
		"hostUrl" : "http://instance-13.europe-west1-b.c.cloudera-218907.internal:7180/cmf/hostRedirect/26ae1cbe-501c-49fb-88ac-143eb98f1b66",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 2,
		"totalPhysMemBytes" : 15600513024
	  } ]
	}