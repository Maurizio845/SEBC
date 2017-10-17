# groupadd sebc

# useradd -g sebc -m maurizio845

# sudo -u hdfs hdfs dfs -mkdir /user/maurizio845

# sudo -u hdfs hdfs dfs -chown maurizio845:sebc /user/maurizio845

# time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 100000000 /user/maurizio845/teragen.data
17/10/17 13:21:13 INFO mapreduce.Job: Job job_1508232161574_0006 completed successfully
17/10/17 13:21:13 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=488756
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=543606
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=543606
                Total vcore-seconds taken by all map tasks=543606
                Total megabyte-seconds taken by all map tasks=556652544
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1450
                CPU time spent (ms)=153460
                Physical memory (bytes) snapshot=844582912
                Virtual memory (bytes) snapshot=6263808000
                Total committed heap usage (bytes)=836239360
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    2m30.064s
user    0m5.971s
sys     0m0.322s



# time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort /user/maurizio845/teragen.data /user/maurizio845/terasort.data
17/10/17 13:34:07 INFO mapreduce.Job: Job job_1508232161574_0007 completed successfully
17/10/17 13:34:07 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4481894721
                FILE: Number of bytes written=8894917804
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000049800
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=918
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=6
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=1705984
                Total time spent by all reduces in occupied slots (ms)=638469
                Total time spent by all map tasks (ms)=1705984
                Total time spent by all reduce tasks (ms)=638469
                Total vcore-seconds taken by all map tasks=1705984
                Total vcore-seconds taken by all reduce tasks=638469
                Total megabyte-seconds taken by all map tasks=1746927616
                Total megabyte-seconds taken by all reduce tasks=653792256
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375170195
                Input split bytes=49800
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375170195
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =1800
                Failed Shuffles=0
                Merged Map outputs=1800
                GC time elapsed (ms)=22331
                CPU time spent (ms)=1247510
                Physical memory (bytes) snapshot=144675061760
                Virtual memory (bytes) snapshot=480941027328
                Total committed heap usage (bytes)=173799899136
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
17/10/17 13:34:07 INFO terasort.TeraSort: done

real    11m27.028s
user    0m9.944s
sys     0m0.471s

