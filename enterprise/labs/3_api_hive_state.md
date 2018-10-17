curl -X POST  -u VasilyMelnik:cloudera http://35.228.170.128:7180/api/v1/clusters/VasilyMelnik/services/hive/commands/stop
{
  "id" : 1367,
  "name" : "Stop",
  "startTime" : "2018-10-17T10:30:44.743Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}

 curl -X POST  -u VasilyMelnik:cloudera http://35.228.170.128:7180/api/v1/clusters/VasilyMelnik/services/hive/commands/start
{
  "id" : 1371,
  "name" : "Start",
  "startTime" : "2018-10-17T10:31:20.381Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
curl -u VasilyMelnik:cloudera http://35.228.170.128:7180/api/v1/clusters/VasilyMelnik/services/hive 2>&1 | grep serviceState
  "serviceState" : "STARTED",

