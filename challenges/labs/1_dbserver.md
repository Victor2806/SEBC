
[root@ip-172-31-12-156 ~]# service mysqld start
Starting mysqld:                                           [  OK  ]
[root@ip-172-31-12-156 ~]#



[root@ip-172-31-12-156 ~]# mysql
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 2
Server version: 5.1.73 Source distribution

Copyright (c) 2000, 2013, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> create database scm DEFAULT CHARACTER SET utf8;
ERROR 1007 (HY000): Can't create database 'scm'; database exists
mysql> grant all on metastore.* TO 'scm'@'%' IDENTIFIED BY 'scm';
Query OK, 0 rows affected (0.00 sec)

mysql>
mysql> create database hive DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

mysql> grant all on metastore.* TO 'hive'@'%' IDENTIFIED BY 'hive';
Query OK, 0 rows affected (0.00 sec)

mysql>
mysql> create database hue DEFAULT CHARACTER SET utf8;
ERROR 1007 (HY000): Can't create database 'hue'; database exists
mysql> grant all on hue.* TO 'hue'@'%' IDENTIFIED BY 'hue';
Query OK, 0 rows affected (0.00 sec)

mysql>
mysql>
mysql> create database rman DEFAULT CHARACTER SET utf8;
ERROR 1007 (HY000): Can't create database 'rman'; database exists
mysql> grant all on rman.* TO 'rman'@'%' IDENTIFIED BY 'rman';
Query OK, 0 rows affected (0.00 sec)

mysql>
mysql> create database oozie DEFAULT CHARACTER SET utf8;
ERROR 1007 (HY000): Can't create database 'oozie'; database exists
mysql> grant all on oozie.* TO 'oozie'@'%' IDENTIFIED BY 'oozie';
Query OK, 0 rows affected (0.00 sec)

mysql>
mysql>
mysql> create database amon DEFAULT CHARACTER SET utf8;
ERROR 1007 (HY000): Can't create database 'amon'; database exists
mysql> grant all on amon.* TO 'amon'@'%' IDENTIFIED BY 'amon';
Query OK, 0 rows affected (0.00 sec)

mysql>
mysql>
mysql> create database sentry DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

mysql> grant all on amon.* TO 'sentry'@'%' IDENTIFIED BY 'sentry';
Query OK, 0 rows affected (0.00 sec)

mysql>

------------------



create database scm DEFAULT CHARACTER SET utf8; 
grant all on metastore.* TO 'scm'@'%' IDENTIFIED BY 'scm'; 

create database hive DEFAULT CHARACTER SET utf8; 
grant all on metastore.* TO 'hive'@'%' IDENTIFIED BY 'hive'; 
 
create database hue DEFAULT CHARACTER SET utf8; 
grant all on hue.* TO 'hue'@'%' IDENTIFIED BY 'hue'; 
 

create database rman DEFAULT CHARACTER SET utf8; 
grant all on rman.* TO 'rman'@'%' IDENTIFIED BY 'rman'; 
 
create database oozie DEFAULT CHARACTER SET utf8; 
grant all on oozie.* TO 'oozie'@'%' IDENTIFIED BY 'oozie';


create database amon DEFAULT CHARACTER SET utf8; 
grant all on amon.* TO 'amon'@'%' IDENTIFIED BY 'amon';
 

create database sentry DEFAULT CHARACTER SET utf8; 
grant all on amon.* TO 'sentry'@'%' IDENTIFIED BY 'sentry';
 
----------------------


Hostname of DB hub 

[root@ip-172-31-12-156 ~]# hostname -f
ip-172-31-12-156.us-west-2.compute.internal
[root@ip-172-31-12-156 ~]#

ec2-52-39-69-132.us-west-2.compute.amazonaws.com  52.39.69.132


---------


mysql> version
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'version' at line 1
mysql> show version;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'version' at line 1
mysql> Select @@version
    -> ;
+-----------+
| @@version |
+-----------+
| 5.1.73    |
+-----------+
1 row in set (0.00 sec)

mysql>



