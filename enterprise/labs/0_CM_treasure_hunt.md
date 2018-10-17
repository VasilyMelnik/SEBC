* What is ubertask optimization?
Whether to enable ubertask optimization, which runs "sufficiently small" 
jobs sequentially within a single JVM. 
"Small" is defined by the mapreduce.job.ubertask.maxmaps, 
mapreduce.job.ubertask.maxreduces, 
and mapreduce.job.ubertask.maxbytes settings.

* Where in CM is the Kerberos Security Realm value displayed?
In Administration->Settings

*Which CDH service(s) host a property for enabling Kerberos authentication?

Zookeeper
YARN 
HDFS 
Hue (principal)
Ooozie (principal)
Cloudera Management Service (Activity monitor, Report manager, Navigator, Telemetry princioals)

* How do you upgrade the CM agents?
In Administration->Settings we can enable TLS Encryption
In Hosts->Configuration we edit Agent configuratiion snippet and set monitoring thresholds
To upgrade packages we can use wizard 
http://<CM host and port>/cmf/upgrade

* Give the tsquery statement used to chart Hue's CPU utilization?
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME

*Name all the roles that make up the Hive service
Hive Metastore Server
WebHCat Server 
HiveServer2
Gateway

*What steps must be completed before integrating Cloudera Manager with Kerberos?

- Kerberos client OS-specific packages must be installed on all cluster hosts and client hosts that will authenticate using Kerberos
- Set up a working KDC
- Configure the KDC to allow renewable tickets with non-zero ticket lifetimes.
- Create an account for Cloudera Manager that has the permissions to create other accounts in the KDC. 

