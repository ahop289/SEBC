Enumere el proveedor de la nube que está utilizando (AWS, GCE, Azure, CloudCat, otro)
Azure

Enumere sus instancias por dirección IP y nombre DNS (no lo use /etc/hostspara esto)
10.1.0.4        nodo1a.angel.com
10.1.0.5        nodo2a.angel.com
10.1.0.6        nodo3a.angel.com
10.1.0.7        nodo4a.angel.com 

Enumera la versión de Linux que estás usando
Red Hat 7.4

Listar la capacidad del sistema de archivos para el primer nodo
[root@nodo1a cloudera]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda2        32G  1.6G   30G   5% /
devtmpfs         16G     0   16G   0% /dev
tmpfs            16G     0   16G   0% /dev/shm
tmpfs            16G  8.4M   16G   1% /run
tmpfs            16G     0   16G   0% /sys/fs/cgroup
/dev/sda1       497M  103M  394M  21% /boot
/dev/sdb1        63G  2.1G   58G   4% /mnt/resource
tmpfs           3.2G     0  3.2G   0% /run/user/1000


Listar el comando y salida para yum repolist enabled
[root@nodo1a cloudera]# yum repolist enabled
Loaded plugins: langpacks, product-id, search-disabled-repos
repo id                                                          repo name             status
rhui-microsoft-azure-rhel7                                       Microsoft Azure RPMs       2
rhui-rhel-7-server-dotnet-rhui-debug-rpms/7Server/x86_64         dotNET on RHEL Debug      27
rhui-rhel-7-server-dotnet-rhui-rpms/7Server/x86_64               dotNET on RHEL RPMs f     63
rhui-rhel-7-server-dotnet-rhui-source-rpms/7Server/x86_64        dotNET on RHEL Source     32
rhui-rhel-7-server-rhui-debug-rpms/7Server/x86_64                Red Hat Enterprise Li  6,382
rhui-rhel-7-server-rhui-extras-debug-rpms/x86_64                 Red Hat Enterprise Li    126
rhui-rhel-7-server-rhui-extras-rpms/x86_64                       Red Hat Enterprise Li    709
rhui-rhel-7-server-rhui-extras-source-rpms/x86_64                Red Hat Enterprise Li    276
rhui-rhel-7-server-rhui-optional-debug-rpms/7Server/x86_64       Red Hat Enterprise Li  4,263
rhui-rhel-7-server-rhui-optional-rpms/7Server/x86_64             Red Hat Enterprise Li 13,030
rhui-rhel-7-server-rhui-optional-source-rpms/7Server/x86_64      Red Hat Enterprise Li  3,038
rhui-rhel-7-server-rhui-rh-common-debug-rpms/7Server/x86_64      Red Hat Enterprise Li     31
rhui-rhel-7-server-rhui-rh-common-rpms/7Server/x86_64            Red Hat Enterprise Li    228
rhui-rhel-7-server-rhui-rh-common-source-rpms/7Server/x86_64     Red Hat Enterprise Li     89
rhui-rhel-7-server-rhui-rpms/7Server/x86_64                      Red Hat Enterprise Li 17,720
rhui-rhel-7-server-rhui-source-rpms/7Server/x86_64               Red Hat Enterprise Li  5,185
rhui-rhel-7-server-rhui-supplementary-debug-rpms/7Server/x86_64  Red Hat Enterprise Li      0
rhui-rhel-7-server-rhui-supplementary-rpms/7Server/x86_64        Red Hat Enterprise Li    238
rhui-rhel-7-server-rhui-supplementary-source-rpms/7Server/x86_64 Red Hat Enterprise Li      8
rhui-rhel-server-rhui-rhscl-7-debug-rpms/7Server/x86_64          Red Hat Software Coll    570
rhui-rhel-server-rhui-rhscl-7-rpms/7Server/x86_64                Red Hat Software Coll  9,198
rhui-rhel-server-rhui-rhscl-7-source-rpms/7Server/x86_64         Red Hat Software Coll  3,841
repolist: 65,056

Add the following Linux accounts to all nodes
[root@nodo1a mysql-connector-java-5.1.44]# sudo more /etc/passwd
saturn:x:2800:2800::/home/saturn:/bin/bash
haley:x:2900:2900::/home/haley:/bin/bash

mysql> SHOW VARIABLES WHERE Variable_name IN ('hostname','port');
+---------------+------------------+
| Variable_name | Value            |
+---------------+------------------+
| hostname      | nodo1a.angel.com |
| port          | 3306             |
+---------------+------------------+
2 rows in set (0.00 sec)

mysql> SELECT version();
+-----------+
| version() |
+-----------+
| 5.7.20    |
+-----------+
1 row in set (0.00 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| hue                |
| metastore          |
| mysql              |
| nav                |
| navms              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
| sys                |
+--------------------+
13 rows in set (0.00 sec)


