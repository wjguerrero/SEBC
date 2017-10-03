[hdfs@ip-172-31-13-29 centos]$ hdfs dfs -ls /user/hdfs/precious
Found 1 items
-rw-r--r--   3 hdfs supergroup     474831 2017-10-03 15:57 /user/hdfs/precious/SEBC-master-students.zip
[hdfs@ip-172-31-13-29 centos]$ hdfs dfs -rm -r /user/hdfs/precious
rm: Failed to move to trash: hdfs://ip-172-31-13-29.us-east-2.compute.internal:8020/user/hdfs/precious: The directory /user/hdfs/precious cannot be deleted since /user/hdfs/precious is snapshottable and already has snapshots
[hdfs@ip-172-31-13-29 centos]$ hdfs dfs -rm /user/hdfs/precious/SEBC-master-students.zip
17/10/03 16:53:56 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-13-29.us-east-2.compute.internal:8020/user/hdfs/precious/SEBC-master-students.zip' to trash at: hdfs://ip-172-31-13-29.us-east-2.compute.internal:8020/user/hdfs/.Trash/Current/user/hdfs/precious/SEBC-master-students.zip
[hdfs@ip-172-31-13-29 centos]$
