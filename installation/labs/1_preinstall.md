
1. Check vm.swappiness on all your nodes
Set the value to 1 if necessary


	[root@ip-172-31-24-143 ~]# cat /proc/sys/vm/swappiness
	30
	
	[root@ip-172-31-24-143 ~]# /sbin/sysctl -a | grep swappiness
	sysctl: reading key "net.ipv6.conf.all.stable_secret"
	sysctl: reading key "net.ipv6.conf.default.stable_secret"
	sysctl: reading key "net.ipv6.conf.eth0.stable_secret"
	sysctl: reading key "net.ipv6.conf.lo.stable_secret"
	vm.swappiness = 30
	



	[root@ip-172-31-24-143 ~]# echo 1 > /proc/sys/vm/swappiness
	[root@ip-172-31-24-143 ~]#  cat /proc/sys/vm/swappiness
	1
	[root@ip-172-31-24-143 ~]#
	
	
	##### INCLLUDE it in the /etc/sysctl.conf
	
	[root@ip-172-31-24-143 etc]# more /etc/sysctl.conf |grep -i swappiness
	vm.swappiness = 1
	[root@ip-172-31-24-143 etc]#



2. Show the mount attributes of your volume(s)

DF

	[ec2-user@ip-172-31-24-143 ~]$ df -h
	
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvda2       30G  945M   30G   4% /
	devtmpfs        7.8G     0  7.8G   0% /dev
	tmpfs           7.8G     0  7.8G   0% /dev/shm
	tmpfs           7.8G   17M  7.8G   1% /run
	tmpfs           7.8G     0  7.8G   0% /sys/fs/cgroup
	tmpfs           1.6G     0  1.6G   0% /run/user/0
	tmpfs           1.6G     0  1.6G   0% /run/user/1000
	[ec2-user@ip-172-31-24-143 ~]$


3. If you have ext-based volumes, list the reserve space setting
XFS volumes do not support reserve space

	LSBLK
	
	[ec2-user@ip-172-31-24-143 ~]$ lsblk -f
	
	NAME    FSTYPE LABEL UUID                                 MOUNTPOINT
	xvda
	+-xvda1
	+-xvda2 xfs          50a9826b-3a50-44d0-ad12-28f2056e9927 /



4. Disable transparent hugepage support

	HUGE PAGES
	
	[root@ip-172-31-24-143 etc]# cat /sys/kernel/mm/transparent_hugepage/enabled
	[always] madvise never
	
	[root@ip-172-31-24-143 etc]# cat /sys/kernel/mm/transparent_hugepage/defrag
	[always] madvise never
	
	[root@ip-172-31-24-143 etc]# echo never > /sys/kernel/mm/transparent_hugepage/enabled
	[root@ip-172-31-24-143 etc]# echo never > /sys/kernel/mm/transparent_hugepage/defrag
	
	[root@ip-172-31-24-143 etc]# ls -la /etc/rc.d/rc.local
	-rw-r--r--. 1 root root 473 Feb 20 15:47 /etc/rc.d/rc.local
	[root@ip-172-31-24-143 etc]# chmod +x /etc/rc.d/rc.local
	[root@ip-172-31-24-143 etc]# ls -la /etc/rc.d/rc.local
	-rwxr-xr-x. 1 root root 473 Feb 20 15:47 /etc/rc.d/rc.local
	
	
	
	[root@ip-172-31-24-143 etc]# systemctl stop tuned
	[root@ip-172-31-24-143 etc]# systemctl disable tuned
	


5. List your network interface configuration

[root@ip-172-31-24-143 etc]# hostnamectl

	   Static hostname: ip-172-31-24-143.ap-southeast-1.compute.internal
	         Icon name: computer-vm
	           Chassis: vm
	        Machine ID: a50c09915ca948cda4b0a9dfea42359b
	           Boot ID: d9b6bd7b4bf34d8eb768c46e44b92945
	    Virtualization: xen
	  Operating System: Red Hat Enterprise Linux Server 7.5 (Maipo)
	       CPE OS Name: cpe:/o:redhat:enterprise_linux:7.5:GA:server
	            Kernel: Linux 3.10.0-862.el7.x86_64
	      Architecture: x86-64



6. Show that forward and reverse host lookups are correctly resolved

	  NOTE: No available command installed
		For /etc/hosts, use getent	-> can also use (cat /etc/hosts)
		For DNS, use nslookup		


6. Show the nscd service is running

	  NOTE: No available command installed, but can use this to get the output
	
		#ps -ef|grep -i nscd


7. Show the ntpd service is running

	   NOTE: No available command installed
	
		#ntpq -p
#ps -ef|grep -i ntp