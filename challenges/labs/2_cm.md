```
[root@ip-172-31-44-3 yum.repos.d]# ls /etc/yum.repos.d
CentOS-Base.repo       CentOS-fasttrack.repo  CentOS-Vault.repo
CentOS-CR.repo         CentOS-Media.repo      cloudera-manager.repo
CentOS-Debuginfo.repo  CentOS-Sources.repo    MariaDB.repo

[root@ip-172-31-44-3 yum.repos.d]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-45-105.us-east-2.compute.internal scm scm scm_password              JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
[root@ip-172-31-44-3 yum.repos.d]#

```
