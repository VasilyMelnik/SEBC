```
[root@instance-7 ~]# kinit VasilyMelnik
Password for VasilyMelnik@EXAMPLE.COM:
[root@instance-7 ~]# beeline
Beeline version 1.1.0-cdh5.14.4 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/instance-7.europe-north1-a.c.cloudera-218907.internal@EXAMPLE.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/instance-7.europe-north1-a.c.cloudera-218907.internal@EXAMPLE.COM
Connected to: Apache Hive (version 1.1.0-cdh5.14.4)
Driver: Hive JDBC (version 1.1.0-cdh5.14.4)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show databasesl
. . . . . . . . . . . . . . . . . . . .> ;
Error: Error while compiling statement: FAILED: ParseException line 1:5 cannot recognize input near 'show' 'databasesl' '<EOF>' in ddl statement (state=42000,code=40000)
0: jdbc:hive2://localhost:10000/default> show databases;
INFO  : Compiling command(queryId=hive_20181018090303_5434c501-f988-4c60-987c-c0d8abbe26b1): show databases
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:database_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018090303_5434c501-f988-4c60-987c-c0d8abbe26b1); Time taken: 0.528 seconds
INFO  : Executing command(queryId=hive_20181018090303_5434c501-f988-4c60-987c-c0d8abbe26b1): show databases
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018090303_5434c501-f988-4c60-987c-c0d8abbe26b1); Time taken: 0.548 seconds
INFO  : OK
+----------------+--+
| database_name  |
+----------------+--+
| default        |
+----------------+--+
1 row selected (2.456 seconds)
0: jdbc:hive2://localhost:10000/default> show roles;
INFO  : Compiling command(queryId=hive_20181018090404_4717dfef-b485-4bd0-a13f-e993fb2f0df0): show roles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:role, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018090404_4717dfef-b485-4bd0-a13f-e993fb2f0df0); Time taken: 0.11 seconds
INFO  : Executing command(queryId=hive_20181018090404_4717dfef-b485-4bd0-a13f-e993fb2f0df0): show roles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018090404_4717dfef-b485-4bd0-a13f-e993fb2f0df0); Time taken: 0.166 seconds
INFO  : OK
+-------+--+
| role  |
+-------+--+
+-------+--+
No rows selected (0.298 seconds)
0: jdbc:hive2://localhost:10000/default> show current roles;
INFO  : Compiling command(queryId=hive_20181018090404_0317bb4d-89a8-4f55-af68-615df1537e57): show current roles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:role, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018090404_0317bb4d-89a8-4f55-af68-615df1537e57); Time taken: 0.086 seconds
INFO  : Executing command(queryId=hive_20181018090404_0317bb4d-89a8-4f55-af68-615df1537e57): show current roles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018090404_0317bb4d-89a8-4f55-af68-615df1537e57); Time taken: 0.01 seconds
INFO  : OK
+-------+--+
| role  |
+-------+--+
+-------+--+
No rows selected (0.118 seconds)
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20181018090505_0cd43b58-37ce-4067-8553-d96edc1992fa): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018090505_0cd43b58-37ce-4067-8553-d96edc1992fa); Time taken: 0.111 seconds
INFO  : Executing command(queryId=hive_20181018090505_0cd43b58-37ce-4067-8553-d96edc1992fa): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018090505_0cd43b58-37ce-4067-8553-d96edc1992fa); Time taken: 0.164 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.299 seconds)

[root@instance-7 ~]# kinit george
Password for george@EXAMPLE.COM:
[root@instance-7 ~]# beeline
Beeline version 1.1.0-cdh5.14.4 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/instance-7.europe-north1-a.c.cloudera-218907.internal@EXAMPLE.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/instance-7.europe-north1-a.c.cloudera-218907.internal@EXAMPLE.COM
Connected to: Apache Hive (version 1.1.0-cdh5.14.4)
Driver: Hive JDBC (version 1.1.0-cdh5.14.4)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show current roles;
INFO  : Compiling command(queryId=hive_20181018092828_bfc1011d-0c97-4d2c-88c2-b62d054261ed): show current roles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:role, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018092828_bfc1011d-0c97-4d2c-88c2-b62d054261ed); Time taken: 0.093 seconds
INFO  : Executing command(queryId=hive_20181018092828_bfc1011d-0c97-4d2c-88c2-b62d054261ed): show current roles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018092828_bfc1011d-0c97-4d2c-88c2-b62d054261ed); Time taken: 0.02 seconds
INFO  : OK
+--------+--+
|  role  |
+--------+--+
| reads  |
+--------+--+
1 row selected (0.223 seconds)
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20181018092828_ca2e6bbb-4154-491d-8a37-1a94d6dc2b33): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018092828_ca2e6bbb-4154-491d-8a37-1a94d6dc2b33); Time taken: 0.081 seconds
INFO  : Executing command(queryId=hive_20181018092828_ca2e6bbb-4154-491d-8a37-1a94d6dc2b33): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018092828_ca2e6bbb-4154-491d-8a37-1a94d6dc2b33); Time taken: 0.185 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.293 seconds)
0: jdbc:hive2://localhost:10000/default> !q
Closing: 0: jdbc:hive2://localhost:10000/default;principal=hive/instance-7.europe-north1-a.c.cloudera-218907.internal@EXAMPLE.COM
[root@instance-7 ~]# kinit ferdinand
Password for ferdinand@EXAMPLE.COM:
[root@instance-7 ~]# beeline
Beeline version 1.1.0-cdh5.14.4 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/instance-7.europe-north1-a.c.cloudera-218907.internal@EXAMPLE.COM
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/instance-7.europe-north1-a.c.cloudera-218907.internal@EXAMPLE.COM
Connected to: Apache Hive (version 1.1.0-cdh5.14.4)
Driver: Hive JDBC (version 1.1.0-cdh5.14.4)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show current roles;
INFO  : Compiling command(queryId=hive_20181018093030_eda75ffb-6ff7-427e-a7f4-65893a99ecf7): show current roles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:role, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018093030_eda75ffb-6ff7-427e-a7f4-65893a99ecf7); Time taken: 0.089 seconds
INFO  : Executing command(queryId=hive_20181018093030_eda75ffb-6ff7-427e-a7f4-65893a99ecf7): show current roles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018093030_eda75ffb-6ff7-427e-a7f4-65893a99ecf7); Time taken: 0.021 seconds
INFO  : OK
+---------+--+
|  role   |
+---------+--+
| writes  |
+---------+--+
1 row selected (0.23 seconds)
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20181018093030_07e2d479-d3af-435e-a885-20fb1d03aad0): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018093030_07e2d479-d3af-435e-a885-20fb1d03aad0); Time taken: 0.104 seconds
INFO  : Executing command(queryId=hive_20181018093030_07e2d479-d3af-435e-a885-20fb1d03aad0): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018093030_07e2d479-d3af-435e-a885-20fb1d03aad0); Time taken: 0.209 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.351 seconds)
0: jdbc:hive2://localhost:10000/default>


```
