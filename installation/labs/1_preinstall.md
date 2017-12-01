vi /etc/selinux/config
reboot
sysctl -w vm.swappiness=1
vi /etc/sysctl.conf
	vm.swappiness=1
fdisk -l
fdisk /dev/sdd
fdisk /dev/sdc
mkfs.xfs -f /dev/sdd1
mkfs.xfs -f /dev/sdc1
mkdir /mnt/temp1
mkdir /mnt/temp2
mount /var/log/ /mnt/temp1
mount /opt/ /mnt/temp2
cp -a /var/log/ /mnt/temp1
cp -a /opt/ /mnt/temp2
vi /etc/fstab
	/dev/sdc1               /opt/       	xfs   noatime,defaults        0 0
	/dev/sdd1               /var/log/       xfs   noatime,defaults        0 0
echo never > /sys/kernel/mm/transparent_hugepage/defrag
echo never > /sys/kernel/mm/transparent_hugepage/enabled
chmod a+x /etc/rc.d/rc.local && sudo /etc/rc.d/rc.local
systemctl start rc-local 
systemctl enable rc-local
service firewalld stop
systemctl disable firewalld
yum install ntp -y
systemctl start ntpd
systemctl status ntpd
service tuned stop
systemctl disable tuned
service chronyd stop
systemctl disable chronyd
vi /etc/hosts
	10.1.0.4        nodo1a.angel.com        nodo1a
	10.1.0.5        nodo2a.angel.com        nodo2a
	10.1.0.6        nodo3a.angel.com        nodo3a
	10.1.0.7        nodo4a.angel.com        nodo4a
yum -y install dnsmasq
vi /etc/dnsmasq.conf
	# line 19: uncomment (never forward plain names)
	domain-needed
	# line 21: uncomment (never forward addresses in the non-routed address spaces)
	bogus-priv
	# line 41: uncomment (query with each server strictly in the order in resolv.conf)
	strict-order
	# line 123: uncomment (add domain name automatically)
	expand-hosts
	# line 133: add (define domain name)
	domain=angel.com
systemctl start dnsmasq 
systemctl enable dnsmasq 
#solo en nodos clientes
yum -y install bind-utils
dig dlp.srv.world. 
dig -x 10.0.0.30 
vi /etc/resolv.conf
	#antes del nameserver preconfigurado
	nameserver 10.1.0.4
dig -x 10.1.0.4
dig -x nodo1a
nmtui 
	#CONFIGURAR_HOST_NAMEANOMBRE_LARGO
hostname
	nodo1a.angel.com
getent hosts
wget https://dev.mysql.com/get/mysql57-community-release-el7-11.noarch.rpm
yum install ./mysql57-community-release-el7-11.noarch.rpm
yum install mysql
wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.44.tar.gz
tar zxvf mysql-connector-java-5.1.44.tar.gz
cp mysql-connector-java-5.1.44-bin.jar /usr/share/java/mysql-connector-java.jar
mkdir -p /usr/share/java/
sudo cp mysql-connector-java-5.1.31-bin.jar /usr/share/java/mysql-connector-java.jar

#MYSQL-SERVER (SOLO NODO UTILITY)
yum install mysql-server
service mysqld start
grep "temporary password" /var/log/mysqld.log
mysql_secure_installation
mysql -u root -p
	create database amon DEFAULT CHARACTER SET utf8;
	create database rman DEFAULT CHARACTER SET utf8;
	create database metastore DEFAULT CHARACTER SET utf8;
	create database sentry DEFAULT CHARACTER SET utf8;
	create database nav DEFAULT CHARACTER SET utf8;
	create database navms DEFAULT CHARACTER SET utf8;
	create database hue DEFAULT CHARACTER SET utf8;
	create database oozie DEFAULT CHARACTER SET utf8;
	create database scm DEFAULT CHARACTER SET utf8;
	grant all privileges on scm.* to 'cloudera'@'%' identified by 'C@paCuatro1.';
	grant all privileges on amon.* to 'amon'@'%' identified by 'C@paCuatro1.';
	grant all privileges on rman.* to 'rman'@'%' identified by 'C@paCuatro1.';
	grant all privileges on sentry.* to 'sentry'@'%' identified by 'C@paCuatro1.';
	grant all privileges on nav.* to 'nav'@'%' identified by 'C@paCuatro1.';
	grant all privileges on navms.* to 'navms'@'%' identified by 'C@paCuatro1.';
	grant all privileges on metastore.* to 'hive'@'%' identified by 'C@paCuatro1.';
	grant all on hue.* to 'hue'@'%' identified by 'C@paCuatro1.';
	grant all privileges on oozie.* to 'oozie'@'localhost' identified by 'C@paCuatro1.';
	grant all privileges on oozie.* to 'oozie'@'%' identified by 'C@paCuatro1.';
	FLUSH PRIVILEGES; 
vi /etc/cloudera-scm-server/db.properties
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
passwd root
vi /etc/yum.repos.d/cloudera.repo
	[cloudera-manager]
	# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 7 x86_64 
	name = Cloudera Manager

	baseurl = https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.12/

	gpgkey = https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera

	gpgcheck = 1
yum install oracle-j2sdk1.7
yum install cloudera-manager-daemons cloudera-manager-server
service cloudera-scm-server start