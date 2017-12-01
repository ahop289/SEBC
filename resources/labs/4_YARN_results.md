[angel-dev@nodo2a ~]$ HADOOP_USER_NAME=hdfs ./YARNtest.sh
Testing loop started on Fri Dec 1 06:42:04 UTC 2017

real    2m0.714s
user    0m5.244s
sys     0m0.365s
17/12/01 06:44:05 INFO terasort.TeraSort: starting
17/12/01 06:44:07 INFO input.FileInputFormat: Total input paths to process : 24
17/12/01 06:44:08 INFO client.RMProxy: Connecting to ResourceManager at nodo4a.angel.com/10.1.0.7:8032
17/12/01 06:44:08 INFO mapreduce.JobSubmitter: number of splits:48
17/12/01 06:44:08 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512094475170_0005
17/12/01 06:44:09 INFO impl.YarnClientImpl: Submitted application application_1512094475170_0005
17/12/01 06:44:09 INFO mapreduce.Job: The url to track the job: http://nodo4a.angel.com:8088/proxy/application_1512094475170_0005/
17/12/01 06:44:09 INFO mapreduce.Job: Running job: job_1512094475170_0005
17/12/01 06:44:15 INFO mapreduce.Job: Job job_1512094475170_0005 running in uber mode : false
17/12/01 06:44:15 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 06:44:25 INFO mapreduce.Job:  map 2% reduce 0%
17/12/01 06:44:30 INFO mapreduce.Job:  map 6% reduce 0%
17/12/01 06:44:31 INFO mapreduce.Job:  map 21% reduce 0%
17/12/01 06:44:32 INFO mapreduce.Job:  map 27% reduce 0%
17/12/01 06:44:33 INFO mapreduce.Job:  map 29% reduce 0%
17/12/01 06:44:40 INFO mapreduce.Job:  map 31% reduce 0%
17/12/01 06:44:44 INFO mapreduce.Job:  map 35% reduce 0%
17/12/01 06:44:45 INFO mapreduce.Job:  map 48% reduce 0%
17/12/01 06:44:46 INFO mapreduce.Job:  map 56% reduce 0%
17/12/01 06:44:47 INFO mapreduce.Job:  map 58% reduce 0%
17/12/01 06:44:54 INFO mapreduce.Job:  map 60% reduce 0%
17/12/01 06:44:57 INFO mapreduce.Job:  map 67% reduce 0%
17/12/01 06:44:58 INFO mapreduce.Job:  map 79% reduce 0%
17/12/01 06:44:59 INFO mapreduce.Job:  map 85% reduce 0%
17/12/01 06:45:01 INFO mapreduce.Job:  map 88% reduce 0%
17/12/01 06:45:06 INFO mapreduce.Job:  map 98% reduce 0%
17/12/01 06:45:09 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 06:45:18 INFO mapreduce.Job:  map 100% reduce 68%
17/12/01 06:45:24 INFO mapreduce.Job:  map 100% reduce 71%
17/12/01 06:45:30 INFO mapreduce.Job:  map 100% reduce 72%
17/12/01 06:45:36 INFO mapreduce.Job:  map 100% reduce 73%
17/12/01 06:45:42 INFO mapreduce.Job:  map 100% reduce 74%
17/12/01 06:45:48 INFO mapreduce.Job:  map 100% reduce 75%
17/12/01 06:46:00 INFO mapreduce.Job:  map 100% reduce 76%
17/12/01 06:46:06 INFO mapreduce.Job:  map 100% reduce 78%
17/12/01 06:46:21 INFO mapreduce.Job:  map 100% reduce 79%
17/12/01 06:46:27 INFO mapreduce.Job:  map 100% reduce 82%
17/12/01 06:46:33 INFO mapreduce.Job:  map 100% reduce 84%
17/12/01 06:46:39 INFO mapreduce.Job:  map 100% reduce 86%
17/12/01 06:46:45 INFO mapreduce.Job:  map 100% reduce 88%
17/12/01 06:46:51 INFO mapreduce.Job:  map 100% reduce 90%
17/12/01 06:46:57 INFO mapreduce.Job:  map 100% reduce 92%
17/12/01 06:47:03 INFO mapreduce.Job:  map 100% reduce 93%
17/12/01 06:47:09 INFO mapreduce.Job:  map 100% reduce 94%
17/12/01 06:47:15 INFO mapreduce.Job:  map 100% reduce 95%
17/12/01 06:47:21 INFO mapreduce.Job:  map 100% reduce 96%
17/12/01 06:47:28 INFO mapreduce.Job:  map 100% reduce 98%
17/12/01 06:47:34 INFO mapreduce.Job:  map 100% reduce 100%
17/12/01 06:47:34 INFO mapreduce.Job: Job job_1512094475170_0005 completed successfully
17/12/01 06:47:34 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2236152994
                FILE: Number of bytes written=4479600993
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120005856
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=147
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=2
        Job Counters
                Launched map tasks=48
                Launched reduce tasks=1
                Data-local map tasks=48
                Total time spent by all maps in occupied slots (ms)=549878
                Total time spent by all reduces in occupied slots (ms)=152817
                Total time spent by all map tasks (ms)=549878
                Total time spent by all reduce tasks (ms)=152817
                Total vcore-milliseconds taken by all map tasks=549878
                Total vcore-milliseconds taken by all reduce tasks=152817
                Total megabyte-milliseconds taken by all map tasks=563075072
                Total megabyte-milliseconds taken by all reduce tasks=156484608
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2236152994
                Input split bytes=5856
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2236152994
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =48
                Failed Shuffles=0
                Merged Map outputs=48
                GC time elapsed (ms)=22542
                CPU time spent (ms)=442950
                Physical memory (bytes) snapshot=24848826368
                Virtual memory (bytes) snapshot=56541519872
                Total committed heap usage (bytes)=20105920512
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
17/12/01 06:47:34 INFO terasort.TeraSort: done

