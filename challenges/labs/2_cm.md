# yum

	[root@instance-13 ~]# ls /etc/yum.repos.d
	cloudera-manager.repo  epel.repo  epel-testing.repo  google-cloud.repo  rh-cloud.repo

# Prepare database

	[root@instance-13 ~]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h instance-14 scm scm 123456
	JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera/
	Verifying that we can write to /etc/cloudera-scm-server
	Creating SCM configuration file in /etc/cloudera-scm-server
	Executing:  /usr/java/jdk1.7.0_67-cloudera//bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/java/postgresql-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
	[                          main] DbCommandExecutor              INFO  Successfully connected to database.
	All done, your SCM database is configured correctly!
