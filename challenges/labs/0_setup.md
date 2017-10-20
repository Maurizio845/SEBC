```
#### Cloud Provider
AWS

#### Linux Release
[root@ip-172-31-39-254 ~]# cat /etc/centos-release
CentOS Linux release 7.4.1708 (Core)

#### Disk space
[root@ip-172-31-39-254 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       60G  880M   60G   2% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.3G     0  7.3G   0% /dev/shm
tmpfs           7.3G   17M  7.3G   1% /run
tmpfs           7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs           1.5G     0  1.5G   0% /run/user/1000


#### Repository
[root@ip-172-31-39-254 ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.23media.de
 * extras: mirror.imt-systems.com
 * updates: centos.intergenia.de
repo id                                                                                 repo name                                                                                  status
base/7/x86_64                                                                           CentOS-7 - Base                                                                            9,591
extras/7/x86_64                                                                         CentOS-7 - Extras                                                                            227
updates/7/x86_64                                                                        CentOS-7 - Updates                                                                           741
repolist: 10,559

#### Users
[root@ip-172-31-34-43 ~]# cat /etc/passwd | grep -E 'ernest|siwicki'
ernest:x:2000:2000::/home/ernest:/bin/bash
siwicki:x:3000:3000::/home/siwicki:/bin/bash


#### Group
[root@ip-172-31-34-43 ~]# cat /etc/group | grep -E 'usa|emea'
usa:x:1001:
emea:x:1002:

```