real    3m29.518s
user    0m7.916s
sys     0m0.459s
Deleted /results/tg-10GB-24-1-512
Deleted /results/ts-10GB-24-1-512

real    1m40.700s
user    0m5.233s
sys     0m0.355s
17/12/01 06:49:24 INFO terasort.TeraSort: starting
17/12/01 06:49:25 INFO input.FileInputFormat: Total input paths to process : 24
17/12/01 06:49:26 INFO client.RMProxy: Connecting to ResourceManager at nodo4a.angel.com/10.1.0.7:8032
17/12/01 06:49:26 INFO mapreduce.JobSubmitter: number of splits:48
17/12/01 06:49:27 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512094475170_0007
17/12/01 06:49:27 INFO impl.YarnClientImpl: Submitted application application_1512094475170_0007
17/12/01 06:49:27 INFO mapreduce.Job: The url to track the job: http://nodo4a.angel.com:8088/proxy/application_1512094475170_0007/
17/12/01 06:49:27 INFO mapreduce.Job: Running job: job_1512094475170_0007
17/12/01 06:49:33 INFO mapreduce.Job: Job job_1512094475170_0007 running in uber mode : false
17/12/01 06:49:33 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 06:49:47 INFO mapreduce.Job:  map 4% reduce 0%
17/12/01 06:49:54 INFO mapreduce.Job:  map 13% reduce 0%
17/12/01 06:49:55 INFO mapreduce.Job:  map 14% reduce 0%
17/12/01 06:49:57 INFO mapreduce.Job:  map 15% reduce 0%
17/12/01 06:49:59 INFO mapreduce.Job:  map 21% reduce 0%
17/12/01 06:50:06 INFO mapreduce.Job:  map 23% reduce 0%
17/12/01 06:50:07 INFO mapreduce.Job:  map 29% reduce 0%
17/12/01 06:50:11 INFO mapreduce.Job:  map 31% reduce 0%
17/12/01 06:50:12 INFO mapreduce.Job:  map 38% reduce 0%
17/12/01 06:50:17 INFO mapreduce.Job:  map 44% reduce 0%
17/12/01 06:50:19 INFO mapreduce.Job:  map 46% reduce 0%
17/12/01 06:50:20 INFO mapreduce.Job:  map 48% reduce 0%
17/12/01 06:50:22 INFO mapreduce.Job:  map 54% reduce 0%
17/12/01 06:50:23 INFO mapreduce.Job:  map 56% reduce 0%
17/12/01 06:50:25 INFO mapreduce.Job:  map 63% reduce 0%
17/12/01 06:50:30 INFO mapreduce.Job:  map 65% reduce 0%
17/12/01 06:50:31 INFO mapreduce.Job:  map 67% reduce 0%
17/12/01 06:50:32 INFO mapreduce.Job:  map 69% reduce 0%
17/12/01 06:50:33 INFO mapreduce.Job:  map 79% reduce 0%
17/12/01 06:50:34 INFO mapreduce.Job:  map 81% reduce 0%
17/12/01 06:50:41 INFO mapreduce.Job:  map 88% reduce 0%
17/12/01 06:50:42 INFO mapreduce.Job:  map 90% reduce 0%
17/12/01 06:50:44 INFO mapreduce.Job:  map 92% reduce 0%
17/12/01 06:50:45 INFO mapreduce.Job:  map 98% reduce 0%
17/12/01 06:50:47 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 06:50:58 INFO mapreduce.Job:  map 100% reduce 11%
17/12/01 06:51:04 INFO mapreduce.Job:  map 100% reduce 16%
17/12/01 06:51:10 INFO mapreduce.Job:  map 100% reduce 21%
17/12/01 06:51:16 INFO mapreduce.Job:  map 100% reduce 26%
17/12/01 06:51:22 INFO mapreduce.Job:  map 100% reduce 32%
17/12/01 06:51:28 INFO mapreduce.Job:  map 100% reduce 67%
17/12/01 06:51:40 INFO mapreduce.Job:  map 100% reduce 68%
17/12/01 06:51:52 INFO mapreduce.Job:  map 100% reduce 69%
17/12/01 06:51:58 INFO mapreduce.Job:  map 100% reduce 70%
17/12/01 06:52:04 INFO mapreduce.Job:  map 100% reduce 72%
17/12/01 06:52:10 INFO mapreduce.Job:  map 100% reduce 76%
17/12/01 06:52:16 INFO mapreduce.Job:  map 100% reduce 79%
17/12/01 06:52:22 INFO mapreduce.Job:  map 100% reduce 82%
17/12/01 06:52:28 INFO mapreduce.Job:  map 100% reduce 84%
17/12/01 06:52:34 INFO mapreduce.Job:  map 100% reduce 86%
17/12/01 06:52:40 INFO mapreduce.Job:  map 100% reduce 89%
17/12/01 06:53:16 INFO mapreduce.Job:  map 100% reduce 91%
17/12/01 06:53:22 INFO mapreduce.Job:  map 100% reduce 92%
17/12/01 06:53:28 INFO mapreduce.Job:  map 100% reduce 94%
17/12/01 06:53:34 INFO mapreduce.Job:  map 100% reduce 98%
17/12/01 06:53:38 INFO mapreduce.Job:  map 100% reduce 100%
17/12/01 06:53:38 INFO mapreduce.Job: Job job_1512094475170_0007 completed successfully
17/12/01 06:53:38 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2280635097
                FILE: Number of bytes written=4524083439
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120005904
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=147
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=2
        Job Counters
                Launched map tasks=48
                Launched reduce tasks=1
                Data-local map tasks=46
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=1125546
                Total time spent by all reduces in occupied slots (ms)=349138
                Total time spent by all map tasks (ms)=562773
                Total time spent by all reduce tasks (ms)=174569
                Total vcore-milliseconds taken by all map tasks=562773
                Total vcore-milliseconds taken by all reduce tasks=174569
                Total megabyte-milliseconds taken by all map tasks=1152559104
                Total megabyte-milliseconds taken by all reduce tasks=357517312
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2236152994
                Input split bytes=5904
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2236152994
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =48
                Failed Shuffles=0
                Merged Map outputs=48
                GC time elapsed (ms)=4936
                CPU time spent (ms)=432420
                Physical memory (bytes) snapshot=29655953408
                Virtual memory (bytes) snapshot=120860045312
                Total committed heap usage (bytes)=30676090880
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
17/12/01 06:53:38 INFO terasort.TeraSort: done

real    4m15.060s
user    0m7.753s
sys     0m0.481s
Deleted /results/tg-10GB-24-1-2024
Deleted /results/ts-10GB-24-1-2024
Testing loop ended on Fri Dec 1 06:53:44 UTC 2017
