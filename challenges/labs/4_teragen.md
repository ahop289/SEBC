[saturn@nodo3a ~]$ cd /usr/lib/hadoop-0.20-mapreduce/
[saturn@nodo3a hadoop-0.20-mapreduce]$ HADOOP_USER_NAME=hdfs hadoop jar hadoop-examples.jar teragen -D dfs.block.size=33554432 -D mapreduce.job.maps=12 65536000 /user/saturn/results/tgen
17/12/01 19:55:21 INFO client.RMProxy: Connecting to ResourceManager at nodo3a.angel.com/10.1.0.6:8032
17/12/01 19:55:22 INFO terasort.TeraSort: Generating 65536000 using 12
17/12/01 19:55:22 INFO mapreduce.JobSubmitter: number of splits:12
17/12/01 19:55:22 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/12/01 19:55:22 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512151535206_0005
17/12/01 19:55:22 INFO impl.YarnClientImpl: Submitted application application_1512151535206_0005
17/12/01 19:55:22 INFO mapreduce.Job: The url to track the job: http://nodo3a.angel.com:8088/proxy/application_1512151535206_0005/
17/12/01 19:55:22 INFO mapreduce.Job: Running job: job_1512151535206_0005
17/12/01 19:55:27 INFO mapreduce.Job: Job job_1512151535206_0005 running in uber mode : false
17/12/01 19:55:27 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 19:55:39 INFO mapreduce.Job:  map 14% reduce 0%
17/12/01 19:55:40 INFO mapreduce.Job:  map 40% reduce 0%
17/12/01 19:55:42 INFO mapreduce.Job:  map 48% reduce 0%
17/12/01 19:55:43 INFO mapreduce.Job:  map 68% reduce 0%
17/12/01 19:55:44 INFO mapreduce.Job:  map 69% reduce 0%
17/12/01 19:55:46 INFO mapreduce.Job:  map 89% reduce 0%
17/12/01 19:56:08 INFO mapreduce.Job:  map 90% reduce 0%
17/12/01 19:56:11 INFO mapreduce.Job:  map 91% reduce 0%
17/12/01 19:56:23 INFO mapreduce.Job:  map 92% reduce 0%
17/12/01 19:56:38 INFO mapreduce.Job:  map 93% reduce 0%
17/12/01 19:56:47 INFO mapreduce.Job:  map 94% reduce 0%
17/12/01 19:56:56 INFO mapreduce.Job:  map 95% reduce 0%
17/12/01 19:57:04 INFO mapreduce.Job:  map 96% reduce 0%
17/12/01 19:57:08 INFO mapreduce.Job:  map 98% reduce 0%
17/12/01 19:57:29 INFO mapreduce.Job:  map 99% reduce 0%
17/12/01 19:57:34 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 19:57:35 INFO mapreduce.Job: Job job_1512151535206_0005 completed successfully
17/12/01 19:57:35 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1467734
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
                Total time spent by all maps in occupied slots (ms)=1041753
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=1041753
                Total vcore-seconds taken by all map tasks=1041753
                Total megabyte-seconds taken by all map tasks=1066755072
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1025
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=2800
                CPU time spent (ms)=180180
                Physical memory (bytes) snapshot=4486856704
                Virtual memory (bytes) snapshot=19145478144
                Total committed heap usage (bytes)=7183269888
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000
