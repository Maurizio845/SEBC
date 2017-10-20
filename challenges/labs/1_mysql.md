```
#### Mysql Status/Hostname
[root@ip-172-31-46-9 ~]# systemctl status mysqld.service
● mysqld.service - MySQL Community Server
   Loaded: loaded (/usr/lib/systemd/system/mysqld.service; enabled; vendor preset: disabled)
   Active: active (running) since Fri 2017-10-20 07:52:03 UTC; 4min 25s ago
 Main PID: 30809 (mysqld_safe)
   CGroup: /system.slice/mysqld.service
           ├─30809 /bin/sh /usr/bin/mysqld_safe --basedir=/usr
           └─31201 /usr/sbin/mysqld --basedir=/usr --datadir=/var/lib/mysql --plugin-dir=/usr/lib64/mysql/plugin --log-error=/var/log/mysqld.log --pid-file=/var/run/mysqld/mysqld.pid

Oct 20 07:51:52 ip-172-31-46-9.eu-central-1.compute.internal systemd[1]: Starting MySQL Community Server...
Oct 20 07:51:53 ip-172-31-46-9.eu-central-1.compute.internal mysql-systemd-start[30756]: 171020  7:51:53 [Note] Ignoring --secure-file-priv value as server is running with --bootstrap.
Oct 20 07:51:53 ip-172-31-46-9.eu-central-1.compute.internal mysql-systemd-start[30756]: 171020  7:51:53 [Note] /usr/sbin/mysqld (mysqld 5.5.58-log) starting as process 30796 ...
Oct 20 07:51:53 ip-172-31-46-9.eu-central-1.compute.internal mysql-systemd-start[30756]: 171020  7:51:53 [Note] Ignoring --secure-file-priv value as server is running with --bootstrap.
Oct 20 07:51:53 ip-172-31-46-9.eu-central-1.compute.internal mysql-systemd-start[30756]: 171020  7:51:53 [Note] /usr/sbin/mysqld (mysqld 5.5.58-log) starting as process 30803 ...
Oct 20 07:51:53 ip-172-31-46-9.eu-central-1.compute.internal mysql-systemd-start[30756]: PLEASE REMEMBER TO SET A PASSWORD FOR THE MySQL root USER !
Oct 20 07:51:53 ip-172-31-46-9.eu-central-1.compute.internal mysqld_safe[30809]: 171020 07:51:53 mysqld_safe Logging to '/var/log/mysqld.log'.
Oct 20 07:51:53 ip-172-31-46-9.eu-central-1.compute.internal mysqld_safe[30809]: 171020 07:51:53 mysqld_safe Starting mysqld daemon with databases from /var/lib/mysql
Oct 20 07:52:03 ip-172-31-46-9.eu-central-1.compute.internal systemd[1]: Started MySQL Community Server.

#### MySql version
[root@ip-172-31-46-9 ~]# mysql --version
mysql  Ver 14.14 Distrib 5.5.58, for Linux (x86_64) using readline 5.1

#### Databases
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)



```