su hdfs

time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.11.0.jar teragen -Dmapreduce.job.maps=4 -D dfs.block.size=33554432 100000000 /user/Victor2806/teragen.out

 
[hdfs@ip-172-31-12-156 ~]$ hadoop fs -ls /user/Victor2806/teragen.out
Found 5 items
-rw-r--r--   3 hdfs supergroup          0 2017-05-04 02:14 /user/Victor2806/teragen.out/_SUCCESS
-rw-r--r--   3 hdfs supergroup 2500000000 2017-05-04 02:14 /user/Victor2806/teragen.out/part-m-00000
-rw-r--r--   3 hdfs supergroup 2500000000 2017-05-04 02:14 /user/Victor2806/teragen.out/part-m-00001
-rw-r--r--   3 hdfs supergroup 2500000000 2017-05-04 02:14 /user/Victor2806/teragen.out/part-m-00002
-rw-r--r--   3 hdfs supergroup 2500000000 2017-05-04 02:13 /user/Victor2806/teragen.out/part-m-00003
[hdfs@ip-172-31-12-156 ~]$

 

Terasort command

time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.11.0.jar terasort /user/Victor2806/teragen.out /user/ABC/terasort.out


[hdfs@ip-172-31-12-156 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.11.0.jar terasort /user/Victor2806/teragen.out /user/ABC/terasort.out
17/05/04 02:27:48 INFO terasort.TeraSort: starting
17/05/04 02:27:50 INFO input.FileInputFormat: Total input paths to process : 4
Spent 316ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 323ms
Sampling 10 splits of 300
Making 8 from 100000 sampled records
Computing parititions took 970ms
Spent 1295ms computing partitions.
17/05/04 02:27:51 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-14.us-west-2.compute.internal/172.31.0.14:8032
17/05/04 02:27:52 INFO mapreduce.JobSubmitter: number of splits:300
17/05/04 02:27:52 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1493855935344_0002
17/05/04 02:27:52 INFO impl.YarnClientImpl: Submitted application application_1493855935344_0002
17/05/04 02:27:52 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-14.us-west-2.compute.internal:8088/proxy/application_1493855935344_0002/
17/05/04 02:27:52 INFO mapreduce.Job: Running job: job_1493855935344_0002
17/05/04 02:27:59 INFO mapreduce.Job: Job job_1493855935344_0002 running in uber mode : false
17/05/04 02:27:59 INFO mapreduce.Job:  map 0% reduce 0%
17/05/04 02:28:11 INFO mapreduce.Job:  map 1% reduce 0%
17/05/04 02:28:15 INFO mapreduce.Job:  map 3% reduce 0%
17/05/04 02:28:16 INFO mapreduce.Job:  map 5% reduce 0%
17/05/04 02:28:22 INFO mapreduce.Job:  map 6% reduce 0%
17/05/04 02:28:29 INFO mapreduce.Job:  map 8% reduce 0%
17/05/04 02:28:30 INFO mapreduce.Job:  map 9% reduce 0%
17/05/04 02:28:31 INFO mapreduce.Job:  map 10% reduce 0%
17/05/04 02:28:33 INFO mapreduce.Job:  map 11% reduce 0%
17/05/04 02:28:43 INFO mapreduce.Job:  map 12% reduce 0%
17/05/04 02:28:44 INFO mapreduce.Job:  map 15% reduce 0%
17/05/04 02:28:45 INFO mapreduce.Job:  map 16% reduce 0%
17/05/04 02:28:55 INFO mapreduce.Job:  map 17% reduce 0%
17/05/04 02:28:57 INFO mapreduce.Job:  map 19% reduce 0%
17/05/04 02:28:58 INFO mapreduce.Job:  map 20% reduce 0%
17/05/04 02:28:59 INFO mapreduce.Job:  map 21% reduce 0%
17/05/04 02:29:06 INFO mapreduce.Job:  map 22% reduce 0%
17/05/04 02:29:11 INFO mapreduce.Job:  map 23% reduce 0%
17/05/04 02:29:12 INFO mapreduce.Job:  map 25% reduce 0%
17/05/04 02:29:15 INFO mapreduce.Job:  map 26% reduce 0%
17/05/04 02:29:17 INFO mapreduce.Job:  map 27% reduce 0%
17/05/04 02:29:26 INFO mapreduce.Job:  map 30% reduce 0%
17/05/04 02:29:28 INFO mapreduce.Job:  map 32% reduce 0%
17/05/04 02:29:39 INFO mapreduce.Job:  map 33% reduce 0%
17/05/04 02:29:40 INFO mapreduce.Job:  map 36% reduce 0%
17/05/04 02:29:42 INFO mapreduce.Job:  map 37% reduce 0%
17/05/04 02:29:50 INFO mapreduce.Job:  map 38% reduce 0%
17/05/04 02:29:55 INFO mapreduce.Job:  map 41% reduce 0%
17/05/04 02:29:57 INFO mapreduce.Job:  map 42% reduce 0%
17/05/04 02:30:02 INFO mapreduce.Job:  map 43% reduce 0%
17/05/04 02:30:09 INFO mapreduce.Job:  map 45% reduce 0%
17/05/04 02:30:10 INFO mapreduce.Job:  map 46% reduce 0%
17/05/04 02:30:12 INFO mapreduce.Job:  map 47% reduce 0%
17/05/04 02:30:13 INFO mapreduce.Job:  map 48% reduce 0%
17/05/04 02:30:22 INFO mapreduce.Job:  map 49% reduce 0%
17/05/04 02:30:23 INFO mapreduce.Job:  map 51% reduce 0%
17/05/04 02:30:24 INFO mapreduce.Job:  map 52% reduce 0%
17/05/04 02:30:29 INFO mapreduce.Job:  map 53% reduce 0%
17/05/04 02:30:35 INFO mapreduce.Job:  map 54% reduce 0%
17/05/04 02:30:36 INFO mapreduce.Job:  map 55% reduce 0%
17/05/04 02:30:37 INFO mapreduce.Job:  map 57% reduce 0%
17/05/04 02:30:44 INFO mapreduce.Job:  map 58% reduce 0%
17/05/04 02:30:46 INFO mapreduce.Job:  map 59% reduce 0%
17/05/04 02:30:50 INFO mapreduce.Job:  map 60% reduce 0%
17/05/04 02:30:51 INFO mapreduce.Job:  map 62% reduce 0%
17/05/04 02:30:56 INFO mapreduce.Job:  map 63% reduce 0%
17/05/04 02:30:58 INFO mapreduce.Job:  map 64% reduce 0%
17/05/04 02:31:04 INFO mapreduce.Job:  map 65% reduce 0%
17/05/04 02:31:05 INFO mapreduce.Job:  map 66% reduce 0%
17/05/04 02:31:06 INFO mapreduce.Job:  map 67% reduce 0%
17/05/04 02:31:08 INFO mapreduce.Job:  map 68% reduce 0%
17/05/04 02:31:13 INFO mapreduce.Job:  map 69% reduce 0%
17/05/04 02:31:18 INFO mapreduce.Job:  map 70% reduce 0%
17/05/04 02:31:19 INFO mapreduce.Job:  map 73% reduce 0%
17/05/04 02:31:27 INFO mapreduce.Job:  map 74% reduce 0%
17/05/04 02:31:30 INFO mapreduce.Job:  map 75% reduce 0%
17/05/04 02:31:32 INFO mapreduce.Job:  map 77% reduce 0%
17/05/04 02:31:33 INFO mapreduce.Job:  map 78% reduce 0%
17/05/04 02:31:40 INFO mapreduce.Job:  map 79% reduce 0%
17/05/04 02:31:42 INFO mapreduce.Job:  map 80% reduce 0%
17/05/04 02:31:44 INFO mapreduce.Job:  map 81% reduce 0%
17/05/04 02:31:46 INFO mapreduce.Job:  map 82% reduce 0%
17/05/04 02:31:48 INFO mapreduce.Job:  map 83% reduce 0%
17/05/04 02:31:50 INFO mapreduce.Job:  map 84% reduce 0%
17/05/04 02:31:56 INFO mapreduce.Job:  map 85% reduce 0%
17/05/04 02:31:58 INFO mapreduce.Job:  map 86% reduce 0%
17/05/04 02:32:04 INFO mapreduce.Job:  map 87% reduce 0%
17/05/04 02:32:07 INFO mapreduce.Job:  map 87% reduce 6%
17/05/04 02:32:08 INFO mapreduce.Job:  map 87% reduce 11%
17/05/04 02:32:09 INFO mapreduce.Job:  map 87% reduce 14%
17/05/04 02:32:10 INFO mapreduce.Job:  map 88% reduce 14%
17/05/04 02:32:11 INFO mapreduce.Job:  map 88% reduce 20%
17/05/04 02:32:12 INFO mapreduce.Job:  map 89% reduce 20%
17/05/04 02:32:13 INFO mapreduce.Job:  map 89% reduce 21%
17/05/04 02:32:14 INFO mapreduce.Job:  map 89% reduce 23%
17/05/04 02:32:15 INFO mapreduce.Job:  map 89% reduce 24%
17/05/04 02:32:17 INFO mapreduce.Job:  map 89% reduce 26%
17/05/04 02:32:18 INFO mapreduce.Job:  map 90% reduce 26%
17/05/04 02:32:24 INFO mapreduce.Job:  map 91% reduce 26%
17/05/04 02:32:27 INFO mapreduce.Job:  map 92% reduce 26%
17/05/04 02:32:29 INFO mapreduce.Job:  map 93% reduce 26%
17/05/04 02:32:30 INFO mapreduce.Job:  map 93% reduce 27%
17/05/04 02:32:36 INFO mapreduce.Job:  map 94% reduce 27%
17/05/04 02:32:38 INFO mapreduce.Job:  map 95% reduce 27%
17/05/04 02:32:42 INFO mapreduce.Job:  map 96% reduce 28%
17/05/04 02:32:44 INFO mapreduce.Job:  map 97% reduce 28%
17/05/04 02:32:49 INFO mapreduce.Job:  map 98% reduce 28%
17/05/04 02:32:53 INFO mapreduce.Job:  map 99% reduce 28%
17/05/04 02:32:54 INFO mapreduce.Job:  map 99% reduce 29%
17/05/04 02:32:55 INFO mapreduce.Job:  map 100% reduce 29%
17/05/04 02:32:57 INFO mapreduce.Job:  map 100% reduce 34%
17/05/04 02:32:58 INFO mapreduce.Job:  map 100% reduce 36%
17/05/04 02:33:00 INFO mapreduce.Job:  map 100% reduce 45%
17/05/04 02:33:02 INFO mapreduce.Job:  map 100% reduce 53%
17/05/04 02:33:03 INFO mapreduce.Job:  map 100% reduce 58%
17/05/04 02:33:04 INFO mapreduce.Job:  map 100% reduce 61%
17/05/04 02:33:06 INFO mapreduce.Job:  map 100% reduce 65%
17/05/04 02:33:08 INFO mapreduce.Job:  map 100% reduce 67%
17/05/04 02:33:09 INFO mapreduce.Job:  map 100% reduce 69%
17/05/04 02:33:10 INFO mapreduce.Job:  map 100% reduce 70%
17/05/04 02:33:12 INFO mapreduce.Job:  map 100% reduce 73%
17/05/04 02:33:13 INFO mapreduce.Job:  map 100% reduce 74%
17/05/04 02:33:14 INFO mapreduce.Job:  map 100% reduce 76%
17/05/04 02:33:15 INFO mapreduce.Job:  map 100% reduce 77%
17/05/04 02:33:18 INFO mapreduce.Job:  map 100% reduce 82%
17/05/04 02:33:20 INFO mapreduce.Job:  map 100% reduce 83%
17/05/04 02:33:21 INFO mapreduce.Job:  map 100% reduce 84%
17/05/04 02:33:22 INFO mapreduce.Job:  map 100% reduce 85%
17/05/04 02:33:24 INFO mapreduce.Job:  map 100% reduce 89%
17/05/04 02:33:26 INFO mapreduce.Job:  map 100% reduce 91%
17/05/04 02:33:27 INFO mapreduce.Job:  map 100% reduce 92%
17/05/04 02:33:28 INFO mapreduce.Job:  map 100% reduce 93%
17/05/04 02:33:30 INFO mapreduce.Job:  map 100% reduce 94%
17/05/04 02:33:33 INFO mapreduce.Job:  map 100% reduce 95%
17/05/04 02:33:34 INFO mapreduce.Job:  map 100% reduce 96%
17/05/04 02:33:36 INFO mapreduce.Job:  map 100% reduce 98%
17/05/04 02:33:42 INFO mapreduce.Job:  map 100% reduce 99%
17/05/04 02:33:44 INFO mapreduce.Job:  map 100% reduce 100%
17/05/04 02:33:45 INFO mapreduce.Job: Job job_1493855935344_0002 completed successfully
17/05/04 02:33:45 INFO mapreduce.Job: Counters: 53
        File System Counters
                FILE: Number of bytes read=4475262658
                FILE: Number of bytes written=8890253034
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000047700
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=924
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=8
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=3597782
                Total time spent by all reduces in occupied slots (ms)=750116
                Total time spent by all map tasks (ms)=3597782
                Total time spent by all reduce tasks (ms)=750116
                Total vcore-milliseconds taken by all map tasks=3597782
                Total vcore-milliseconds taken by all reduce tasks=750116
                Total megabyte-milliseconds taken by all map tasks=3684128768
                Total megabyte-milliseconds taken by all reduce tasks=768118784
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375225482
                Input split bytes=47700
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375225482
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =2400
                Failed Shuffles=0
                Merged Map outputs=2400
                GC time elapsed (ms)=48390
                CPU time spent (ms)=1643310
                Physical memory (bytes) snapshot=152545083392
                Virtual memory (bytes) snapshot=482302533632
                Total committed heap usage (bytes)=174659207168
                Peak Map Physical memory (bytes)=523718656
                Peak Map Virtual memory (bytes)=1583124480
                Peak Reduce Physical memory (bytes)=1002328064
                Peak Reduce Virtual memory (bytes)=1592778752
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
17/05/04 02:33:45 INFO terasort.TeraSort: done

real    5m58.139s
user    0m9.984s
sys     0m1.188s
[hdfs@ip-172-31-12-156 ~]$


