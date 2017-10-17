1### Create source and target directory
# sudo -u hdfs hdfs dfs -mkdir /tmp/source_Maurizio845
# sudo -u hdfs hdfs dfs -mkdir /tmp/target_laertgjoni

2### generate 500MB data into source directory
# sudo -u hdfs hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 5000000 /tmp/source_Maurizio845

3### Configure a peer into cloudera manager ui
4### Configure and run an HDFS replication

5### Check HDFS source and target status
#[centos@ip-172-31-25-67 ~]$ sudo -u hdfs hdfs fsck /tmp/source_Maurizio845 -files -blocks
Connecting to namenode via http://ip-172-31-26-116.eu-central-1.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.25.67 for path /tmp/source_Maurizio845 at Tue Oct 17 11:27:27 UTC 2017
/tmp/source_Maurizio845 <dir>
/tmp/source_Maurizio845/_SUCCESS 0 bytes, 0 block(s):  OK

/tmp/source_Maurizio845/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-35457092-172.31.26.116-1508227824011:blk_1073741960_1136 len=134217728 Live_repl=3
1. BP-35457092-172.31.26.116-1508227824011:blk_1073741962_1138 len=115782272 Live_repl=3

/tmp/source_Maurizio845/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-35457092-172.31.26.116-1508227824011:blk_1073741959_1135 len=134217728 Live_repl=3
1. BP-35457092-172.31.26.116-1508227824011:blk_1073741961_1137 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 17 11:27:27 UTC 2017 in 3 milliseconds


The filesystem under path '/tmp/source_Maurizio845' is HEALTHY

#[centos@ip-172-31-25-67 ~]$ sudo -u hdfs hdfs fsck /tmp/target_laertgjoni -files -blocks
Connecting to namenode via http://ip-172-31-26-116.eu-central-1.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.25.67 for path /tmp/target_laertgjoni at Tue Oct 17 11:28:10 UTC 2017
/tmp/target_laertgjoni <dir>
/tmp/target_laertgjoni/_SUCCESS 0 bytes, 0 block(s):  OK

/tmp/target_laertgjoni/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-35457092-172.31.26.116-1508227824011:blk_1073742083_1259 len=134217728 Live_repl=3
1. BP-35457092-172.31.26.116-1508227824011:blk_1073742086_1262 len=115782272 Live_repl=3

/tmp/target_laertgjoni/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-35457092-172.31.26.116-1508227824011:blk_1073742085_1261 len=134217728 Live_repl=3
1. BP-35457092-172.31.26.116-1508227824011:blk_1073742087_1263 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 17 11:28:10 UTC 2017 in 2 milliseconds


The filesystem under path '/tmp/target_laertgjoni' is HEALTHY