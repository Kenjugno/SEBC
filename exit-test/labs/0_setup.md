


AWS EC2 instances (m4.xlarge)

	ec2-13-250-2-67.ap-southeast-1.compute.amazonaws.com
	ec2-54-169-31-47.ap-southeast-1.compute.amazonaws.com
	ec2-52-221-193-187.ap-southeast-1.compute.amazonaws.com
	ec2-54-255-239-232.ap-southeast-1.compute.amazonaws.com
	ec2-13-229-84-53.ap-southeast-1.compute.amazonaws.com


UPTIME

	[ec2-user@ip-172-31-27-185 ~]$ uptime
 	03:04:48 up 14 min,  1 user,  load average: 0.00, 0.01, 0.05

	[ec2-user@ip-172-31-27-211 ~]$ uptime
 	03:05:26 up 15 min,  1 user,  load average: 0.08, 0.03, 0.05

	[ec2-user@ip-172-31-26-240 ~]$ uptime
	03:06:00 up 15 min,  1 user,  load average: 0.00, 0.01, 0.03

	[ec2-user@ip-172-31-25-196 ~]$ uptime
 	03:06:39 up 16 min,  1 user,  load average: 0.00, 0.01, 0.04

	[ec2-user@ip-172-31-21-116 ~]$ uptime
 	03:07:19 up 16 min,  1 user,  load average: 0.00, 0.01, 0.04


LINUX RELEASE

	[root@ip-172-31-27-185 ec2-user]# cat /etc/redhat-release
	Red Hat Enterprise Linux Server release 7.5 (Maipo)


FILE SYSTEM CAPACITY

	[root@ip-172-31-27-185 ec2-user]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvda2       50G  945M   50G   2% /
	devtmpfs        7.8G     0  7.8G   0% /dev
	tmpfs           7.8G     0  7.8G   0% /dev/shm
	tmpfs           7.8G   17M  7.8G   1% /run
	tmpfs           7.8G     0  7.8G   0% /sys/fs/cgroup
	tmpfs           1.6G     0  1.6G   0% /run/user/0
	tmpfs           1.6G     0  1.6G   0% /run/user/1000


YUM REPOLIST ENABLED

	[root@ip-172-31-27-185 ec2-user]# yum repolist enabled
	Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
	rhui-REGION-client-config-server-7                                                           | 2.9 kB  00:00:00
	rhui-REGION-rhel-server-releases                                                             | 3.5 kB  00:00:00
	rhui-REGION-rhel-server-rh-common                                                            | 3.8 kB  00:00:00
	(1/7): rhui-REGION-rhel-server-releases/7Server/x86_64/group                                 | 855 kB  00:00:00
	(2/7): rhui-REGION-client-config-server-7/x86_64/primary_db                                  | 2.5 kB  00:00:00
	(3/7): rhui-REGION-rhel-server-releases/7Server/x86_64/updateinfo                            | 2.8 MB  00:00:00
	(4/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/group                                |  104 B  00:00:00
	(5/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/updateinfo                           |  33 kB  00:00:00	
	(6/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/primary_db                           | 120 kB  00:00:00
	(7/7): rhui-REGION-rhel-server-releases/7Server/x86_64/primary_db                            |  51 MB  00:00:00
	repo id                                                repo name                                                              status
	rhui-REGION-client-config-server-7/x86_64              Red Hat Update Infrastructure 2.0 Client Configuration Server 7             1
	rhui-REGION-rhel-server-releases/7Server/x86_64        Red Hat Enterprise Linux Server 7 (RPMs)                               20,399
	rhui-REGION-rhel-server-rh-common/7Server/x86_64       Red Hat Enterprise Linux Server 7 RH Common (RPMs)                        231
	repolist: 20,631


USER ACCOUNTS (CREATED ON ALL NODES)

	[root@ip-172-31-27-185 ec2-user]# useradd -u 2500 thanos
	[root@ip-172-31-27-185 ec2-user]# useradd -u 2600 hulk
	[root@ip-172-31-27-185 ec2-user]# useradd -u 2700 groot
	[root@ip-172-31-27-185 ec2-user]# groupadd blackorder
	[root@ip-172-31-27-185 ec2-user]# groupadd avengers
	[root@ip-172-31-27-185 ec2-user]# usermod -g blackorder thanos
	[root@ip-172-31-27-185 ec2-user]# usermod -g avengers hulk
	[root@ip-172-31-27-185 ec2-user]# usermod -g avengers groot

	[root@ip-172-31-27-185 ec2-user]# id thanos
	uid=2500(thanos) gid=2701(blackorder) groups=2701(blackorder)
	[root@ip-172-31-27-185 ec2-user]# id hulk
	uid=2600(hulk) gid=2702(avengers) groups=2702(avengers)
	[root@ip-172-31-27-185 ec2-user]# id groot
	uid=2700(groot) gid=2702(avengers) groups=2702(avengers)


/ETC/PASSWD

	[root@ip-172-31-27-185 ec2-user]# egrep 'thanos|hulk|groot' /etc/passwd
	thanos:x:2500:2701::/home/thanos:/bin/bash
	hulk:x:2600:2702::/home/hulk:/bin/bash
	groot:x:2700:2702::/home/groot:/bin/bash

/ETC/GROUP

	[root@ip-172-31-27-185 ec2-user]# egrep 'thanos|hulk|groot' /etc/group
	thanos:x:2500:
	hulk:x:2600:
	groot:x:2700:
	[root@ip-172-31-27-185 ec2-user]#













	



