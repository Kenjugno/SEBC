The command hostname -f and its output
[root@ip-172-31-25-119 yum.repos.d]# hostname -f
ip-172-31-25-119.ap-southeast-1.compute.internal
[root@ip-172-31-25-119 yum.repos.d]#


The command mysql -u <user> -p<password> -e "status;" and its output

[root@ip-172-31-25-119 yum.repos.d]# mysql -u hue -phue_password -e "status;"
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          388
Current database:
Current user:           hue@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 2 hours 37 sec

Threads: 1  Questions: 75451  Slow queries: 0  Opens: 693  Flush tables: 2  Open tables: 27  Queries per second avg: 10.425
--------------




[root@ip-172-31-25-119 yum.repos.d]#


[root@ip-172-31-25-119 ec2-user]# mysql -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 2
Server version: 5.5.56-MariaDB MariaDB Server

Copyright (c) 2000, 2017, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> create database hue DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on hue.* TO 'hue'@'%' identified by 'hue_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database oozie DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on oozie.* TO 'oozie'@'%' identified by 'oozie_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database amon DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on amon.* TO 'amon'@'%' identified by 'amon_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database rman DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on rman.* TO 'rman'@'%' identified by 'rman_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database metastore DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.01 sec)

MariaDB [(none)]> grant all on metastore.* TO 'hive'@'%' identified by 'hive_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database sentry DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on sentry.* TO 'sentry'@'%' identified by 'sentry_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database nav DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on nav.* TO 'nav'@'%' identified by 'nav_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database navms DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.01 sec)

MariaDB [(none)]> grant all on navms.* TO 'navms'@'%' identified by 'navms_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]>
