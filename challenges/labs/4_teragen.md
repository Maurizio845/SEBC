```
#### Teragen 
[ernest@ip-172-31-39-254 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=6 -Ddfs.block.size=33554432 51200000 /user/ernest/tgen512m
real    1m37.786s
user    1m5.967s
sys     0m4.290s


#### Hdfs 
[root@ip-172-31-39-254 tmp]# sudo -u hdfs hdfs dfs -ls /user/ernest/tgen512m
Found 2 items
-rw-r--r--   3 ernest ernest          0 2017-10-20 09:44 /user/ernest/tgen512m/_SUCCESS
-rw-r--r--   3 ernest ernest 5120000000 2017-10-20 09:44 /user/ernest/tgen512m/part-m-00000

#### Blocks 
[root@ip-172-31-39-254 tmp]# sudo -u hdfs hdfs fsck /user/ernest/tgen512m
Connecting to namenode via http://ip-172-31-46-9.eu-central-1.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.39.254 for path /user/ernest/tgen512m at Fri Oct 20 09:46:33 UTC 2017
..Status: HEALTHY
 Total size:    5120000000 B
 Total dirs:    1
 Total files:   2
 Total symlinks:                0
 Total blocks (validated):      153 (avg. block size 33464052 B)
 Minimally replicated blocks:   153 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri Oct 20 09:46:33 UTC 2017 in 3 milliseconds


The filesystem under path '/user/ernest/tgen512m' is HEALTHY


```
