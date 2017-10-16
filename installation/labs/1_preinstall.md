#1
[root@ip-172-31-29-107 ~]# sysctl vm.swappiness=60

[root@ip-172-31-29-107 ~]# cat /proc/sys/vm/swappiness
60

#2
[root@ip-172-31-29-107 ~]# mount -l
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)

#3 
[root@ip-172-31-29-107 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       50G  674M   46G   2% /
tmpfs           7.3G     0  7.3G   0% /dev/shm

#4 (Append 'transparent_hugepage=never' to the kernel command line in grub.conf)
[root@ip-172-31-29-107 redhat_transparent_hugepage]# cat /sys/kernel/mm/redhat_transparent_hugepage/enabled
[always] madvise never

[centos@ip-172-31-29-107 ~]$ cat /sys/kernel/mm/redhat_transparent_hugepage/enabled
always madvise [never]

#5
[centos@ip-172-31-29-107 ~]$ ifconfig
eth0      Link encap:Ethernet  HWaddr 02:61:42:5C:3C:F6
          inet addr:172.31.29.107  Bcast:172.31.31.255  Mask:255.255.240.0
          inet6 addr: fe80::61:42ff:fe5c:3cf6/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:310 errors:0 dropped:0 overruns:0 frame:0
          TX packets:338 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:41795 (40.8 KiB)  TX bytes:48236 (47.1 KiB)
          Interrupt:145

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

#6
[centos@ip-172-31-29-107 ~]$ getent hosts ip-172-31-29-107.eu-central-1.compute.internal
172.31.29.107   ip-172-31-29-107.eu-central-1.compute.internal

[centos@ip-172-31-29-107 ~]$ getent hosts 172.31.29.107
172.31.29.107   ip-172-31-29-107.eu-central-1.compute.internal

#7 (installation needed : yum install nscd)

[root@ip-172-31-25-67 ~]# service nscd start
Starting nscd:                                             [  OK  ]

[root@ip-172-31-29-107 ~]# service nscd status
nscd (pid 1927) is running...


#8 (installation needed : yum install ntp)
[root@ip-172-31-25-67 ~]# service ntpd start
Starting ntpd:                                             [  OK  ]


[root@ip-172-31-29-107 ~]# service ntpd status
ntpd (pid  2032) is running...


