# The database type
# Currently 'mysql', 'postgresql' and 'oracle' are valid databases.
com.cloudera.cmf.db.type=mysql

# The database host
# If a non standard port is needed, use 'hostname:port'
com.cloudera.cmf.db.host=localhost

# The database name
com.cloudera.cmf.db.name=scm

# The database user
com.cloudera.cmf.db.user=cloudera

# The database user's password
com.cloudera.cmf.db.password=C@paCuatro1.

# The db setup type
# By default, it is set to INIT
# If scm-server uses Embedded DB then it is set to EMBEDDED
# If scm-server uses External DB then it is set to EXTERNAL
com.cloudera.cmf.db.setupType=EXTERNAL

Revision de correcta instalacion
[root@nodo2a mysql-connector-java-5.1.44]# service cloudera-scm-server status                /etc/init.d/cloudera-scm-server: line 109: pstree: command not found
 cloudera-scm-server.service - LSB: Cloudera SCM Server
   Loaded: loaded (/etc/rc.d/init.d/cloudera-scm-server; bad; vendor preset: disabled)
   Active: active (exited) since Fri 2017-12-01 16:41:23 UTC; 28min ago
     Docs: man:systemd-sysv-generator(8)
  Process: 12589 ExecStart=/etc/rc.d/init.d/cloudera-scm-server start (code=exited, status=0/SUCCESS)

Dec 01 16:41:17 nodo2a.angel.com systemd[1]: Starting LSB: Cloudera SCM Server...
Dec 01 16:41:17 nodo2a.angel.com cloudera-scm-server[12589]: /etc/rc.d/init.d/cloudera-sc...d
Dec 01 16:41:18 nodo2a.angel.com su[12613]: (to cloudera-scm) root on none
Dec 01 16:41:23 nodo2a.angel.com cloudera-scm-server[12589]: Starting cloudera-scm-server...]
Dec 01 16:41:23 nodo2a.angel.com systemd[1]: Started LSB: Cloudera SCM Server.
Hint: Some lines were ellipsized, use -l to show in full.