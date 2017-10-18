[root@ip-172-31-25-67 ~]# curl -X POST -u Maurizio845:cloudera http://ec2-18-194-169-169.eu-central-1.compute.amazonaws.com:7180/api/v12/clusters/Maurizio845/services/hive/commands/stop
{
  "id" : 410,
  "name" : "Stop",
  "startTime" : "2017-10-18T12:24:32.905Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}



[root@ip-172-31-25-67 ~]# curl -u Maurizio845:cloudera http://ec2-18-194-169-169.eu-central-1.compute.amazonaws.com:7180/api/v12/clusters/Maurizio845/services/hive
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-29-107.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-29-107.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STOPPED",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "STOPPED"
}


[root@ip-172-31-25-67 ~]# curl -X POST -u Maurizio845:cloudera http://ec2-18-194-169-169.eu-central-1.compute.amazonaws.com:7180/api/v12/clusters/Maurizio845/services/hive/comands/start
{
  "id" : 413,
  "name" : "Start",
  "startTime" : "2017-10-18T12:25:10.654Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}


[root@ip-172-31-25-67 ~]# curl u Maurizio845:cloudera http://ec2-18-194-169-169.eu-central-1.compute.amazonaws.com:7180/api/v12/clusters/Maurizio845/services/hive             {
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-29-107.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-29-107.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
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
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
