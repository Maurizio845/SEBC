```
#### Repository

[root@ip-172-31-34-43 ~]# ls /etc/yum.repos.d
CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Media.repo    CentOS-Vault.repo      mysql-community.repo
CentOS-CR.repo    CentOS-fasttrack.repo  CentOS-Sources.repo  cloudera-manager.repo  mysql-community-source.repo

#### Database Creation
[root@ip-172-31-34-43 tmp]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-46-9.eu-central-1.compute.internal -utemp -ptemp --scm-host ip-172-31-34-43.eu-central-1.compute.internal scm scm scm
JAVA_HOME=/usr/java/jdk1.8.0_131
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.8.0_131/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!


```
