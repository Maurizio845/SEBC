```
#### hdfs file system
[root@ip-172-31-39-254 tmp]# hdfs dfs -ls /user
Found 7 items
drwxr-xr-x   - ernest  ernest              0 2017-10-20 09:29 /user/ernest
drwxr-xr-x   - hdfs    supergroup          0 2017-10-20 09:25 /user/hdfs
drwxrwxrwx   - mapred  hadoop              0 2017-10-20 09:15 /user/history
drwxrwxr-t   - hive    hive                0 2017-10-20 09:16 /user/hive
drwxrwxr-x   - hue     hue                 0 2017-10-20 09:16 /user/hue
drwxrwxr-x   - oozie   oozie               0 2017-10-20 09:17 /user/oozie
drwxr-xr-x   - siwicki siwicki             0 2017-10-20 09:29 /user/siwicki



#### Hosts
[root@ip-172-31-39-254 tmp]# curl -u admin:admin http://ec2-52-59-18-215.eu-central-1.compute.amazonaws.com:7180/api/v14/hosts
{
  "items" : [ {
    "hostId" : "i-0658502d3132c5c60",
    "ipAddress" : "172.31.34.43",
    "hostname" : "ip-172-31-34-43.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-34-43.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-0658502d3132c5c60",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600140288
  }, {
    "hostId" : "i-0fc635ae8d62dd70e",
    "ipAddress" : "172.31.39.254",
    "hostname" : "ip-172-31-39-254.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-34-43.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-0fc635ae8d62dd70e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600140288
  }, {
    "hostId" : "i-075152213128d6ab0",
    "ipAddress" : "172.31.41.224",
    "hostname" : "ip-172-31-41-224.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-34-43.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-075152213128d6ab0",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600140288
  }, {
    "hostId" : "i-0812be841e301bb56",
    "ipAddress" : "172.31.41.79",
    "hostname" : "ip-172-31-41-79.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-34-43.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-0812be841e301bb56",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600140288
  }, {
    "hostId" : "i-0682f439a371a4df5",
    "ipAddress" : "172.31.46.9",
    "hostname" : "ip-172-31-46-9.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-34-43.eu-central-1.compute.internal:7180/cmf/hostRedirect/i-0682f439a371a4df5",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600140288
  } ]
}


```
