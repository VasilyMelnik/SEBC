CM Install Lab

1. sysctl -w vm.swappiness=1
2. mount
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime,seclabel)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
devtmpfs on /dev type devtmpfs (rw,nosuid,seclabel,size=7609696k,nr_inodes=1902424,mode=755)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev,seclabel)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,seclabel,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,nodev,seclabel,mode=755)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,seclabel,mode=755)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,xattr,release_agent=/usr/lib/systemd/systemd-cgroups-agent,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,cpuacct,cpu)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,blkio)
cgroup on /sys/fs/cgroup/net_cls,net_prio type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,net_prio,net_cls)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,devices)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,perf_event)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,memory)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,freezer)
cgroup on /sys/fs/cgroup/pids type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,pids)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,cpuset)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,seclabel,hugetlb)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/sda1 on / type xfs (rw,relatime,seclabel,attr2,inode64,noquota)
selinuxfs on /sys/fs/selinux type selinuxfs (rw,relatime)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=23,pgrp=1,timeout=0,minproto=5,maxproto=5,direct,pipe_ino=8080)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime,seclabel)
mqueue on /dev/mqueue type mqueue (rw,relatime,seclabel)
tmpfs on /run/user/1001 type tmpfs (rw,nosuid,nodev,relatime,seclabel,size=1523488k,mode=700,uid=1001,gid=1002)
tmpfs on /run/user/0 type tmpfs (rw,nosuid,nodev,relatime,seclabel,size=1523488k,mode=700)

3. df -hT 
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/sda1      xfs        40G  2.2G   38G   6% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.3G     0  7.3G   0% /dev/shm
tmpfs          tmpfs     7.3G  8.5M  7.3G   1% /run
tmpfs          tmpfs     7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1001
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0


4. 
echo "echo never > /sys/kernel/mm/transparent_hugepage/enabled" >> /etc/rc.d/rc.local
echo "echo never > /sys/kernel/mm/transparent_hugepage/defrag" >> /etc/rc.d/rc.local
grub2-mkconfig -o /boot/grub2/grub.cfg

tuned-adm off
tuned-adm list
Available profiles:
- balanced                    - General non-specialized tuned profile
- desktop                     - Optimize for the desktop use-case
- latency-performance         - Optimize for deterministic performance at the cost of increased power consumption
- network-latency             - Optimize for deterministic performance at the cost of increased power consumption, focused on low latency network performance
- network-throughput          - Optimize for streaming network throughput, generally only necessary on older CPUs or 40G+ networks
- powersave                   - Optimize for low power consumption
- throughput-performance      - Broadly applicable tuning that provides excellent performance across a variety of common server workloads
- virtual-guest               - Optimize for running inside a virtual guest
- virtual-host                - Optimize for running KVM guests
No current active profile.

systemctl stop tuned
systemctl disable tuned

5. ifconfig -agent
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1460
        inet 10.166.0.3  netmask 255.255.255.255  broadcast 10.166.0.3
        inet6 fe80::4001:aff:fea6:3  prefixlen 64  scopeid 0x20<link>
        ether 42:01:0a:a6:00:03  txqueuelen 1000  (Ethernet)
        RX packets 6656  bytes 56861420 (54.2 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 5714  bytes 934170 (912.2 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 151  bytes 26848 (26.2 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 151  bytes 26848 (26.2 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
 
6. 
[root@instance-2 ~]# getent hosts instance-4
10.166.0.5      instance-4.europe-north1-a.c.cloudera-218907.internal
[root@instance-2 ~]# getent hosts 10.166.0.5
10.166.0.5      instance-4.europe-north1-a.c.cloudera-218907.internal

7. 
[root@instance-2 ~]# service nscd status
Redirecting to /bin/systemctl status nscd.service
? nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2018-10-15 13:10:49 UTC; 4s ago
  Process: 2776 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 2777 (nscd)
   CGroup: /system.slice/nscd.service
           L-2777 /usr/sbin/nscd

Oct 15 13:10:49 instance-2 nscd[2777]: 2777 monitoring file `/etc/hosts` (4)
Oct 15 13:10:49 instance-2 nscd[2777]: 2777 monitoring directory `/etc` (2)
Oct 15 13:10:49 instance-2 nscd[2777]: 2777 monitoring file `/etc/resolv.conf` (5)
Oct 15 13:10:49 instance-2 nscd[2777]: 2777 monitoring directory `/etc` (2)
Oct 15 13:10:49 instance-2 nscd[2777]: 2777 monitoring file `/etc/services` (6)
Oct 15 13:10:49 instance-2 nscd[2777]: 2777 monitoring directory `/etc` (2)
Oct 15 13:10:49 instance-2 nscd[2777]: 2777 disabled inotify-based monitoring for file `/etc/netgroup': No such file or directory
Oct 15 13:10:49 instance-2 nscd[2777]: 2777 stat failed for file `/etc/netgroup'; will try again later: No such file or directory
Oct 15 13:10:49 instance-2 nscd[2777]: 2777 Access Vector Cache (AVC) started
Oct 15 13:10:49 instance-2 systemd[1]: Started Name Service Cache Daemon.

8. 
[root@instance-2 ~]# service ntpd status
Redirecting to /bin/systemctl status ntpd.service
? ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2018-10-15 13:06:42 UTC; 2s ago
  Process: 2632 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 2633 (ntpd)
   CGroup: /system.slice/ntpd.service
           L-2633 /usr/sbin/ntpd -u ntp:ntp -g

Oct 15 13:06:42 instance-2 ntpd[2633]: Listen and drop on 0 v4wildcard 0.0.0.0 UDP 123
Oct 15 13:06:42 instance-2 ntpd[2633]: Listen and drop on 1 v6wildcard :: UDP 123
Oct 15 13:06:42 instance-2 ntpd[2633]: Listen normally on 2 lo 127.0.0.1 UDP 123
Oct 15 13:06:42 instance-2 ntpd[2633]: Listen normally on 3 eth0 10.166.0.3 UDP 123
Oct 15 13:06:42 instance-2 ntpd[2633]: Listen normally on 4 lo ::1 UDP 123
Oct 15 13:06:42 instance-2 ntpd[2633]: Listen normally on 5 eth0 fe80::4001:aff:fea6:3 UDP 123
Oct 15 13:06:42 instance-2 ntpd[2633]: Listening on routing socket on fd #22 for interface updates
Oct 15 13:06:42 instance-2 ntpd[2633]: 0.0.0.0 c016 06 restart
Oct 15 13:06:42 instance-2 ntpd[2633]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Oct 15 13:06:42 instance-2 ntpd[2633]: 0.0.0.0 c011 01 freq_not_set
