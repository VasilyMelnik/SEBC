# Database creation

	CREATE DATABASE scm DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
	CREATE DATABASE rman DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
	CREATE DATABASE hue DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
	CREATE DATABASE hive DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
	CREATE DATABASE sentry DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
	CREATE DATABASE oozie DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;

	GRANT ALL ON scm.* TO 'scm'@'%' IDENTIFIED BY '123456';
	GRANT ALL ON rman.* TO 'rman'@'%' IDENTIFIED BY '123456';
	GRANT ALL ON hue.* TO 'hue'@'%' IDENTIFIED BY '123456';
	GRANT ALL ON hive.* TO 'hive'@'%' IDENTIFIED BY '123456';
	GRANT ALL ON sentry.* TO 'sentry'@'%' IDENTIFIED BY '123456';
	GRANT ALL ON oozie.* TO 'oozie'@'%' IDENTIFIED BY '123456';

	SET PASSWORD FOR 'scm'@'%' = PASSWORD('123456');
	SET PASSWORD FOR 'rman'@'%' = PASSWORD('123456');
	SET PASSWORD FOR 'hue'@'%' = PASSWORD('123456');
	SET PASSWORD FOR 'hive'@'%' = PASSWORD('123456');
	SET PASSWORD FOR 'sentry'@'%' = PASSWORD('123456');
	SET PASSWORD FOR 'oozie'@'%' = PASSWORD('123456');

	
# Instance and database version 

	[root@instance-14 ~]# mysql --version
	mysql  Ver 15.1 Distrib 5.5.60-MariaDB, for Linux (x86_64) using readline 5.1

# Show databases


	MariaDB [(none)]> show databases;
	+--------------------+
	| Database           |
	+--------------------+
	| information_schema |
	| hive               |
	| hue                |
	| mysql              |
	| oozie              |
	| performance_schema |
	| rman               |
	| scm                |
	| sentry             |
	+--------------------+
	9 rows in set (0.00 sec)
