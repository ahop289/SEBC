[root@nodo2a jars]# su - angel-dev
Last login: Thu Nov 30 23:36:22 UTC 2017 on pts/0
[angel-dev@nodo2a ~]$ cd /opt/cloudera/parcels/CDH/jars/
[angel-dev@nodo2a jars]$ hadoop jar hadoop-examples.jar teragen 100000000 /user/angel-dev/terasort-input
17/11/30 23:39:08 INFO client.RMProxy: Connecting to ResourceManager at nodo4a.angel.com/10.1.0.7:8032
17/11/30 23:39:09 WARN security.UserGroupInformation: PriviledgedActionException as:angel-dev (auth:SIMPLE) cause:org.apache.hadoop.security.AccessControlException: Permission denied: user=angel-dev, access=WRITE, inode="/user/angel-dev":rodo-dev:supergroup:drwxr-xr-x
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.checkFsPermission(DefaultAuthorizationProvider.java:279)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.check(DefaultAuthorizationProvider.java:260)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.check(DefaultAuthorizationProvider.java:240)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.checkPermission(DefaultAuthorizationProvider.java:162)
        at org.apache.hadoop.hdfs.server.namenode.FSPermissionChecker.checkPermission(FSPermissionChecker.java:152)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkPermission(FSDirectory.java:3530)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkPermission(FSDirectory.java:3513)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkAncestorAccess(FSDirectory.java:3495)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.checkAncestorAccess(FSNamesystem.java:6651)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirsInternal(FSNamesystem.java:4421)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirsInt(FSNamesystem.java:4391)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirs(FSNamesystem.java:4364)
        at org.apache.hadoop.hdfs.server.namenode.NameNodeRpcServer.mkdirs(NameNodeRpcServer.java:873)
        at org.apache.hadoop.hdfs.server.namenode.AuthorizationProviderProxyClientProtocol.mkdirs(AuthorizationProviderProxyClientProtocol.java:323)
        at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolServerSideTranslatorPB.mkdirs(ClientNamenodeProtocolServerSideTranslatorPB.java:618)
        at org.apache.hadoop.hdfs.protocol.proto.ClientNamenodeProtocolProtos$ClientNamenodeProtocol$2.callBlockingMethod(ClientNamenodeProtocolProtos.java)
        at org.apache.hadoop.ipc.ProtobufRpcEngine$Server$ProtoBufRpcInvoker.call(ProtobufRpcEngine.java:617)
        at org.apache.hadoop.ipc.RPC$Server.call(RPC.java:1073)
        at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2217)
        at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2213)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:415)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1917)
        at org.apache.hadoop.ipc.Server$Handler.run(Server.java:2211)

