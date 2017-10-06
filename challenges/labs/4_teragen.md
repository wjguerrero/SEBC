```
[saturn@ip-172-31-45-148 tmp]$ time hadoop jar /disco1/cloudera/parcels/CDH/jars                                                                                        /hadoop-examples.jar teragen -Dmapred.map.tasks=12 -Ddfs.block.size=33554432 -Dm                                                                                        apreduce.map.memory.mb=512 65536000 /user/saturn/tgen
17/10/06 15:28:02 INFO client.RMProxy: Connecting to ResourceManager at ip-172-3                                                                                        1-40-210.us-east-2.compute.internal/172.31.40.210:8032
17/10/06 15:28:03 INFO terasort.TeraSort: Generating 65536000 using 12
17/10/06 15:28:03 INFO mapreduce.JobSubmitter: number of splits:12
17/10/06 15:28:03 INFO Configuration.deprecation: mapred.map.tasks is deprecated                                                                                        . Instead, use mapreduce.job.maps
17/10/06 15:28:03 INFO Configuration.deprecation: dfs.block.size is deprecated.                                                                                         Instead, use dfs.blocksize
17/10/06 15:28:03 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_15                                                                                        07300102428_0001
17/10/06 15:28:03 INFO impl.YarnClientImpl: Submitted application application_15                                                                                        07300102428_0001
17/10/06 15:28:03 INFO mapreduce.Job: The url to track the job: http://ip-172-31                                                                                        -40-210.us-east-2.compute.internal:8088/proxy/application_1507300102428_0001/
17/10/06 15:28:03 INFO mapreduce.Job: Running job: job_1507300102428_0001
17/10/06 15:28:09 INFO mapreduce.Job: Job job_1507300102428_0001 running in uber                                                                                         mode : false
17/10/06 15:28:09 INFO mapreduce.Job:  map 0% reduce 0%
17/10/06 15:28:21 INFO mapreduce.Job:  map 6% reduce 0%
17/10/06 15:28:22 INFO mapreduce.Job:  map 8% reduce 0%
17/10/06 15:28:23 INFO mapreduce.Job:  map 13% reduce 0%
17/10/06 15:28:24 INFO mapreduce.Job:  map 15% reduce 0%
17/10/06 15:28:25 INFO mapreduce.Job:  map 16% reduce 0%
17/10/06 15:28:26 INFO mapreduce.Job:  map 19% reduce 0%
17/10/06 15:28:27 INFO mapreduce.Job:  map 21% reduce 0%
17/10/06 15:28:28 INFO mapreduce.Job:  map 22% reduce 0%
17/10/06 15:28:29 INFO mapreduce.Job:  map 24% reduce 0%
17/10/06 15:28:30 INFO mapreduce.Job:  map 27% reduce 0%
17/10/06 15:28:31 INFO mapreduce.Job:  map 28% reduce 0%
17/10/06 15:28:32 INFO mapreduce.Job:  map 30% reduce 0%
17/10/06 15:28:33 INFO mapreduce.Job:  map 32% reduce 0%
17/10/06 15:28:34 INFO mapreduce.Job:  map 33% reduce 0%
17/10/06 15:28:35 INFO mapreduce.Job:  map 36% reduce 0%
17/10/06 15:28:36 INFO mapreduce.Job:  map 38% reduce 0%
17/10/06 15:28:37 INFO mapreduce.Job:  map 39% reduce 0%
17/10/06 15:28:38 INFO mapreduce.Job:  map 42% reduce 0%
17/10/06 15:28:47 INFO mapreduce.Job:  map 47% reduce 0%
17/10/06 15:28:49 INFO mapreduce.Job:  map 54% reduce 0%
17/10/06 15:28:50 INFO mapreduce.Job:  map 56% reduce 0%
17/10/06 15:28:53 INFO mapreduce.Job:  map 57% reduce 0%
17/10/06 15:28:55 INFO mapreduce.Job:  map 58% reduce 0%
17/10/06 15:29:01 INFO mapreduce.Job:  map 59% reduce 0%
17/10/06 15:29:04 INFO mapreduce.Job:  map 60% reduce 0%
17/10/06 15:29:05 INFO mapreduce.Job:  map 61% reduce 0%
17/10/06 15:29:07 INFO mapreduce.Job:  map 64% reduce 0%
17/10/06 15:29:10 INFO mapreduce.Job:  map 67% reduce 0%
17/10/06 15:29:11 INFO mapreduce.Job:  map 72% reduce 0%
17/10/06 15:29:13 INFO mapreduce.Job:  map 75% reduce 0%
17/10/06 15:29:14 INFO mapreduce.Job:  map 76% reduce 0%
17/10/06 15:29:16 INFO mapreduce.Job:  map 78% reduce 0%
17/10/06 15:29:17 INFO mapreduce.Job:  map 79% reduce 0%
17/10/06 15:29:19 INFO mapreduce.Job:  map 80% reduce 0%
17/10/06 15:29:20 INFO mapreduce.Job:  map 83% reduce 0%
17/10/06 15:29:30 INFO mapreduce.Job:  map 92% reduce 0%
17/10/06 15:29:33 INFO mapreduce.Job:  map 100% reduce 0%
17/10/06 15:29:33 INFO mapreduce.Job: Job job_1507300102428_0001 completed succe                                                                                        ssfully
17/10/06 15:29:33 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1483910
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1025
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=48
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=24
        Job Counters
                Launched map tasks=12
                Other local map tasks=12
                Total time spent by all maps in occupied slots (ms)=361387
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=361387
                Total vcore-seconds taken by all map tasks=361387
                Total megabyte-seconds taken by all map tasks=370060288
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1025
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=2873
                CPU time spent (ms)=139370
                Physical memory (bytes) snapshot=2592448512
                Virtual memory (bytes) snapshot=13795086336
                Total committed heap usage (bytes)=4598530048
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    1m33.113s
user    0m4.635s
sys     0m0.232s

[saturn@ip-172-31-45-148 tmp]$ hdfs dfs -ls /user/saturn/tgen
Found 13 items
-rw-r--r--   3 saturn supergroup          0 2017-10-06 15:29 /user/saturn/tgen/_                                                                                        SUCCESS
-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 15:28 /user/saturn/tgen/p                                                                                        art-m-00000
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 15:28 /user/saturn/tgen/p                                                                                        art-m-00001
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 15:28 /user/saturn/tgen/p                                                                                        art-m-00002
-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 15:28 /user/saturn/tgen/p                                                                                        art-m-00003
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 15:28 /user/saturn/tgen/p                                                                                        art-m-00004
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 15:29 /user/saturn/tgen/p                                                                                        art-m-00005
-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 15:29 /user/saturn/tgen/p                                                                                        art-m-00006
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 15:29 /user/saturn/tgen/p                                                                                        art-m-00007
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 15:29 /user/saturn/tgen/p                                                                                        art-m-00008
-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 15:29 /user/saturn/tgen/p                                                                                        art-m-00009
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 15:29 /user/saturn/tgen/p                                                                                        art-m-00010
-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 15:29 /user/saturn/tgen/p                                                                                        art-m-00011

[saturn@ip-172-31-45-148 tmp]$ hadoop fsck -blocks /user/saturn
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-40-210.us-east-2.compute.internal:50                                                                                        070
FSCK started by saturn (auth:SIMPLE) from /172.31.45.148 for path /user/saturn a                                                                                        t Fri Oct 06 15:32:11 UTC 2017
.................Status: HEALTHY
 Total size:    19660800000 B
 Total dirs:    9
 Total files:   17
 Total symlinks:                0
 Total blocks (validated):      596 (avg. block size 32987919 B)
 Minimally replicated blocks:   596 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri Oct 06 15:32:11 UTC 2017 in 19 milliseconds


The filesystem under path '/user/saturn' is HEALTHY
```

