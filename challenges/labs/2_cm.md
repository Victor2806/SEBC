HTTP request sent, awaiting response... 200 OK
Length: 273
Saving to: “cloudera-manager.repo”

100%[==============================================================================================================================>] 273         --.-K/s   in 0s

2017-05-05 00:21:01 (30.8 MB/s) - “cloudera-manager.repo” saved [273/273]

[root@ip-172-31-12-156 ~]# cp cloudera-manager.repo /etc/yum.repos.d/
cp: overwrite `/etc/yum.repos.d/cloudera-manager.repo'? n
[root@ip-172-31-12-156 ~]# cd /etc/yum.repos.d/
[root@ip-172-31-12-156 yum.repos.d]# ls -lt r| tail
echo " file load in progress 
ls: cannot access r: No such file or directory
[root@ip-172-31-12-156 yum.repos.d]# ls -ltr
total 36
-rw-r--r--. 1 root root 7989 Mar 28 10:25 CentOS-Vault.repo
-rw-r--r--. 1 root root  630 Mar 28 10:25 CentOS-Media.repo
-rw-r--r--. 1 root root  289 Mar 28 10:25 CentOS-fasttrack.repo
-rw-r--r--. 1 root root  647 Mar 28 10:25 CentOS-Debuginfo.repo
-rw-r--r--. 1 root root 1991 Mar 28 10:25 CentOS-Base.repo
-rw-r--r--. 1 root root  290 May  2 07:52 cloudera-manager.repo.~1~
-rw-r--r--. 1 root root  213 May  3 06:45 cloudera-manager.repo
-rw-r--r--  1 root root 1625 May  4 23:48 mysql-community.repo.rpmsave
[root@ip-172-31-12-156 yum.repos.d]# cp cloudera-manager.repo /etc/yum.repos.d/
cp: `cloudera-manager.repo' and `/etc/yum.repos.d/cloudera-manager.repo' are the same file
[root@ip-172-31-12-156 yum.repos.d]# y
-bash: y: command not found
[root@ip-172-31-12-156 yum.repos.d]# ls -ltr
total 36
-rw-r--r--. 1 root root 7989 Mar 28 10:25 CentOS-Vault.repo
-rw-r--r--. 1 root root  630 Mar 28 10:25 CentOS-Media.repo
-rw-r--r--. 1 root root  289 Mar 28 10:25 CentOS-fasttrack.repo
-rw-r--r--. 1 root root  647 Mar 28 10:25 CentOS-Debuginfo.repo
-rw-r--r--. 1 root root 1991 Mar 28 10:25 CentOS-Base.repo
-rw-r--r--. 1 root root  290 May  2 07:52 cloudera-manager.repo.~1~
-rw-r--r--. 1 root root  213 May  3 06:45 cloudera-manager.repo
-rw-r--r--  1 root root 1625 May  4 23:48 mysql-community.repo.rpmsave
[root@ip-172-31-12-156 yum.repos.d]# vi /etc/yum.repos.d/cloudera-manager.repo
[root@ip-172-31-12-156 yum.repos.d]# mysql
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 36
Server version: 5.1.73 Source distribution

Copyright (c) 2000, 2013, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> grant all on *.* to 'temp'@'%' identified by 'temp' with grant option;
Query OK, 0 rows affected (0.00 sec)

mysql>


[root@ip-172-31-12-156 yum.repos.d]# ls /etc/yum.repos.d
CentOS-Base.repo       CentOS-fasttrack.repo  CentOS-Vault.repo      cloudera-manager.repo.~1~
CentOS-Debuginfo.repo  CentOS-Media.repo      cloudera-manager.repo  mysql-community.repo.rpmsave
[root@ip-172-31-12-156 yum.repos.d]#


-----------



[root@ip-172-31-12-156 yum.repos.d]# hostname -f
ip-172-31-12-156.us-west-2.compute.internal
[root@ip-172-31-12-156 yum.repos.d]# sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql  --scm-host ip-172-31-12-156.us-west-2.compute.internal scm scm scm
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
[root@ip-172-31-12-156 yum.repos.d]#




[root@ip-172-31-12-156 cloudera-scm-server]# tail -f cloudera-scm-server.log
        at org.apache.avro.ipc.Transceiver.transceive(Transceiver.java:72)
        at org.apache.avro.ipc.Requestor.request(Requestor.java:147)
        at org.apache.avro.ipc.Requestor.request(Requestor.java:101)
        at org.apache.avro.ipc.specific.SpecificRequestor.invoke(SpecificRequestor.java:72)
        ... 40 more
2017-05-05 00:40:04,265 INFO WebServerImpl:org.springframework.web.servlet.handler.SimpleUrlHandlerMapping: Root mapping to handler of type [class org.springframework.web.servlet.mvc.ParameterizableViewController]
2017-05-05 00:40:04,369 INFO WebServerImpl:org.springframework.web.servlet.DispatcherServlet: FrameworkServlet 'Spring MVC Dispatcher Servlet': initialization completed in 21847 ms
2017-05-05 00:40:04,390 INFO WebServerImpl:com.cloudera.server.web.cmon.JobDetailGatekeeper: ActivityMonitor configured to allow job details for all jobs.
2017-05-05 00:40:05,437 INFO SearchRepositoryManager-0:com.cloudera.server.web.cmf.search.components.SearchRepositoryManager: Initializing SearchTemplateManager:2017-05-05T00:40:05.437Z
2017-05-05 00:40:05,476 INFO SearchRepositoryManager-0:com.cloudera.server.web.cmf.search.components.SearchRepositoryManager: Generating entities:2017-05-05T00:40:05.476Z
2017-05-05 00:40:06,449 INFO WebServerImpl:com.cloudera.server.web.cmf.AggregatorController: AggregateSummaryScheduler started.
2017-05-05 00:40:07,331 INFO WebServerImpl:org.mortbay.log: jetty-6.1.26.cloudera.4
2017-05-05 00:40:07,333 INFO WebServerImpl:org.mortbay.log: Started SelectChannelConnector@0.0.0.0:7180
2017-05-05 00:40:07,333 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