org.apache.hadoop.security.AccessControlException: Permission denied: user=angel-dev, access=WRITE, inode="/user/angel-dev":rodo-dev:supergroup:drwxr-xr-x
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.checkFsPermission(DefaultAuthorizationProvider.java:279)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.check(DefaultAuthorizationProvider.java:260)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.check(DefaultAuthorizationProvider.java:240)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.checkPermission(DefaultAuthorizationProvider.java:162)
        at org.apache.hadoop.hdfs.server.namenode.FSPermissionChecker.checkPermission(FSPermissionChecker.java:152)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkPermission(FSDirectory.java:3530)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkPermission(FSDirectory.java:3513)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkAncestorAccess(FSDirectory.java:3495)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.checkAncestorAccess(FSNamesystem.java:6651)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirsInternal(FSNamesystem.java:4421)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirsInt(FSNamesystem.java:4391)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirs(FSNamesystem.java:4364)
        at org.apache.hadoop.hdfs.server.namenode.NameNodeRpcServer.mkdirs(NameNodeRpcServer.java:873)
        at org.apache.hadoop.hdfs.server.namenode.AuthorizationProviderProxyClientProtocol.mkdirs(AuthorizationProviderProxyClientProtocol.java:323)
        at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolServerSideTranslatorPB.mkdirs(ClientNamenodeProtocolServerSideTranslatorPB.java:618)
        at org.apache.hadoop.hdfs.protocol.proto.ClientNamenodeProtocolProtos$ClientNamenodeProtocol$2.callBlockingMethod(ClientNamenodeProtocolProtos.java)
        at org.apache.hadoop.ipc.ProtobufRpcEngine$Server$ProtoBufRpcInvoker.call(ProtobufRpcEngine.java:617)
        at org.apache.hadoop.ipc.RPC$Server.call(RPC.java:1073)
        at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2217)
        at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2213)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:415)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1917)
        at org.apache.hadoop.ipc.Server$Handler.run(Server.java:2211)

        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:57)
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)
        at java.lang.reflect.Constructor.newInstance(Constructor.java:526)
        at org.apache.hadoop.ipc.RemoteException.instantiateException(RemoteException.java:106)
        at org.apache.hadoop.ipc.RemoteException.unwrapRemoteException(RemoteException.java:73)
        at org.apache.hadoop.hdfs.DFSClient.primitiveMkdir(DFSClient.java:3115)
        at org.apache.hadoop.hdfs.DFSClient.mkdirs(DFSClient.java:3080)
        at org.apache.hadoop.hdfs.DistributedFileSystem$19.doCall(DistributedFileSystem.java:1001)
        at org.apache.hadoop.hdfs.DistributedFileSystem$19.doCall(DistributedFileSystem.java:997)
        at org.apache.hadoop.fs.FileSystemLinkResolver.resolve(FileSystemLinkResolver.java:81)
        at org.apache.hadoop.hdfs.DistributedFileSystem.mkdirsInternal(DistributedFileSystem.java:997)
        at org.apache.hadoop.hdfs.DistributedFileSystem.mkdirs(DistributedFileSystem.java:989)
        at org.apache.hadoop.mapreduce.JobSubmissionFiles.getStagingDir(JobSubmissionFiles.java:133)
        at org.apache.hadoop.mapreduce.JobSubmitter.submitJobInternal(JobSubmitter.java:148)
        at org.apache.hadoop.mapreduce.Job$10.run(Job.java:1307)
        at org.apache.hadoop.mapreduce.Job$10.run(Job.java:1304)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:415)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1917)
        at org.apache.hadoop.mapreduce.Job.submit(Job.java:1304)
        at org.apache.hadoop.mapreduce.Job.waitForCompletion(Job.java:1325)
        at org.apache.hadoop.examples.terasort.TeraGen.run(TeraGen.java:305)
        at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
        at org.apache.hadoop.examples.terasort.TeraGen.main(TeraGen.java:309)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.util.ProgramDriver$ProgramDescription.invoke(ProgramDriver.java:71)
        at org.apache.hadoop.util.ProgramDriver.run(ProgramDriver.java:144)
        at org.apache.hadoop.examples.ExampleDriver.main(ExampleDriver.java:74)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.util.RunJar.run(RunJar.java:221)
        at org.apache.hadoop.util.RunJar.main(RunJar.java:136)
Caused by: org.apache.hadoop.ipc.RemoteException(org.apache.hadoop.security.AccessControlException): Permission denied: user=angel-dev, access=WRITE, inode="/user/angel-dev":rodo-dev:supergroup:drwxr-xr-x
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.checkFsPermission(DefaultAuthorizationProvider.java:279)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.check(DefaultAuthorizationProvider.java:260)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.check(DefaultAuthorizationProvider.java:240)
        at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.checkPermission(DefaultAuthorizationProvider.java:162)
        at org.apache.hadoop.hdfs.server.namenode.FSPermissionChecker.checkPermission(FSPermissionChecker.java:152)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkPermission(FSDirectory.java:3530)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkPermission(FSDirectory.java:3513)
        at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkAncestorAccess(FSDirectory.java:3495)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.checkAncestorAccess(FSNamesystem.java:6651)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirsInternal(FSNamesystem.java:4421)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirsInt(FSNamesystem.java:4391)
        at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirs(FSNamesystem.java:4364)
        at org.apache.hadoop.hdfs.server.namenode.NameNodeRpcServer.mkdirs(NameNodeRpcServer.java:873)
        at org.apache.hadoop.hdfs.server.namenode.AuthorizationProviderProxyClientProtocol.mkdirs(AuthorizationProviderProxyClientProtocol.java:323)
        at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolServerSideTranslatorPB.mkdirs(ClientNamenodeProtocolServerSideTranslatorPB.java:618)
        at org.apache.hadoop.hdfs.protocol.proto.ClientNamenodeProtocolProtos$ClientNamenodeProtocol$2.callBlockingMethod(ClientNamenodeProtocolProtos.java)
        at org.apache.hadoop.ipc.ProtobufRpcEngine$Server$ProtoBufRpcInvoker.call(ProtobufRpcEngine.java:617)
        at org.apache.hadoop.ipc.RPC$Server.call(RPC.java:1073)
        at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2217)
        at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2213)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:415)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1917)
        at org.apache.hadoop.ipc.Server$Handler.run(Server.java:2211)

        at org.apache.hadoop.ipc.Client.call(Client.java:1504)
        at org.apache.hadoop.ipc.Client.call(Client.java:1441)
        at org.apache.hadoop.ipc.ProtobufRpcEngine$Invoker.invoke(ProtobufRpcEngine.java:230)
        at com.sun.proxy.$Proxy16.mkdirs(Unknown Source)
        at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolTranslatorPB.mkdirs(ClientNamenodeProtocolTranslatorPB.java:558)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.io.retry.RetryInvocationHandler.invokeMethod(RetryInvocationHandler.java:260)
        at org.apache.hadoop.io.retry.RetryInvocationHandler.invoke(RetryInvocationHandler.java:104)
        at com.sun.proxy.$Proxy17.mkdirs(Unknown Source)
        at org.apache.hadoop.hdfs.DFSClient.primitiveMkdir(DFSClient.java:3113)
        ... 31 more
