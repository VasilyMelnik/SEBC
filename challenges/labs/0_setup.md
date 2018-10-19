# Cloud Provide
Google Compute Engine
# OS version
Red Hat Enterprise Linux Server release 7.5 (Maipo)
# disk space
...
	[root@instance-13 ~]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/sda1        80G  2.8G   78G   4% /
	devtmpfs        7.3G     0  7.3G   0% /dev
	tmpfs           7.3G     0  7.3G   0% /dev/shm
	tmpfs           7.3G  8.5M  7.3G   1% /run
	tmpfs           7.3G     0  7.3G   0% /sys/fs/cgroup
	tmpfs           1.5G     0  1.5G   0% /run/user/0

	[root@instance-14 ~]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/sda1        80G  2.5G   78G   4% /
	devtmpfs        7.3G     0  7.3G   0% /dev
	tmpfs           7.3G     0  7.3G   0% /dev/shm
	tmpfs           7.3G  8.5M  7.3G   1% /run
	tmpfs           7.3G     0  7.3G   0% /sys/fs/cgroup
	tmpfs           1.5G     0  1.5G   0% /run/user/0

	[root@instance-15 ~]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/sda1        80G  2.5G   78G   4% /
	devtmpfs        7.3G     0  7.3G   0% /dev
	tmpfs           7.3G     0  7.3G   0% /dev/shm
	tmpfs           7.3G  8.5M  7.3G   1% /run
	tmpfs           7.3G     0  7.3G   0% /sys/fs/cgroup
	tmpfs           1.5G     0  1.5G   0% /run/user/0	

	[root@instance-16 ~]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/sda1        80G  2.5G   78G   4% /
	devtmpfs        7.3G     0  7.3G   0% /dev
	tmpfs           7.3G     0  7.3G   0% /dev/shm
	tmpfs           7.3G  8.5M  7.3G   1% /run
	tmpfs           7.3G     0  7.3G   0% /sys/fs/cgroup
	tmpfs           1.5G     0  1.5G   0% /run/user/0

	[root@instance-17 ~]# df -h
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/sda1        80G  2.5G   78G   4% /
	devtmpfs        7.3G     0  7.3G   0% /dev
	tmpfs           7.3G     0  7.3G   0% /dev/shm
	tmpfs           7.3G  8.5M  7.3G   1% /run
	tmpfs           7.3G     0  7.3G   0% /sys/fs/cgroup
	tmpfs           1.5G     0  1.5G   0% /run/user/0

...
# yum result
...
	[root@instance-13 ~]# yum repolist enabled
	repo id                                                   repo name                                                               status
	cloudera-manager                                          Cloudera Manager                                                             7
	epel/x86_64                                               Extra Packages for Enterprise Linux 7 - x86_64                          12,741
	google-cloud-compute                                      Google Cloud Compute                                                        11
	google-cloud-sdk                                          Google Cloud SDK                                                           354
	rhui-rhel-7-server-rhui-extras-rpms/x86_64                Red Hat Enterprise Linux 7 Server - Extras from RHUI (RPMs)                923
	rhui-rhel-7-server-rhui-optional-rpms/7Server/x86_64      Red Hat Enterprise Linux 7 Server - Optional from RHUI (RPMs)           15,399
	rhui-rhel-7-server-rhui-rh-common-rpms/7Server/x86_64     Red Hat Enterprise Linux 7 Server - RH Common from RHUI (RPMs)             234
	rhui-rhel-7-server-rhui-rpms/7Server/x86_64               Red Hat Enterprise Linux 7 Server from RHUI (RPMs)                      21,093
	rhui-rhel-7-server-rhui-supplementary-rpms/7Server/x86_64 Red Hat Enterprise Linux 7 Server - Supplementary from RHUI (RPMs)         280
	rhui-rhel-ha-for-rhel-7-server-rhui-rpms/7Server/x86_64   Red Hat Enterprise Linux High Availability (for RHEL 7 Server) (RPMs) f    500
	rhui-rhel-rs-for-rhel-7-server-rhui-rpms/7Server/x86_64   Red Hat Enterprise Linux Resilient Storage (for RHEL 7 Server) (RPMs) f    593
	rhui-rhel-server-rhui-rhscl-7-rpms/7Server/x86_64         Red Hat Software Collections RPMs for Red Hat Enterprise Linux 7 Server 10,509
	repolist: 62,644
...

# user add

	groupadd -g 2000 hotels  && useradd -G hotels fullerton && groupadd -g 2100 shops && useradd -G shops raffles
	[root@instance-17 ~]# cat /etc/passwd | grep raffles
	raffles:x:1003:1003::/home/raffles:/bin/bash
	[root@instance-17 ~]# cat /etc/passwd | grep fullerton
	fullerton:x:1002:2001::/home/fullerton:/bin/bash
	[root@instance-17 ~]# cat /etc/group | grep hotels
	hotels:x:2000:fullerton
	[root@instance-17 ~]# cat /etc/group | grep shops
	shops:x:2100:raffles