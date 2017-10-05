```
[root@ip-172-31-6-242 bin]# curl -X POST -u admin:admin 'http://13.59.169.94:7180/api/v14/clusters/wjguerrero/services/hive/commands/stop'
{
  "id" : 768,
  "name" : "Stop",
  "startTime" : "2017-10-05T16:25:06.363Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
[root@ip-172-31-6-242 bin]# curl -X POST -u admin:admin 'http://13.59.169.94:7180/api/v14/clusters/wjguerrero/services/hive/commands/start'
{
  "id" : 778,
  "name" : "Start",
  "startTime" : "2017-10-05T16:26:29.209Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
[root@ip-172-31-6-242 bin]# curl -u admin:admin 'http://13.59.169.94:7180/api/v14/clusters/wjguerrero/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-6-242.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-6-242.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_WEBHCATS_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
```