[angel-dev@nodo2a jars]$ exit
logout
[root@nodo2a jars]# HADOOP_USER_NAME=hdfs hdfs dfs -chown angel-dev /user/angel-dev
[root@nodo2a jars]# su - angel-dev
Last login: Thu Nov 30 23:37:50 UTC 2017 on pts/0
[angel-dev@nodo2a ~]$ cd /opt/cloudera/parcels/CDH/jars/
[angel-dev@nodo2a jars]$ hadoop jar hadoop-examples.jar teragen 100000000 /user/angel-dev/terasort-input
17/11/30 23:40:31 INFO client.RMProxy: Connecting to ResourceManager at nodo4a.angel.com/10.1.0.7:8032
17/11/30 23:40:31 INFO terasort.TeraGen: Generating 100000000 using 2
17/11/30 23:40:32 INFO mapreduce.JobSubmitter: number of splits:2
17/11/30 23:40:32 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512082519883_0001
17/11/30 23:40:32 INFO impl.YarnClientImpl: Submitted application application_1512082519883_0001
17/11/30 23:40:32 INFO mapreduce.Job: The url to track the job: http://nodo4a.angel.com:8088/proxy/application_1512082519883_0001/
17/11/30 23:40:32 INFO mapreduce.Job: Running job: job_1512082519883_0001
17/11/30 23:40:39 INFO mapreduce.Job: Job job_1512082519883_0001 running in uber mode : false
17/11/30 23:40:39 INFO mapreduce.Job:  map 0% reduce 0%
17/11/30 23:40:56 INFO mapreduce.Job:  map 7% reduce 0%
17/11/30 23:40:57 INFO mapreduce.Job:  map 14% reduce 0%
17/11/30 23:41:02 INFO mapreduce.Job:  map 16% reduce 0%
17/11/30 23:41:03 INFO mapreduce.Job:  map 18% reduce 0%
17/11/30 23:41:08 INFO mapreduce.Job:  map 23% reduce 0%
17/11/30 23:41:09 INFO mapreduce.Job:  map 28% reduce 0%
17/11/30 23:41:14 INFO mapreduce.Job:  map 31% reduce 0%
17/11/30 23:41:15 INFO mapreduce.Job:  map 34% reduce 0%
17/11/30 23:41:20 INFO mapreduce.Job:  map 35% reduce 0%
17/11/30 23:41:33 INFO mapreduce.Job:  map 36% reduce 0%
17/11/30 23:41:38 INFO mapreduce.Job:  map 38% reduce 0%
17/11/30 23:41:44 INFO mapreduce.Job:  map 39% reduce 0%
17/11/30 23:41:45 INFO mapreduce.Job:  map 40% reduce 0%
17/11/30 23:41:57 INFO mapreduce.Job:  map 42% reduce 0%
17/11/30 23:42:02 INFO mapreduce.Job:  map 43% reduce 0%
17/11/30 23:42:16 INFO mapreduce.Job:  map 44% reduce 0%
17/11/30 23:42:22 INFO mapreduce.Job:  map 45% reduce 0%
17/11/30 23:42:27 INFO mapreduce.Job:  map 46% reduce 0%
17/11/30 23:42:28 INFO mapreduce.Job:  map 48% reduce 0%
17/11/30 23:42:33 INFO mapreduce.Job:  map 52% reduce 0%
17/11/30 23:42:34 INFO mapreduce.Job:  map 55% reduce 0%
17/11/30 23:42:39 INFO mapreduce.Job:  map 60% reduce 0%
17/11/30 23:42:40 INFO mapreduce.Job:  map 65% reduce 0%
17/11/30 23:42:45 INFO mapreduce.Job:  map 69% reduce 0%
17/11/30 23:42:46 INFO mapreduce.Job:  map 73% reduce 0%
17/11/30 23:42:51 INFO mapreduce.Job:  map 74% reduce 0%
17/11/30 23:42:58 INFO mapreduce.Job:  map 75% reduce 0%
17/11/30 23:43:17 INFO mapreduce.Job:  map 77% reduce 0%
17/11/30 23:43:28 INFO mapreduce.Job:  map 78% reduce 0%
17/11/30 23:43:52 INFO mapreduce.Job:  map 89% reduce 0%
17/11/30 23:43:58 INFO mapreduce.Job:  map 97% reduce 0%
17/11/30 23:44:03 INFO mapreduce.Job:  map 100% reduce 0%
17/11/30 23:44:03 INFO mapreduce.Job: Job job_1512082519883_0001 completed successfully
17/11/30 23:44:03 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=294032
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=170
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=400516
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=400516
                Total vcore-milliseconds taken by all map tasks=400516
                Total megabyte-milliseconds taken by all map tasks=410128384
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=170
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1260
                CPU time spent (ms)=153120
                Physical memory (bytes) snapshot=459685888
                Virtual memory (bytes) snapshot=3177529344
                Total committed heap usage (bytes)=878182400
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000
[angel-dev@nodo2a jars]$ hdfs dfs -ls -h terasort-input
Found 3 items
-rw-r--r--   3 angel-dev supergroup          0 2017-11-30 23:44 terasort-input/_SUCCESS
-rw-r--r--   3 angel-dev supergroup      4.7 G 2017-11-30 23:44 terasort-input/part-m-00000
-rw-r--r--   3 angel-dev supergroup      4.7 G 2017-11-30 23:43 terasort-input/part-m-00001
[angel-dev@nodo2a jars]$ hdfs dfs -rm -r      terasort-input
17/11/30 23:51:55 INFO fs.TrashPolicyDefault: Moved: 'hdfs://nameservice1/user/angel-dev/terasort-input' to trash at: hdfs://nameservice1/user/angel-dev/.Trash/Current/user/angel-dev/terasort-input
[angel-dev@nodo2a jars]$ hadoop jar hadoop-examples.jar terasort /user/angel-dev/terasort-input /user/angel-dev/terasort-output
17/11/30 23:54:25 INFO terasort.TeraSort: starting
17/11/30 23:54:26 ERROR terasort.TeraSort: Input path does not exist: hdfs://nameservice1/user/angel-dev/terasort-input
[angel-dev@nodo2a jars]$ hadoop jar hadoop-examples.jar teragen 100000000 /user/angel-dev/terasort-input
17/11/30 23:56:46 INFO client.RMProxy: Connecting to ResourceManager at nodo4a.angel.com/10.1.0.7:8032
17/11/30 23:56:47 INFO terasort.TeraGen: Generating 100000000 using 2
17/11/30 23:56:47 INFO mapreduce.JobSubmitter: number of splits:2
17/11/30 23:56:47 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512082519883_0002
17/11/30 23:56:47 INFO impl.YarnClientImpl: Submitted application application_1512082519883_0002
17/11/30 23:56:47 INFO mapreduce.Job: The url to track the job: http://nodo4a.angel.com:8088/proxy/application_1512082519883_0002/
17/11/30 23:56:47 INFO mapreduce.Job: Running job: job_1512082519883_0002
17/11/30 23:56:53 INFO mapreduce.Job: Job job_1512082519883_0002 running in uber mode : false
17/11/30 23:56:53 INFO mapreduce.Job:  map 0% reduce 0%
17/11/30 23:57:11 INFO mapreduce.Job:  map 14% reduce 0%
17/11/30 23:57:17 INFO mapreduce.Job:  map 23% reduce 0%
17/11/30 23:57:23 INFO mapreduce.Job:  map 30% reduce 0%
17/11/30 23:57:29 INFO mapreduce.Job:  map 32% reduce 0%
17/11/30 23:57:35 INFO mapreduce.Job:  map 34% reduce 0%
17/11/30 23:57:47 INFO mapreduce.Job:  map 35% reduce 0%
17/11/30 23:58:27 INFO mapreduce.Job:  map 40% reduce 0%
17/11/30 23:58:33 INFO mapreduce.Job:  map 46% reduce 0%
17/11/30 23:58:34 INFO mapreduce.Job:  map 57% reduce 0%
17/11/30 23:58:39 INFO mapreduce.Job:  map 61% reduce 0%
17/11/30 23:58:40 INFO mapreduce.Job:  map 65% reduce 0%
17/11/30 23:58:45 INFO mapreduce.Job:  map 66% reduce 0%
17/11/30 23:58:46 INFO mapreduce.Job:  map 67% reduce 0%
17/11/30 23:58:51 INFO mapreduce.Job:  map 68% reduce 0%
17/11/30 23:58:57 INFO mapreduce.Job:  map 69% reduce 0%
17/11/30 23:59:04 INFO mapreduce.Job:  map 70% reduce 0%
17/11/30 23:59:09 INFO mapreduce.Job:  map 71% reduce 0%
17/11/30 23:59:10 INFO mapreduce.Job:  map 73% reduce 0%
17/11/30 23:59:15 INFO mapreduce.Job:  map 74% reduce 0%
17/11/30 23:59:29 INFO mapreduce.Job:  map 75% reduce 0%
17/11/30 23:59:36 INFO mapreduce.Job:  map 77% reduce 0%
17/11/30 23:59:41 INFO mapreduce.Job:  map 79% reduce 0%
17/11/30 23:59:47 INFO mapreduce.Job:  map 81% reduce 0%
17/11/30 23:59:48 INFO mapreduce.Job:  map 83% reduce 0%
17/11/30 23:59:53 INFO mapreduce.Job:  map 85% reduce 0%
17/11/30 23:59:54 INFO mapreduce.Job:  map 87% reduce 0%
17/11/30 23:59:59 INFO mapreduce.Job:  map 90% reduce 0%
17/12/01 00:00:00 INFO mapreduce.Job:  map 94% reduce 0%
17/12/01 00:00:03 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 00:00:04 INFO mapreduce.Job: Job job_1512082519883_0002 completed successfully
17/12/01 00:00:04 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=294032
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=170
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=374479
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=374479
                Total vcore-milliseconds taken by all map tasks=374479
                Total megabyte-milliseconds taken by all map tasks=383466496
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=170
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=966
                CPU time spent (ms)=136780
                Physical memory (bytes) snapshot=406585344
                Virtual memory (bytes) snapshot=3194556416
                Total committed heap usage (bytes)=812646400
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000
[angel-dev@nodo2a jars]$ hdfs dfs -ls -h terasort-input
Found 3 items
-rw-r--r--   3 angel-dev supergroup          0 2017-12-01 00:00 terasort-input/_SUCCESS
-rw-r--r--   3 angel-dev supergroup      4.7 G 2017-12-01 00:00 terasort-input/part-m-00000
-rw-r--r--   3 angel-dev supergroup      4.7 G 2017-12-01 00:00 terasort-input/part-m-00001
[angel-dev@nodo2a jars]$ hadoop jar hadoop-examples.jar terasort /user/USER-dev/terasort-input /user/USER-dev/terasort-output
17/12/01 00:01:29 INFO terasort.TeraSort: starting
17/12/01 00:01:30 ERROR terasort.TeraSort: Input path does not exist: hdfs://nameservice1/user/USER-dev/terasort-input
^C[angel-dev@nodo2a jars]$ hadoop jar hadoop-examples.jar terasort /user/angel-dev/terasort-input /user/angel-dev/terasort-output
17/12/01 00:01:47 INFO terasort.TeraSort: starting
17/12/01 00:01:49 INFO input.FileInputFormat: Total input paths to process : 2
Spent 193ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 197ms
Sampling 10 splits of 76
Making 12 from 100000 sampled records
Computing parititions took 648ms
Spent 847ms computing partitions.
17/12/01 00:01:49 INFO client.RMProxy: Connecting to ResourceManager at nodo4a.angel.com/10.1.0.7:8032
17/12/01 00:01:50 INFO mapreduce.JobSubmitter: number of splits:76
17/12/01 00:01:50 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512082519883_0003
17/12/01 00:01:50 INFO impl.YarnClientImpl: Submitted application application_1512082519883_0003
17/12/01 00:01:50 INFO mapreduce.Job: The url to track the job: http://nodo4a.angel.com:8088/proxy/application_1512082519883_0003/
17/12/01 00:01:50 INFO mapreduce.Job: Running job: job_1512082519883_0003
17/12/01 00:01:57 INFO mapreduce.Job: Job job_1512082519883_0003 running in uber mode : false
17/12/01 00:01:57 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 00:02:11 INFO mapreduce.Job:  map 3% reduce 0%
17/12/01 00:02:12 INFO mapreduce.Job:  map 7% reduce 0%
17/12/01 00:02:15 INFO mapreduce.Job:  map 13% reduce 0%
17/12/01 00:02:16 INFO mapreduce.Job:  map 22% reduce 0%
17/12/01 00:02:17 INFO mapreduce.Job:  map 25% reduce 0%
17/12/01 00:02:18 INFO mapreduce.Job:  map 26% reduce 0%
17/12/01 00:02:24 INFO mapreduce.Job:  map 30% reduce 0%
17/12/01 00:02:25 INFO mapreduce.Job:  map 33% reduce 0%
17/12/01 00:02:31 INFO mapreduce.Job:  map 34% reduce 0%
17/12/01 00:02:32 INFO mapreduce.Job:  map 38% reduce 0%
17/12/01 00:02:33 INFO mapreduce.Job:  map 47% reduce 0%
17/12/01 00:02:34 INFO mapreduce.Job:  map 53% reduce 0%
17/12/01 00:02:36 INFO mapreduce.Job:  map 55% reduce 0%
17/12/01 00:02:37 INFO mapreduce.Job:  map 57% reduce 0%
17/12/01 00:02:38 INFO mapreduce.Job:  map 59% reduce 0%
17/12/01 00:02:48 INFO mapreduce.Job:  map 63% reduce 0%
17/12/01 00:02:49 INFO mapreduce.Job:  map 71% reduce 0%
17/12/01 00:02:50 INFO mapreduce.Job:  map 78% reduce 0%
17/12/01 00:02:51 INFO mapreduce.Job:  map 83% reduce 0%
17/12/01 00:02:52 INFO mapreduce.Job:  map 86% reduce 0%
17/12/01 00:02:58 INFO mapreduce.Job:  map 87% reduce 0%
17/12/01 00:03:01 INFO mapreduce.Job:  map 91% reduce 0%
17/12/01 00:03:02 INFO mapreduce.Job:  map 92% reduce 0%
17/12/01 00:03:05 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 00:03:10 INFO mapreduce.Job:  map 100% reduce 8%
17/12/01 00:03:11 INFO mapreduce.Job:  map 100% reduce 14%
17/12/01 00:03:12 INFO mapreduce.Job:  map 100% reduce 23%
17/12/01 00:03:14 INFO mapreduce.Job:  map 100% reduce 26%
17/12/01 00:03:15 INFO mapreduce.Job:  map 100% reduce 28%
17/12/01 00:03:16 INFO mapreduce.Job:  map 100% reduce 29%
17/12/01 00:03:17 INFO mapreduce.Job:  map 100% reduce 38%
17/12/01 00:03:18 INFO mapreduce.Job:  map 100% reduce 46%
17/12/01 00:03:19 INFO mapreduce.Job:  map 100% reduce 49%
17/12/01 00:03:20 INFO mapreduce.Job:  map 100% reduce 53%
17/12/01 00:03:22 INFO mapreduce.Job:  map 100% reduce 58%
17/12/01 00:03:23 INFO mapreduce.Job:  map 100% reduce 63%
17/12/01 00:03:24 INFO mapreduce.Job:  map 100% reduce 68%
17/12/01 00:03:25 INFO mapreduce.Job:  map 100% reduce 70%
17/12/01 00:03:27 INFO mapreduce.Job:  map 100% reduce 73%
17/12/01 00:03:28 INFO mapreduce.Job:  map 100% reduce 74%
17/12/01 00:03:29 INFO mapreduce.Job:  map 100% reduce 75%
17/12/01 00:03:30 INFO mapreduce.Job:  map 100% reduce 76%
17/12/01 00:03:31 INFO mapreduce.Job:  map 100% reduce 77%
17/12/01 00:03:35 INFO mapreduce.Job:  map 100% reduce 78%
17/12/01 00:03:36 INFO mapreduce.Job:  map 100% reduce 79%
17/12/01 00:03:41 INFO mapreduce.Job:  map 100% reduce 80%
17/12/01 00:03:42 INFO mapreduce.Job:  map 100% reduce 81%
17/12/01 00:03:45 INFO mapreduce.Job:  map 100% reduce 82%
17/12/01 00:03:46 INFO mapreduce.Job:  map 100% reduce 83%
17/12/01 00:03:47 INFO mapreduce.Job:  map 100% reduce 84%
17/12/01 00:03:48 INFO mapreduce.Job:  map 100% reduce 85%
17/12/01 00:03:50 INFO mapreduce.Job:  map 100% reduce 86%
17/12/01 00:04:01 INFO mapreduce.Job:  map 100% reduce 87%
17/12/01 00:04:15 INFO mapreduce.Job:  map 100% reduce 89%
17/12/01 00:04:17 INFO mapreduce.Job:  map 100% reduce 90%
17/12/01 00:04:18 INFO mapreduce.Job:  map 100% reduce 92%
17/12/01 00:04:19 INFO mapreduce.Job:  map 100% reduce 94%
17/12/01 00:04:24 INFO mapreduce.Job:  map 100% reduce 95%
17/12/01 00:04:25 INFO mapreduce.Job:  map 100% reduce 96%
17/12/01 00:04:34 INFO mapreduce.Job:  map 100% reduce 97%
17/12/01 00:04:38 INFO mapreduce.Job:  map 100% reduce 100%
17/12/01 00:04:39 INFO mapreduce.Job: Job job_1512082519883_0003 completed successfully
17/12/01 00:04:39 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4444901452
                FILE: Number of bytes written=8828848298
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000009652
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=264
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=24
        Job Counters
                Launched map tasks=76
                Launched reduce tasks=12
                Data-local map tasks=76
                Total time spent by all maps in occupied slots (ms)=1098090
                Total time spent by all reduces in occupied slots (ms)=1107474
                Total time spent by all map tasks (ms)=1098090
                Total time spent by all reduce tasks (ms)=1107474
                Total vcore-milliseconds taken by all map tasks=1098090
                Total vcore-milliseconds taken by all reduce tasks=1107474
                Total megabyte-milliseconds taken by all map tasks=1124444160
                Total megabyte-milliseconds taken by all reduce tasks=1134053376
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4370860826
                Input split bytes=9652
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4370860826
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =912
                Failed Shuffles=0
                Merged Map outputs=912
                GC time elapsed (ms)=20696
                CPU time spent (ms)=1026770
                Physical memory (bytes) snapshot=56016818176
                Virtual memory (bytes) snapshot=140739756032
                Total committed heap usage (bytes)=56337891328
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
17/12/01 00:04:39 INFO terasort.TeraSort: done
[angel-dev@nodo2a jars]$ hadoop jar hadoop-examples.jar teravalidate /user/USER-dev/terasort-output /user/USER-dev/terasort-validate
17/12/01 00:05:55 INFO client.RMProxy: Connecting to ResourceManager at nodo4a.angel.com/10.1.0.7:8032
17/12/01 00:05:56 INFO mapreduce.JobSubmitter: Cleaning up the staging area /user/angel-dev/.staging/job_1512082519883_0004
17/12/01 00:05:56 WARN security.UserGroupInformation: PriviledgedActionException as:angel-dev (auth:SIMPLE) cause:org.apache.hadoop.mapreduce.lib.input.InvalidInputException: Input path does not exist: hdfs://nameservice1/user/USER-dev/terasort-output
org.apache.hadoop.mapreduce.lib.input.InvalidInputException: Input path does not exist: hdfs://nameservice1/user/USER-dev/terasort-output
        at org.apache.hadoop.mapreduce.lib.input.FileInputFormat.singleThreadedListStatus(FileInputFormat.java:323)
        at org.apache.hadoop.mapreduce.lib.input.FileInputFormat.listStatus(FileInputFormat.java:265)
        at org.apache.hadoop.mapreduce.lib.input.FileInputFormat.getSplits(FileInputFormat.java:387)
        at org.apache.hadoop.examples.terasort.TeraInputFormat.getSplits(TeraInputFormat.java:294)
        at org.apache.hadoop.mapreduce.JobSubmitter.writeNewSplits(JobSubmitter.java:305)
        at org.apache.hadoop.mapreduce.JobSubmitter.writeSplits(JobSubmitter.java:322)
        at org.apache.hadoop.mapreduce.JobSubmitter.submitJobInternal(JobSubmitter.java:200)
        at org.apache.hadoop.mapreduce.Job$10.run(Job.java:1307)
        at org.apache.hadoop.mapreduce.Job$10.run(Job.java:1304)
        at java.security.AccessController.doPrivileged(Native Method)
        at javax.security.auth.Subject.doAs(Subject.java:415)
        at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1917)
        at org.apache.hadoop.mapreduce.Job.submit(Job.java:1304)
        at org.apache.hadoop.mapreduce.Job.waitForCompletion(Job.java:1325)
        at org.apache.hadoop.examples.terasort.TeraValidate.run(TeraValidate.java:178)
        at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
        at org.apache.hadoop.examples.terasort.TeraValidate.main(TeraValidate.java:185)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.util.ProgramDriver$ProgramDescription.invoke(ProgramDriver.java:71)
        at org.apache.hadoop.util.ProgramDriver.run(ProgramDriver.java:144)
        at org.apache.hadoop.examples.ExampleDriver.main(ExampleDriver.java:74)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.util.RunJar.run(RunJar.java:221)
        at org.apache.hadoop.util.RunJar.main(RunJar.java:136)
