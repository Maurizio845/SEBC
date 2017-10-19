```

[root@ip-172-31-25-67 tmp]# curl -u Maurizio845:cloudera http://ec2-18-194-169-169.eu-central-1.compute.amazonaws.com:7180/api/version
v14


[root@ip-172-31-25-67 tmp]# curl -u Maurizio845:cloudera http://ec2-18-194-169-169.eu-central-1.compute.amazonaws.com:7180/api/v14/cm/version
{
  "version" : "5.9.3",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170627-1506",
  "gitHash" : "23506bb4e114dd460bdac64c57a672e6be631907",
  "snapshot" : false
}


[root@ip-172-31-25-67 tmp]# curl -u Maurizio845:cloudera http://ec2-18-194-169-169.eu-central-1.compute.amazonaws.com:7180/api/v14/users
{
  "items" : [ {
    "name" : "Maurizio845",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "minotaur ",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  }]
}


[root@ip-172-31-25-67 tmp]# curl -u Maurizio845:cloudera http://ec2-18-194-169-169.eu-central-1.compute.amazonaws.com:7180/api/v14/cm/scmDbInfo
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}

```