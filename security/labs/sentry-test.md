```

[root@ip-172-31-25-67 ~]# beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM
Enter username for jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM: maurizio845
Enter password for jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-29-107.eu-central-1> show tables;
INFO  : Compiling command(queryId=hive_20171019081919_04ca7e0c-5a52-4d8c-89d4-cf34d2823c55): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019081919_04ca7e0c-5a52-4d8c-89d4-cf34d2823c55); Time taken: 0.09 seconds
INFO  : Executing command(queryId=hive_20171019081919_04ca7e0c-5a52-4d8c-89d4-cf34d2823c55): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019081919_04ca7e0c-5a52-4d8c-89d4-cf34d2823c55); Time taken: 0.13 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.332 seconds)

(After create sentry role with full authorization)

[root@ip-172-31-25-67 ~]# beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM
scan complete in 3ms
Connecting to jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM
Enter username for jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM: cloudera
Enter password for jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-29-107.eu-central-1> show tables;
INFO  : Compiling command(queryId=hive_20171019095656_453053a5-68af-4e81-aa02-92cdec3366cf): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019095656_453053a5-68af-4e81-aa02-92cdec3366cf); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20171019095656_453053a5-68af-4e81-aa02-92cdec3366cf): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019095656_453053a5-68af-4e81-aa02-92cdec3366cf); Time taken: 0.12 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.301 seconds)



[root@ip-172-31-25-67 ~]# kinit george
Password for george@SEBC.COM:

[root@ip-172-31-25-67 ~]# klist -e
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: george@SEBC.COM

Valid starting     Expires            Service principal
10/19/17 08:35:08  10/20/17 08:35:08  krbtgt/SEBC.COM@SEBC.COM
        renew until 10/26/17 08:35:08, Etype (skey, tkt): aes256-cts-hmac-sha1-96, aes256-cts-hmac-sha1-96
		
		
[root@ip-172-31-25-67 ~]# beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive


beeline> !connect jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM
Enter username for jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM: george
Enter password for jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM: ******
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-29-107.eu-central-1> show tables;
INFO  : Compiling command(queryId=hive_20171019083636_eeb6b066-3c32-4852-9026-70520381a37c): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019083636_eeb6b066-3c32-4852-9026-70520381a37c); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20171019083636_eeb6b066-3c32-4852-9026-70520381a37c): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019083636_eeb6b066-3c32-4852-9026-70520381a37c); Time taken: 0.138 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.323 seconds)



[root@ip-172-31-25-67 ~]# kinit ferdinand
Password for ferdinand@SEBC.COM:

[root@ip-172-31-25-67 ~]# beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive

beeline> !connect jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM
Enter username for jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM: ferdinand
Enter password for jdbc:hive2://ip-172-31-29-107.eu-central-1.compute.internal:10000/default;principal=hive/ip-172-31-29-107.eu-central-1.compute.internal@SEBC.COM: *********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-29-107.eu-central-1> show tables;
INFO  : Compiling command(queryId=hive_20171019083838_1464740a-38a9-4efa-9081-b1b46de0083a): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019083838_1464740a-38a9-4efa-9081-b1b46de0083a); Time taken: 0.066 seconds
INFO  : Executing command(queryId=hive_20171019083838_1464740a-38a9-4efa-9081-b1b46de0083a): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019083838_1464740a-38a9-4efa-9081-b1b46de0083a); Time taken: 0.203 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.381 seconds)


```