[angel-dev@nodo2a jars]$ hadoop jar hadoop-examples.jar teravalidate /user/angel-dev/terasort-output /user/angel-dev/terasort-validate
17/12/01 00:06:21 INFO client.RMProxy: Connecting to ResourceManager at nodo4a.angel.com/10.1.0.7:8032
17/12/01 00:06:22 INFO input.FileInputFormat: Total input paths to process : 12
Spent 41ms computing base-splits.
Spent 10ms computing TeraScheduler splits.
17/12/01 00:06:22 INFO mapreduce.JobSubmitter: number of splits:12
17/12/01 00:06:22 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512082519883_0005
17/12/01 00:06:22 INFO impl.YarnClientImpl: Submitted application application_1512082519883_0005
17/12/01 00:06:22 INFO mapreduce.Job: The url to track the job: http://nodo4a.angel.com:8088/proxy/application_1512082519883_0005/
17/12/01 00:06:22 INFO mapreduce.Job: Running job: job_1512082519883_0005
17/12/01 00:06:27 INFO mapreduce.Job: Job job_1512082519883_0005 running in uber mode : false
17/12/01 00:06:27 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 00:06:41 INFO mapreduce.Job:  map 25% reduce 0%
17/12/01 00:06:42 INFO mapreduce.Job:  map 58% reduce 0%
17/12/01 00:06:45 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 00:06:50 INFO mapreduce.Job:  map 100% reduce 100%
17/12/01 00:06:50 INFO mapreduce.Job: Job job_1512082519883_0005 completed successfully
17/12/01 00:06:50 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=680
                FILE: Number of bytes written=1918733
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000001536
                HDFS: Number of bytes written=25
                HDFS: Number of read operations=39
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=2
        Job Counters
                Launched map tasks=12
                Launched reduce tasks=1
                Data-local map tasks=8
                Rack-local map tasks=4
                Total time spent by all maps in occupied slots (ms)=155591
                Total time spent by all reduces in occupied slots (ms)=3043
                Total time spent by all map tasks (ms)=155591
                Total time spent by all reduce tasks (ms)=3043
                Total vcore-milliseconds taken by all map tasks=155591
                Total vcore-milliseconds taken by all reduce tasks=3043
                Total megabyte-milliseconds taken by all map tasks=159325184
                Total megabyte-milliseconds taken by all reduce tasks=3116032
        Map-Reduce Framework
                Map input records=100000000
                Map output records=36
                Map output bytes=984
                Map output materialized bytes=1152
                Input split bytes=1536
                Combine input records=0
                Combine output records=0
                Reduce input groups=25
                Reduce shuffle bytes=1152
                Reduce input records=36
                Reduce output records=1
                Spilled Records=72
                Shuffled Maps =12
                Failed Shuffles=0
                Merged Map outputs=12
                GC time elapsed (ms)=2095
                CPU time spent (ms)=120940
                Physical memory (bytes) snapshot=7886938112
                Virtual memory (bytes) snapshot=20712841216
                Total committed heap usage (bytes)=7842824192
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
                Bytes Written=25
