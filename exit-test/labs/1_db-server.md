

JDBC CONNECTOR

	[root@ip-172-31-27-185 mysql-connector-java-5.1.6]# ls -lrth /usr/share/java
	total 688K
	-rw-r--r-- 1 root root 687K May 18 03:54 mysql-connector-java.jar
	[root@ip-172-31-27-185 mysql-connector-java-5.1.6]#

	[root@ip-172-31-27-211 mysql-connector-java-5.1.6]# ls -lrth /usr/share/java
	total 688K
	-rw-r--r-- 1 root root 687K May 18 04:07 mysql-connector-java.jar
	[root@ip-172-31-27-211 mysql-connector-java-5.1.6]#

	[root@ip-172-31-26-240 mysql-connector-java-5.1.6]# ls -lrth /usr/share/java
	total 688K
	-rw-r--r-- 1 root root 687K May 18 04:10 mysql-connector-java.jar
	[root@ip-172-31-26-240 mysql-connector-java-5.1.6]#

	[root@ip-172-31-25-196 mysql-connector-java-5.1.6]# ls -lrth /usr/share/java
	total 688K
	-rw-r--r-- 1 root root 687K May 18 04:11 mysql-connector-java.jar
	[root@ip-172-31-25-196 mysql-connector-java-5.1.6]#

	[root@ip-172-31-21-116 mysql-connector-java-5.1.6]# ls -lrth /usr/share/java
	total 688K
	-rw-r--r-- 1 root root 687K May 18 04:12 mysql-connector-java.jar
	[root@ip-172-31-21-116 mysql-connector-java-5.1.6]#

	MariaDB [(none)]> create database scm DEFAULT CHARACTER SET utf8;
	Query OK, 1 row affected (0.00 sec)

	MariaDB [(none)]> grant all on scm.* TO 'scm'@'%' identified by 'scm_password';
	Query OK, 0 rows affected (0.00 sec)


DATABASES CREATION

	MariaDB [(none)]> create database rman DEFAULT CHARACTER SET utf8;
	Query OK, 1 row affected (0.00 sec)

	MariaDB [(none)]> grant all on rman.* TO 'rman'@'%' identified by 'rman_password';
	Query OK, 0 rows affected (0.00 sec)

	MariaDB [(none)]> create database hive DEFAULT CHARACTER SET utf8;
	Query OK, 1 row affected (0.00 sec)

	MariaDB [(none)]> grant all on hive.* TO 'hue'@'%' identified by 'hive_password';
	Query OK, 0 rows affected (0.00 sec)

	MariaDB [(none)]> create database oozie DEFAULT CHARACTER SET utf8;
	Query OK, 1 row affected (0.00 sec)

	MariaDB [(none)]> grant all on oozie.* TO 'oozie'@'%' identified by 'oozie_password';
	Query OK, 0 rows affected (0.00 sec)

	MariaDB [(none)]> create database hue DEFAULT CHARACTER SET utf8;
	Query OK, 1 row affected (0.00 sec)

	MariaDB [(none)]> grant all on hue.* TO 'hue'@'%' identified by 'hue_password';
	Query OK, 0 rows affected (0.00 sec)

	MariaDB [(none)]> create database sentry DEFAULT CHARACTER SET utf8;
	Query OK, 1 row affected (0.00 sec)

	MariaDB [(none)]> grant all on sentry.* TO 'sentry'@'%' identified by 'sentry_password';
	Query OK, 0 rows affected (0.00 sec)


HOSTNAME

	[root@ip-172-31-27-185 mysql-connector-java-5.1.6]# hostname -f
	ip-172-31-27-185.ap-southeast-1.compute.internal


DB STATUS

	[root@ip-172-31-27-185 mysql-connector-java-5.1.6]# mysql -u oozie -p oozie -e "status;"
	Enter password:
	ERROR 1045 (28000): Access denied for user 'oozie'@'localhost' (using password: YES)
	[root@ip-172-31-27-185 mysql-connector-java-5.1.6]#


SHOW DB
	
	[root@ip-172-31-27-185 mysql-connector-java-5.1.6]# mysql -u oozie -p oozie -e "show databases;"
	Enter password:
	+--------------------+
	| Database           |
	+--------------------+
	| information_schema |
	| oozie              |
	+--------------------+
	[root@ip-172-31-27-185 mysql-connector-java-5.1.6]#



