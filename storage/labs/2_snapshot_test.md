# hdfs dfs -mkdir /user/maurizio845/precious

# hdfs dfs -put /tmp/SEBC-master.zip /user/maurizio845/precious

#[root@ip-172-31-25-67 ~]# sudo -u hdfs hdfs dfsadmin -allowSnapshot /user/maurizio845/precious
Allowing snaphot on /user/maurizio845/precious succeeded

#[root@ip-172-31-25-67 ~]# sudo -u hdfs hdfs dfs -createSnapshot /user/maurizio845/precious sebc-hdfs-test
Created snapshot /user/maurizio845/precious/.snapshot/sebc-hdfs-test

# hdfs dfs -rm -r /user/maurizio845/precious/
rm: Failed to move to trash: hdfs://ip-172-31-26-116.eu-central-1.compute.internal:8020/user/maurizio845/precious: The directory /user/maurizio845/precious cannot be deleted since /user/maurizio845/precious is snapshottable and already has snapshots


# hdfs dfs -rm /user/maurizio845/precious/SEBC-master.zip
17/10/17 14:03:21 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-26-116.eu-central-1.compute.internal:8020/user/maurizio845/precious/SEBC-master.zip' to trash at: hdfs://ip-172-31-26-116.eu-central-1.compute.internal:8020/user/maurizio845/.Trash/Current/user/maurizio845/precious/SEBC-master.zip

#[maurizio845@ip-172-31-25-67 ~]$ hdfs dfs -cp /user/maurizio845/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /user/maurizio845/precious/