curl -u VasilyMelnik:cloudera http://35.228.170.128:7180/api/version
v19

curl -u VasilyMelnik:cloudera http://35.228.170.128:7180/api/v19/cm/version
{
  "version" : "5.15.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20180731-0834",
  "gitHash" : "6e046fd999fd99e7e12299386ba69b23afa43c60",
  "snapshot" : false
}

curl -u VasilyMelnik:cloudera http://35.228.170.128:7180/api/v19/users
{
  "items" : [ {
    "name" : "VasilyMelnik",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}

curl -u VasilyMelnik:cloudera http://35.228.170.128:7180/api/v19/cm/scmDbInfo
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}