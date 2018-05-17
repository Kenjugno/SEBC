
List the cloud provider you are using
	AWS EC2 instances m4.xlarge

List your instances by IP address and DNS name

	ec2-54-254-131-32.ap-southeast-1.compute.amazonaws.com		
	ec2-54-169-200-109.ap-southeast-1.compute.amazonaws.com		
	ec2-54-169-16-143.ap-southeast-1.compute.amazonaws.com		
	ec2-13-229-128-120.ap-southeast-1.compute.amazonaws.com		
	ec2-52-221-208-27.ap-southeast-1.compute.amazonaws.com	


List the Linux release you are using

	[root@ip-172-31-25-119 etc]# cat /etc/redhat-release
	Red Hat Enterprise Linux Server release 7.5 (Maipo)

	[root@ip-172-31-25-119 etc]# uname -a
	Linux ip-172-31-25-119.ap-southeast-1.compute.internal 3.10.0-862.el7.x86_64 #1 SMP Wed Mar 21 18:14:51 EDT 2018 x86_64 x86_64 x86_64 GNU/Linux
	[root@ip-172-31-25-119 etc]#

List the file system capacity for the first node
	[root@ip-172-31-25-119 etc]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvda2       50G  3.0G   48G   6% /
	devtmpfs        7.8G     0  7.8G   0% /dev
	tmpfs           7.8G     0  7.8G   0% /dev/shm
	tmpfs           7.8G   17M  7.8G   1% /run
	tmpfs           7.8G     0  7.8G   0% /sys/fs/cgroup
	tmpfs           1.6G     0  1.6G   0% /run/user/1000
	tmpfs           1.6G     0  1.6G   0% /run/user/997	


List the command and output for yum repolist enabled

	[root@ip-172-31-25-119 yum.repos.d]# yum repolist enabled
	Loaded plugins: amazon-id, rhui-lb, search-disabled-repos	
	repo id                                               repo name                                                            status
	cloudera-director                                     Cloudera Director                                                         5
	cloudera-manager                                      Cloudera Manager                                                          7
	rhui-REGION-client-config-server-7/x86_64             Red Hat Update Infrastructure 2.0 Client Configuration Server 7           1
	rhui-REGION-rhel-server-releases/7Server/x86_64       Red Hat Enterprise Linux Server 7 (RPMs)                             20,399
	rhui-REGION-rhel-server-rh-common/7Server/x86_64      Red Hat Enterprise Linux Server 7 RH Common (RPMs)                      231
	repolist: 20,643
	[root@ip-172-31-25-119 yum.repos.d]

User jimenez with a UID of 2800
	useradd -u 2800 jimenez

User beltran with a UID of 2900
	useradd -u 2900 beltran

Create the group astros and add beltran to it
Create the group rangers and add jimenez to it

	[root@ip-172-31-25-119 yum.repos.d]# groupadd rangers
	[root@ip-172-31-25-119 yum.repos.d]# useradd -G rangers jimenez

	[root@ip-172-31-25-119 yum.repos.d]# groupadd astros
	[root@ip-172-31-25-119 yum.repos.d]# useradd -G astros beltran





