
Copy the repo configuration you use to challenges/labs/1_my-database-server.repo.md


[root@ip-172-31-25-119 yum.repos.d]# yum info mariadb
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
Installed Packages
Name        : mariadb
Arch        : x86_64
Epoch       : 1
Version     : 5.5.56
Release     : 2.el7
Size        : 49 M
Repo        : installed
From repo   : rhui-REGION-rhel-server-releases
Summary     : A community developed branch of MySQL
URL         : http://mariadb.org
License     : GPLv2 with exceptions and LGPLv2 and BSD
Description : MariaDB is a community developed branch of MySQL.
            : MariaDB is a multi-user, multi-threaded SQL database server.
            : It is a client/server implementation consisting of a server daemon (mysqld)
            : and many different client programs and libraries. The base package
            : contains the standard MariaDB/MySQL client programs and generic MySQL files.

[root@ip-172-31-25-119 yum.repos.d]#




[root@ip-172-31-25-119 selinux]# yum -y install mariadb-server
	Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
	rhui-REGION-client-config-server-7                                                                    | 2.9 kB  00:00:00
	rhui-REGION-rhel-server-releases                                                                      | 3.5 kB  00:00:00
	rhui-REGION-rhel-server-rh-common                                                                     | 3.8 kB  00:00:00
	(1/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/group                                         |  104 B  00:00:00
	(2/7): rhui-REGION-client-config-server-7/x86_64/primary_db                                           | 2.5 kB  00:00:00
	(3/7): rhui-REGION-rhel-server-releases/7Server/x86_64/updateinfo                                     | 2.8 MB  00:00:00
	(4/7): rhui-REGION-rhel-server-releases/7Server/x86_64/group                                          | 855 kB  00:00:00
	(5/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/updateinfo                                    |  33 kB  00:00:00
	(6/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/primary_db                                    | 120 kB  00:00:00
	(7/7): rhui-REGION-rhel-server-releases/7Server/x86_64/primary_db                                     |  51 MB  00:00:00
	Resolving Dependencies
	--> Running transaction check
	---> Package mariadb-server.x86_64 1:5.5.56-2.el7 will be installed
	--> Processing Dependency: mariadb(x86-64) = 1:5.5.56-2.el7 for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: /usr/bin/perl for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: libaio.so.1(LIBAIO_0.1)(64bit) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: libaio.so.1(LIBAIO_0.4)(64bit) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(DBI) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(Data::Dumper) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(File::Basename) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(File::Copy) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(File::Path) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(File::Temp) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(Getopt::Long) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(POSIX) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(Sys::Hostname) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(strict) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl(vars) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl-DBD-MySQL for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: perl-DBI for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Processing Dependency: libaio.so.1()(64bit) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
	--> Running transaction check
