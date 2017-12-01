Cracion de repositorio

[root@nodo2a mysql-connector-java-5.1.44]# ls /etc/yum.repos.d
cloudera.repo  mysql-community.repo  mysql-community-source.repo  redhat.repo  rh-cloud.repo
[root@nodo2a mysql-connector-java-5.1.44]# more /etc/yum.repos.d/cloudera.repo

[cloudera-manager]
# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 7 x86_64
name = Cloudera Manager

baseurl = https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.11/

gpgkey = https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera

gpgcheck = 1
------------------------------------------------------------------------------------------

Base de datos
mysql -u root -p

create database scm DEFAULT CHARACTER SET utf8;
grant all privileges on scm.* to 'cloudera'@'%' identified by 'C@paCuatro1.';

FLUSH PRIVILEGES; 
------------------------------------------------------------------------------------------

Edicion del archivo db.properties

vi /etc/cloudera-scm-server/db.properties
