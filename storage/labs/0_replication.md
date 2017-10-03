[hdfs@ip-172-31-0-4 centos]$ hdfs fsck /user/hdfs/wjguerrero -files -blocks
Connecting to namenode via http://ip-172-31-13-29.us-east-2.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.0.4 for path /user/hdfs/wjguerrero at Tue Oct 03 14:45:27 UTC 2017
/user/hdfs/wjguerrero <dir>
/user/hdfs/wjguerrero/teragen <dir>
/user/hdfs/wjguerrero/teragen/* <dir>
/user/hdfs/wjguerrero/teragen/*/teragen <dir>
/user/hdfs/wjguerrero/teragen/*/teragen/_SUCCESS 0 bytes, 0 block(s):  OK

/user/hdfs/wjguerrero/teragen/*/teragen/part-m-00000 524288000 bytes, 4 block(s):  OK
0. BP-1961274915-172.31.13.29-1506979786245:blk_1073743566_2742 len=134217728 Live_repl=3
1. BP-1961274915-172.31.13.29-1506979786245:blk_1073743568_2744 len=134217728 Live_repl=3
2. BP-1961274915-172.31.13.29-1506979786245:blk_1073743569_2745 len=134217728 Live_repl=3
3. BP-1961274915-172.31.13.29-1506979786245:blk_1073743570_2746 len=121634816 Live_repl=3

/user/hdfs/wjguerrero/teragen/_SUCCESS 0 bytes, 0 block(s):  OK

/user/hdfs/wjguerrero/teragen/part-m-00000 262144000 bytes, 2 block(s):  OK
0. BP-1961274915-172.31.13.29-1506979786245:blk_1073743487_2663 len=134217728 Live_repl=3
1. BP-1961274915-172.31.13.29-1506979786245:blk_1073743490_2666 len=127926272 Live_repl=3

/user/hdfs/wjguerrero/teragen/part-m-00001 262144000 bytes, 2 block(s):  OK
0. BP-1961274915-172.31.13.29-1506979786245:blk_1073743488_2664 len=134217728 Live_repl=3
1. BP-1961274915-172.31.13.29-1506979786245:blk_1073743489_2665 len=127926272 Live_repl=3

Status: HEALTHY
 Total size:    1048576000 B
 Total dirs:    4
 Total files:   5
 Total symlinks:                0
 Total blocks (validated):      8 (avg. block size 131072000 B)
 Minimally replicated blocks:   8 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 03 14:45:27 UTC 2017 in 3 milliseconds


The filesystem under path '/user/hdfs/wjguerrero' is HEALTHY

[hdfs@ip-172-31-0-4 centos]$ hdfs fsck /user/hdfs/danielrozental -files -blocks
Connecting to namenode via http://ip-172-31-13-29.us-east-2.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.0.4 for path /user/hdfs/danielrozental at Tue Oct 03 14:50:30 UTC 2017
/user/hdfs/danielrozental <dir>
/user/hdfs/danielrozental/teragen <dir>
/user/hdfs/danielrozental/teragen/* <dir>
/user/hdfs/danielrozental/teragen/*/teragen <dir>
/user/hdfs/danielrozental/teragen/*/teragen/_SUCCESS 0 bytes, 0 block(s):  OK

/user/hdfs/danielrozental/teragen/*/teragen/part-m-00000 524288000 bytes, 4 block(s):  OK
0. BP-1961274915-172.31.13.29-1506979786245:blk_1073743596_2772 len=134217728 Live_repl=3
1. BP-1961274915-172.31.13.29-1506979786245:blk_1073743598_2774 len=134217728 Live_repl=3
2. BP-1961274915-172.31.13.29-1506979786245:blk_1073743599_2775 len=134217728 Live_repl=3
3. BP-1961274915-172.31.13.29-1506979786245:blk_1073743600_2776 len=121634816 Live_repl=3

Status: HEALTHY
 Total size:    524288000 B
 Total dirs:    4
 Total files:   2
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 131072000 B)
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
FSCK ended at Tue Oct 03 14:50:30 UTC 2017 in 2 milliseconds


The filesystem under path '/user/hdfs/danielrozental' is HEALTHY
