[wjguerrero@ip-172-31-5-64 centos]$ time hadoop jar /disco1/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 10737418 /user/wjguerrero/teragen
17/10/03 15:06:08 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-13-29.us-east-2.compute.internal/172.31.13.29:8032
17/10/03 15:06:08 INFO terasort.TeraSort: Generating 10737418 using 4
17/10/03 15:06:09 INFO mapreduce.JobSubmitter: number of splits:4
17/10/03 15:06:09 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/10/03 15:06:09 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/10/03 15:06:09 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507040114856_0003
17/10/03 15:06:09 INFO impl.YarnClientImpl: Submitted application application_1507040114856_0003
17/10/03 15:06:09 INFO mapreduce.Job: The url to track the job: http://ip-172-31-13-29.us-east-2.compute.internal:8088/proxy/application_1507040114856_0003/
17/10/03 15:06:09 INFO mapreduce.Job: Running job: job_1507040114856_0003
17/10/03 15:06:14 INFO mapreduce.Job: Job job_1507040114856_0003 running in uber mode : false
17/10/03 15:06:14 INFO mapreduce.Job:  map 0% reduce 0%
17/10/03 15:06:26 INFO mapreduce.Job:  map 56% reduce 0%
17/10/03 15:06:27 INFO mapreduce.Job:  map 76% reduce 0%
17/10/03 15:06:28 INFO mapreduce.Job:  map 88% reduce 0%
17/10/03 15:06:29 INFO mapreduce.Job:  map 100% reduce 0%
17/10/03 15:06:29 INFO mapreduce.Job: Job job_1507040114856_0003 completed successfully
17/10/03 15:06:30 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=494656
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=337
                HDFS: Number of bytes written=1073741800
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=47313
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=47313
                Total vcore-seconds taken by all map tasks=47313
                Total megabyte-seconds taken by all map tasks=48448512
        Map-Reduce Framework
                Map input records=10737418
                Map output records=10737418
                Input split bytes=337
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=542
                CPU time spent (ms)=29900
                Physical memory (bytes) snapshot=1495355392
                Virtual memory (bytes) snapshot=6375088128
                Total committed heap usage (bytes)=2399141888
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=23055106908592388
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=1073741800

real    0m23.478s
user    0m4.181s
sys     0m0.200s
[wjguerrero@ip-172-31-5-64 centos]$ time hadoop jar /disco1/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort  /user/wjguerrero/teragen /user/wjguerrero/terasort
17/10/03 15:18:25 INFO terasort.TeraSort: starting
17/10/03 15:18:26 INFO input.FileInputFormat: Total input paths to process : 4
Spent 140ms computing base-splits.
Spent 2ms computing TeraScheduler splits.
Computing input splits took 143ms
Sampling 10 splits of 32
Making 4 from 100000 sampled records
Computing parititions took 499ms
Spent 644ms computing partitions.
17/10/03 15:18:26 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-13-29.us-east-2.compute.internal/172.31.13.29:8032
17/10/03 15:18:27 INFO mapreduce.JobSubmitter: number of splits:32
17/10/03 15:18:27 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507040114856_0004
17/10/03 15:18:27 INFO impl.YarnClientImpl: Submitted application application_1507040114856_0004
17/10/03 15:18:27 INFO mapreduce.Job: The url to track the job: http://ip-172-31-13-29.us-east-2.compute.internal:8088/proxy/application_1507040114856_0004/
17/10/03 15:18:27 INFO mapreduce.Job: Running job: job_1507040114856_0004
17/10/03 15:18:32 INFO mapreduce.Job: Job job_1507040114856_0004 running in uber mode : false
17/10/03 15:18:32 INFO mapreduce.Job:  map 0% reduce 0%
17/10/03 15:18:39 INFO mapreduce.Job:  map 6% reduce 0%
17/10/03 15:18:40 INFO mapreduce.Job:  map 13% reduce 0%
17/10/03 15:18:47 INFO mapreduce.Job:  map 25% reduce 0%
17/10/03 15:18:53 INFO mapreduce.Job:  map 34% reduce 0%
17/10/03 15:18:54 INFO mapreduce.Job:  map 38% reduce 0%
17/10/03 15:19:00 INFO mapreduce.Job:  map 44% reduce 0%
17/10/03 15:19:01 INFO mapreduce.Job:  map 50% reduce 0%
17/10/03 15:19:08 INFO mapreduce.Job:  map 59% reduce 0%
17/10/03 15:19:09 INFO mapreduce.Job:  map 63% reduce 0%
17/10/03 15:19:15 INFO mapreduce.Job:  map 72% reduce 0%
17/10/03 15:19:16 INFO mapreduce.Job:  map 75% reduce 0%
17/10/03 15:19:22 INFO mapreduce.Job:  map 84% reduce 0%
17/10/03 15:19:23 INFO mapreduce.Job:  map 88% reduce 0%
17/10/03 15:19:29 INFO mapreduce.Job:  map 97% reduce 0%
17/10/03 15:19:34 INFO mapreduce.Job:  map 97% reduce 8%
17/10/03 15:19:35 INFO mapreduce.Job:  map 100% reduce 8%
17/10/03 15:19:37 INFO mapreduce.Job:  map 100% reduce 10%
17/10/03 15:19:39 INFO mapreduce.Job:  map 100% reduce 27%
17/10/03 15:19:40 INFO mapreduce.Job:  map 100% reduce 34%
17/10/03 15:19:41 INFO mapreduce.Job:  map 100% reduce 53%
17/10/03 15:19:42 INFO mapreduce.Job:  map 100% reduce 61%
17/10/03 15:19:43 INFO mapreduce.Job:  map 100% reduce 75%
17/10/03 15:19:45 INFO mapreduce.Job:  map 100% reduce 96%
17/10/03 15:19:46 INFO mapreduce.Job:  map 100% reduce 100%
17/10/03 15:19:47 INFO mapreduce.Job: Job job_1507040114856_0004 completed successfully
17/10/03 15:19:47 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=472256307
                FILE: Number of bytes written=942996561
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1073746792
                HDFS: Number of bytes written=1073741800
                HDFS: Number of read operations=108
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=32
                Launched reduce tasks=4
                Data-local map tasks=28
                Rack-local map tasks=4
                Total time spent by all maps in occupied slots (ms)=185172
                Total time spent by all reduces in occupied slots (ms)=52178
                Total time spent by all map tasks (ms)=185172
                Total time spent by all reduce tasks (ms)=52178
                Total vcore-seconds taken by all map tasks=185172
                Total vcore-seconds taken by all reduce tasks=52178
                Total megabyte-seconds taken by all map tasks=189616128
                Total megabyte-seconds taken by all reduce tasks=53430272
        Map-Reduce Framework
                Map input records=10737418
                Map output records=10737418
                Map output bytes=1095216636
                Map output materialized bytes=466235496
                Input split bytes=4992
                Combine input records=0
                Combine output records=0
                Reduce input groups=10737418
                Reduce shuffle bytes=466235496
                Reduce input records=10737418
                Reduce output records=10737418
                Spilled Records=21474836
                Shuffled Maps =128
                Failed Shuffles=0
                Merged Map outputs=128
                GC time elapsed (ms)=2678
                CPU time spent (ms)=146620
                Physical memory (bytes) snapshot=19694194688
                Virtual memory (bytes) snapshot=57593798656
                Total committed heap usage (bytes)=20294139904
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1073741800
        File Output Format Counters
                Bytes Written=1073741800
17/10/03 15:19:47 INFO terasort.TeraSort: done

real    1m23.229s
user    0m6.320s
sys     0m0.212s
