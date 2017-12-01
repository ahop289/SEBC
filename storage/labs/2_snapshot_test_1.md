[angel-dev@nodo2a ~]$ HADOOP_USER_NAME=hdfs hdfs dfs -rm /user/angel-dev/SEBC.zip
17/12/01 01:22:15 INFO fs.TrashPolicyDefault: Moved: 'hdfs://nameservice1/user/angel-dev/SEBC.zip' to trash at: hdfs://nameservice1/user/hdfs/.Trash/Current/user/angel-dev/SEBC.zip
rm: The directory /user/angel-dev/precious cannot be deleted since /user/angel-dev/precious is snapshottable and already has snapshots
[angel-dev@nodo2a ~]$ HADOOP_USER_NAME=hdfs hdfs dfs -cp /user/angel-dev/precious/.snapshot/sebc-hdfs-test/SEBC.zip /user/angel-dev/
