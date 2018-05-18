

DB COMMAND

	[root@ip-172-31-27-185 ~]# sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql -uroot -pqwerty123 scm scm scm

	JAVA_HOME=/usr/java/jdk1.8.0_121-cloudera
	Verifying that we can write to /etc/cloudera-scm-server
	Creating SCM configuration file in /etc/cloudera-scm-server
	Executing:  /usr/java/jdk1.8.0_121-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-		java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
	[                          main] DbCommandExecutor              INFO  Successfully connected to database.
	All done, your SCM database is configured correctly!
	[root@ip-172-31-27-185 ~]#