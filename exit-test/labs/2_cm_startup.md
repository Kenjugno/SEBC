
/etc/yum.repos.d

	[root@ip-172-31-27-185 ec2-user]# ls -la /etc/yum.repos.d
	total 32
	drwxr-xr-x.  2 root root  100 May 18 03:32 .
	drwxr-xr-x. 75 root root 8192 May 18 03:59 ..
	-rw-r--r--   1 root root  607 May 18 03:32 redhat-rhui-client-config.repo
	-rw-r--r--.  1 root root 8679 May 18 03:32 redhat-rhui.repo
	-rw-r--r--   1 root root   90 May 18 03:32 rhui-load-balancers.conf
	[root@ip-172-31-27-185 ec2-user]#

	
	[root@ip-172-31-27-185 ec2-user]# more /etc/yum.repos.d/cloudera-manager.repo
	[cloudera-manager]
	# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 7 x86_64
	name=Cloudera Manager
	baseurl=https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.11.2/
	gpgkey =https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera
	gpgcheck = 1

	[root@ip-172-31-27-185 ec2-user]#