[root@ip-172-31-12-156 ~]# wget http://dev.mysql.com/get/mysql57-community-release-el6-9.noarch.rpm
--2017-05-04 23:43:08--  http://dev.mysql.com/get/mysql57-community-release-el6-9.noarch.rpm
Resolving dev.mysql.com... 137.254.60.11
Connecting to dev.mysql.com|137.254.60.11|:80... connected.
HTTP request sent, awaiting response... 301 Moved Permanently
Location: https://dev.mysql.com/get/mysql57-community-release-el6-9.noarch.rpm [following]
--2017-05-04 23:43:08--  https://dev.mysql.com/get/mysql57-community-release-el6-9.noarch.rpm
Connecting to dev.mysql.com|137.254.60.11|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://repo.mysql.com//mysql57-community-release-el6-9.noarch.rpm [following]
--2017-05-04 23:43:09--  https://repo.mysql.com//mysql57-community-release-el6-9.noarch.rpm
Resolving repo.mysql.com... 23.44.160.128
Connecting to repo.mysql.com|23.44.160.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9216 (9.0K) [application/x-redhat-package-manager]
Saving to: “mysql57-community-release-el6-9.noarch.rpm”

100%[==============================================================================================================================>] 9,216       --.-K/s   in 0s

2017-05-04 23:43:09 (413 MB/s) - “mysql57-community-release-el6-9.noarch.rpm” saved [9216/9216]

[root@ip-172-31-12-156 ~]# rpm -ivh mysql57-community-release-el6-9.noarch.rpm
Preparing...                ########################################### [100%]
   1:mysql57-community-relea########################################### [100%]
[root@ip-172-31-12-156 ~]# yum update
Loaded plugins: fastestmirror, presto
Setting up Update Process
Loading mirror speeds from cached hostfile
 * base: mirrors.sonic.net
 * extras: mirrors.unifiedlayer.com
 * updates: mirror.keystealth.org
mysql-connectors-community                                                                                                                       | 2.5 kB     00:00
mysql-connectors-community/primary_db                                                                                                            |  15 kB     00:00
mysql-tools-community                                                                                                                            | 2.5 kB     00:00
mysql-tools-community/primary_db                                                                                                                 |  35 kB     00:00
mysql57-community                                                                                                                                | 2.5 kB     00:00
mysql57-community/primary_db                                                                                                                     | 112 kB     00:00
Resolving Dependencies
--> Running transaction check
---> Package mysql.x86_64 0:5.1.73-8.el6_8 will be obsoleted
---> Package mysql-community-client.x86_64 0:5.7.18-1.el6 will be obsoleting
---> Package mysql-community-libs.x86_64 0:5.7.18-1.el6 will be obsoleting
--> Processing Dependency: mysql-community-common(x86-64) >= 5.7.9 for package: mysql-community-libs-5.7.18-1.el6.x86_64
---> Package mysql-community-libs-compat.x86_64 0:5.7.18-1.el6 will be obsoleting
---> Package mysql-community-server.x86_64 0:5.7.18-1.el6 will be obsoleting
---> Package mysql-libs.x86_64 0:5.1.73-8.el6_8 will be obsoleted
---> Package mysql-server.x86_64 0:5.1.73-8.el6_8 will be obsoleted
---> Package mysql57-community-release.noarch 0:el6-9 will be updated
---> Package mysql57-community-release.noarch 0:el6-10 will be an update
--> Running transaction check
---> Package mysql-community-common.x86_64 0:5.7.18-1.el6 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

========================================================================================================================================================================
 Package                                            Arch                          Version                                Repository                                Size
========================================================================================================================================================================
Installing:
 mysql-community-client                             x86_64                        5.7.18-1.el6                           mysql57-community                         23 M
     replacing  mysql.x86_64 5.1.73-8.el6_8
 mysql-community-libs                               x86_64                        5.7.18-1.el6                           mysql57-community                        2.1 M
     replacing  mysql-libs.x86_64 5.1.73-8.el6_8
 mysql-community-libs-compat                        x86_64                        5.7.18-1.el6                           mysql57-community                        1.6 M
     replacing  mysql-libs.x86_64 5.1.73-8.el6_8
 mysql-community-server                             x86_64                        5.7.18-1.el6                           mysql57-community                        152 M
     replacing  mysql-server.x86_64 5.1.73-8.el6_8
Updating:
 mysql57-community-release                          noarch                        el6-10                                 mysql57-community                         25 k
Installing for dependencies:
 mysql-community-common                             x86_64                        5.7.18-1.el6                           mysql57-community                        328 k

Transaction Summary
========================================================================================================================================================================
Install       5 Package(s)
Upgrade       1 Package(s)

Total download size: 178 M
Is this ok [y/N]: y
Downloading Packages:
Setting up and reading Presto delta metadata
Processing delta metadata
Package(s) data still to download: 178 M
(1/6): mysql-community-client-5.7.18-1.el6.x86_64.rpm                                                                                            |  23 MB     00:00
(2/6): mysql-community-common-5.7.18-1.el6.x86_64.rpm                                                                                            | 328 kB     00:00
(3/6): mysql-community-libs-5.7.18-1.el6.x86_64.rpm                                                                                              | 2.1 MB     00:00
(4/6): mysql-community-libs-compat-5.7.18-1.el6.x86_64.rpm                                                                                       | 1.6 MB     00:00
(5/6): mysql-community-server-5.7.18-1.el6.x86_64.rpm                                                                                            | 152 MB     00:01
(6/6): mysql57-community-release-el6-10.noarch.rpm                                                                                               |  25 kB     00:00
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                                    74 MB/s | 178 MB     00:02
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
Warning: RPMDB altered outside of yum.
  Installing : mysql-community-common-5.7.18-1.el6.x86_64                                                                                                          1/10
  Installing : mysql-community-libs-5.7.18-1.el6.x86_64                                                                                                            2/10
  Installing : mysql-community-client-5.7.18-1.el6.x86_64                                                                                                          3/10
  Installing : mysql-community-server-5.7.18-1.el6.x86_64                                                                                                          4/10
  Installing : mysql-community-libs-compat-5.7.18-1.el6.x86_64                                                                                                     5/10
  Updating   : mysql57-community-release-el6-10.noarch                                                                                                             6/10
  Cleanup    : mysql57-community-release-el6-9.noarch                                                                                                              7/10
  Erasing    : mysql-server-5.1.73-8.el6_8.x86_64                                                                                                                  8/10
warning: /var/log/mysqld.log saved as /var/log/mysqld.log.rpmsave
  Erasing    : mysql-5.1.73-8.el6_8.x86_64                                                                                                                         9/10
  Erasing    : mysql-libs-5.1.73-8.el6_8.x86_64                                                                                                                   10/10
  Verifying  : mysql-community-libs-compat-5.7.18-1.el6.x86_64                                                                                                     1/10
  Verifying  : mysql57-community-release-el6-10.noarch                                                                                                             2/10
  Verifying  : mysql-community-server-5.7.18-1.el6.x86_64                                                                                                          3/10
  Verifying  : mysql-community-libs-5.7.18-1.el6.x86_64                                                                                                            4/10
  Verifying  : mysql-community-common-5.7.18-1.el6.x86_64                                                                                                          5/10
  Verifying  : mysql-community-client-5.7.18-1.el6.x86_64                                                                                                          6/10
  Verifying  : mysql57-community-release-el6-9.noarch                                                                                                              7/10
  Verifying  : mysql-server-5.1.73-8.el6_8.x86_64                                                                                                                  8/10
  Verifying  : mysql-libs-5.1.73-8.el6_8.x86_64                                                                                                                    9/10
  Verifying  : mysql-5.1.73-8.el6_8.x86_64                                                                                                                        10/10

Installed:
  mysql-community-client.x86_64 0:5.7.18-1.el6          mysql-community-libs.x86_64 0:5.7.18-1.el6          mysql-community-libs-compat.x86_64 0:5.7.18-1.el6
  mysql-community-server.x86_64 0:5.7.18-1.el6

Dependency Installed:
  mysql-community-common.x86_64 0:5.7.18-1.el6

Updated:
  mysql57-community-release.noarch 0:el6-10

Replaced:
  mysql.x86_64 0:5.1.73-8.el6_8                      mysql-libs.x86_64 0:5.1.73-8.el6_8                      mysql-server.x86_64 0:5.1.73-8.el6_8

Complete!
[root@ip-172-31-12-156 ~]#


[root@ip-172-31-12-156 ~]# yum repolist all | grep mysql
mysql-cluster-7.5-community        MySQL Cluster 7.5 Community    disabled
mysql-cluster-7.5-community-source MySQL Cluster 7.5 Community -  disabled
mysql-connectors-community         MySQL Connectors Community     enabled:    36
mysql-connectors-community-source  MySQL Connectors Community - S disabled
mysql-tools-community              MySQL Tools Community          enabled:    47
mysql-tools-community-source       MySQL Tools Community - Source disabled
mysql-tools-preview                MySQL Tools Preview            disabled
mysql-tools-preview-source         MySQL Tools Preview - Source   disabled
mysql55-community                  MySQL 5.5 Community Server     disabled
mysql55-community-source           MySQL 5.5 Community Server - S disabled
mysql56-community                  MySQL 5.6 Community Server     disabled
mysql56-community-source           MySQL 5.6 Community Server - S disabled
mysql57-community                  MySQL 5.7 Community Server     enabled:   183
mysql57-community-source           MySQL 5.7 Community Server - S disabled
mysql80-community                  MySQL 8.0 Community Server     disabled
mysql80-community-source           MySQL 8.0 Community Server - S disabled
[root@ip-172-31-12-156 ~]# sudo vi /etc/yum.repos.d/mysql-community.repo
[root@ip-172-31-12-156 ~]#





[root@ip-172-31-12-156 ~]# yum install mysql-server
Loaded plugins: fastestmirror, presto
Setting up Install Process
Loading mirror speeds from cached hostfile
 * base: mirrors.sonic.net
 * extras: repos.lax.quadranet.com
 * updates: mirror.keystealth.org
mysql-connectors-community                                                                                                                       | 2.5 kB     00:00
mysql-tools-community                                                                                                                            | 2.5 kB     00:00
mysql56-community                                                                                                                                | 2.5 kB     00:00
mysql56-community/primary_db                                                                                                                     | 183 kB     00:00
Package mysql-server-5.1.73-8.el6_8.x86_64 is obsoleted by mysql-community-server-5.7.18-1.el6.x86_64 which is already installed
Nothing to do
[root@ip-172-31-12-156 ~]# yum remove "*mysql*"
Loaded plugins: fastestmirror, presto
Setting up Remove Process
Resolving Dependencies
--> Running transaction check
---> Package mysql-community-client.x86_64 0:5.7.18-1.el6 will be erased
---> Package mysql-community-common.x86_64 0:5.7.18-1.el6 will be erased
---> Package mysql-community-libs.x86_64 0:5.7.18-1.el6 will be erased
--> Processing Dependency: mysql-libs for package: 2:postfix-2.6.6-8.el6.x86_64
---> Package mysql-community-libs-compat.x86_64 0:5.7.18-1.el6 will be erased
--> Processing Dependency: libmysqlclient.so.16()(64bit) for package: perl-DBD-MySQL-4.013-3.el6.x86_64
--> Processing Dependency: libmysqlclient.so.16(libmysqlclient_16)(64bit) for package: perl-DBD-MySQL-4.013-3.el6.x86_64
--> Processing Dependency: libmysqlclient_r.so.16()(64bit) for package: MySQL-python-1.2.3-0.3.c1.1.el6.x86_64
--> Processing Dependency: libmysqlclient_r.so.16(libmysqlclient_16)(64bit) for package: MySQL-python-1.2.3-0.3.c1.1.el6.x86_64
---> Package mysql-community-server.x86_64 0:5.7.18-1.el6 will be erased
---> Package mysql57-community-release.noarch 0:el6-10 will be erased
--> Running transaction check
---> Package MySQL-python.x86_64 0:1.2.3-0.3.c1.1.el6 will be erased
--> Processing Dependency: MySQL-python for package: cloudera-manager-agent-5.11.0-1.cm5110.p0.101.el6.x86_64
---> Package perl-DBD-MySQL.x86_64 0:4.013-3.el6 will be erased
---> Package postfix.x86_64 2:2.6.6-8.el6 will be erased
--> Processing Dependency: /usr/sbin/sendmail for package: redhat-lsb-core-4.0-7.el6.centos.x86_64
--> Processing Dependency: /usr/sbin/sendmail for package: cronie-1.4.4-16.el6_8.2.x86_64
--> Running transaction check
---> Package cloudera-manager-agent.x86_64 0:5.11.0-1.cm5110.p0.101.el6 will be erased
---> Package cronie.x86_64 0:1.4.4-16.el6_8.2 will be erased
--> Processing Dependency: cronie = 1.4.4-16.el6_8.2 for package: cronie-anacron-1.4.4-16.el6_8.2.x86_64
---> Package redhat-lsb-core.x86_64 0:4.0-7.el6.centos will be erased
--> Running transaction check
---> Package cronie-anacron.x86_64 0:1.4.4-16.el6_8.2 will be erased
--> Processing Dependency: /etc/cron.d for package: crontabs-1.10-33.el6.noarch
--> Restarting Dependency Resolution with new changes.
--> Running transaction check
---> Package crontabs.noarch 0:1.10-33.el6 will be erased
--> Finished Dependency Resolution

Dependencies Resolved

========================================================================================================================================================================
 Package                                         Arch                       Version                                        Repository                              Size
========================================================================================================================================================================
Removing:
 mysql-community-client                          x86_64                     5.7.18-1.el6                                   @mysql57-community                     100 M
 mysql-community-common                          x86_64                     5.7.18-1.el6                                   @mysql57-community                     2.5 M
 mysql-community-libs                            x86_64                     5.7.18-1.el6                                   @mysql57-community                     8.9 M
 mysql-community-libs-compat                     x86_64                     5.7.18-1.el6                                   @mysql57-community                     5.4 M
 mysql-community-server                          x86_64                     5.7.18-1.el6                                   @mysql57-community                     769 M
 mysql57-community-release                       noarch                     el6-10                                         @mysql57-community                      30 k
Removing for dependencies:
 MySQL-python                                    x86_64                     1.2.3-0.3.c1.1.el6                             @base                                  246 k
 cloudera-manager-agent                          x86_64                     5.11.0-1.cm5110.p0.101.el6                     @cloudera-manager                       71 M
 cronie                                          x86_64                     1.4.4-16.el6_8.2                               @base                                  174 k
 cronie-anacron                                  x86_64                     1.4.4-16.el6_8.2                               @base                                   43 k
 crontabs                                        noarch                     1.10-33.el6                                    @base                                  2.4 k
 perl-DBD-MySQL                                  x86_64                     4.013-3.el6                                    @base                                  338 k
 postfix                                         x86_64                     2:2.6.6-8.el6                                  @base                                  9.7 M
 redhat-lsb-core                                 x86_64                     4.0-7.el6.centos                               @base                                   22 k

Transaction Summary
========================================================================================================================================================================
Remove       14 Package(s)

Installed size: 967 M
Is this ok [y/N]: y
Downloading Packages:
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Erasing    : cloudera-manager-agent-5.11.0-1.cm5110.p0.101.el6.x86_64                                                                                            1/14
warning: /etc/cloudera-scm-agent/config.ini saved as /etc/cloudera-scm-agent/config.ini.rpmsave
  Erasing    : redhat-lsb-core-4.0-7.el6.centos.x86_64                                                                                                             2/14
/var/tmp/rpm-tmp.9JkAMo: line 1: lsb_release: command not found
  Erasing    : cronie-1.4.4-16.el6_8.2.x86_64                                                                                                                      3/14
  Erasing    : cronie-anacron-1.4.4-16.el6_8.2.x86_64                                                                                                              4/14
  Erasing    : crontabs-1.10-33.el6.noarch                                                                                                                         5/14
  Erasing    : 2:postfix-2.6.6-8.el6.x86_64                                                                                                                        6/14
  Erasing    : mysql-community-server-5.7.18-1.el6.x86_64                                                                                                          7/14
  Erasing    : mysql-community-client-5.7.18-1.el6.x86_64                                                                                                          8/14
  Erasing    : MySQL-python-1.2.3-0.3.c1.1.el6.x86_64                                                                                                              9/14
  Erasing    : perl-DBD-MySQL-4.013-3.el6.x86_64                                                                                                                  10/14
  Erasing    : mysql57-community-release-el6-10.noarch                                                                                                            11/14
warning: /etc/yum.repos.d/mysql-community.repo saved as /etc/yum.repos.d/mysql-community.repo.rpmsave
  Erasing    : mysql-community-libs-compat-5.7.18-1.el6.x86_64                                                                                                    12/14
  Erasing    : mysql-community-libs-5.7.18-1.el6.x86_64                                                                                                           13/14
  Erasing    : mysql-community-common-5.7.18-1.el6.x86_64                                                                                                         14/14
  Verifying  : cronie-anacron-1.4.4-16.el6_8.2.x86_64                                                                                                              1/14
  Verifying  : cronie-1.4.4-16.el6_8.2.x86_64                                                                                                                      2/14
  Verifying  : cloudera-manager-agent-5.11.0-1.cm5110.p0.101.el6.x86_64                                                                                            3/14
  Verifying  : 2:postfix-2.6.6-8.el6.x86_64                                                                                                                        4/14
  Verifying  : redhat-lsb-core-4.0-7.el6.centos.x86_64                                                                                                             5/14
  Verifying  : mysql-community-libs-compat-5.7.18-1.el6.x86_64                                                                                                     6/14
  Verifying  : crontabs-1.10-33.el6.noarch                                                                                                                         7/14
  Verifying  : perl-DBD-MySQL-4.013-3.el6.x86_64                                                                                                                   8/14
  Verifying  : mysql-community-server-5.7.18-1.el6.x86_64                                                                                                          9/14
  Verifying  : mysql-community-libs-5.7.18-1.el6.x86_64                                                                                                           10/14
  Verifying  : mysql-community-common-5.7.18-1.el6.x86_64                                                                                                         11/14
  Verifying  : MySQL-python-1.2.3-0.3.c1.1.el6.x86_64                                                                                                             12/14
  Verifying  : mysql57-community-release-el6-10.noarch                                                                                                            13/14
  Verifying  : mysql-community-client-5.7.18-1.el6.x86_64                                                                                                         14/14

Removed:
  mysql-community-client.x86_64 0:5.7.18-1.el6               mysql-community-common.x86_64 0:5.7.18-1.el6          mysql-community-libs.x86_64 0:5.7.18-1.el6
  mysql-community-libs-compat.x86_64 0:5.7.18-1.el6          mysql-community-server.x86_64 0:5.7.18-1.el6          mysql57-community-release.noarch 0:el6-10

Dependency Removed:
  MySQL-python.x86_64 0:1.2.3-0.3.c1.1.el6           cloudera-manager-agent.x86_64 0:5.11.0-1.cm5110.p0.101.el6           cronie.x86_64 0:1.4.4-16.el6_8.2
  cronie-anacron.x86_64 0:1.4.4-16.el6_8.2           crontabs.noarch 0:1.10-33.el6                                        perl-DBD-MySQL.x86_64 0:4.013-3.el6
  postfix.x86_64 2:2.6.6-8.el6                       redhat-lsb-core.x86_64 0:4.0-7.el6.centos

Complete!
[root@ip-172-31-12-156 ~]# yum install mysql-server
Loaded plugins: fastestmirror, presto
Setting up Install Process
Loading mirror speeds from cached hostfile
 * base: mirrors.sonic.net
 * extras: repos.lax.quadranet.com
 * updates: mirror.keystealth.org
Resolving Dependencies
--> Running transaction check
---> Package mysql-server.x86_64 0:5.1.73-8.el6_8 will be installed
--> Processing Dependency: mysql = 5.1.73-8.el6_8 for package: mysql-server-5.1.73-8.el6_8.x86_64
--> Processing Dependency: perl-DBD-MySQL for package: mysql-server-5.1.73-8.el6_8.x86_64
--> Processing Dependency: libmysqlclient_r.so.16(libmysqlclient_16)(64bit) for package: mysql-server-5.1.73-8.el6_8.x86_64
--> Processing Dependency: libmysqlclient.so.16(libmysqlclient_16)(64bit) for package: mysql-server-5.1.73-8.el6_8.x86_64
--> Processing Dependency: libmysqlclient_r.so.16()(64bit) for package: mysql-server-5.1.73-8.el6_8.x86_64
--> Processing Dependency: libmysqlclient.so.16()(64bit) for package: mysql-server-5.1.73-8.el6_8.x86_64
--> Running transaction check
---> Package mysql.x86_64 0:5.1.73-8.el6_8 will be installed
---> Package mysql-libs.x86_64 0:5.1.73-8.el6_8 will be installed
---> Package perl-DBD-MySQL.x86_64 0:4.013-3.el6 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

========================================================================================================================================================================
 Package                                     Arch                                Version                                        Repository                         Size
========================================================================================================================================================================
Installing:
 mysql-server                                x86_64                              5.1.73-8.el6_8                                 base                              8.6 M
Installing for dependencies:
 mysql                                       x86_64                              5.1.73-8.el6_8                                 base                              895 k
 mysql-libs                                  x86_64                              5.1.73-8.el6_8                                 base                              1.2 M
 perl-DBD-MySQL                              x86_64                              4.013-3.el6                                    base                              134 k

Transaction Summary
========================================================================================================================================================================
Install       4 Package(s)

Total download size: 11 M
Installed size: 31 M
Is this ok [y/N]: y
Downloading Packages:
Setting up and reading Presto delta metadata
Processing delta metadata
Package(s) data still to download: 11 M
(1/4): mysql-5.1.73-8.el6_8.x86_64.rpm                                                                                                           | 895 kB     00:00
(2/4): mysql-libs-5.1.73-8.el6_8.x86_64.rpm                                                                                                      | 1.2 MB     00:00
(3/4): mysql-server-5.1.73-8.el6_8.x86_64.rpm                                                                                                    | 8.6 MB     00:00
(4/4): perl-DBD-MySQL-4.013-3.el6.x86_64.rpm                                                                                                     | 134 kB     00:00
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                                   6.5 MB/s |  11 MB     00:01
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : mysql-libs-5.1.73-8.el6_8.x86_64                                                                                                                     1/4
  Installing : perl-DBD-MySQL-4.013-3.el6.x86_64                                                                                                                    2/4
  Installing : mysql-5.1.73-8.el6_8.x86_64                                                                                                                          3/4
  Installing : mysql-server-5.1.73-8.el6_8.x86_64                                                                                                                   4/4
  Verifying  : perl-DBD-MySQL-4.013-3.el6.x86_64                                                                                                                    1/4
  Verifying  : mysql-server-5.1.73-8.el6_8.x86_64                                                                                                                   2/4
  Verifying  : mysql-5.1.73-8.el6_8.x86_64                                                                                                                          3/4
  Verifying  : mysql-libs-5.1.73-8.el6_8.x86_64                                                                                                                     4/4

Installed:
  mysql-server.x86_64 0:5.1.73-8.el6_8

Dependency Installed:
  mysql.x86_64 0:5.1.73-8.el6_8                       mysql-libs.x86_64 0:5.1.73-8.el6_8                       perl-DBD-MySQL.x86_64 0:4.013-3.el6

Complete!
[root@ip-172-31-12-156 ~]#

[root@ip-172-31-12-156 ~]# service mysqld start
Starting mysqld:                                           [  OK  ]
[root@ip-172-31-12-156 ~]#




# Enable to use MySQL 5.5
[mysql55-community]
name=MySQL 5.5 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.5-community/el/6/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

# Enable to use MySQL 5.6
[mysql56-community]
name=MySQL 5.6 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.6-community/el/6/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

[mysql57-community]
name=MySQL 5.7 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.7-community/el/6/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

[mysql80-community]
name=MySQL 8.0 Community Server
baseurl=http://repo.mysql.com/yum/mysql-8.0-community/el/6/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql







Database drivers in all hosts 

[root@ip-172-31-44-153 ~]# mkdir -p /usr/share/java/
[root@ip-172-31-44-153 ~]# cp mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-bin.jar /usr/share/java/mysql-connector-java.jar
[root@ip-172-31-44-153 ~]# yum list installed | grep mysql
mysql-libs.x86_64           5.1.71-1.el6               @CentOS6-Base/$releasever
[root@ip-172-31-44-153 ~]#



[root@ip-172-31-36-127 ~]# cp mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-bin.jar /usr/share/java/mysql-connector-java.jar
[root@ip-172-31-36-127 ~]#
[root@ip-172-31-36-127 ~]#  yum list installed | grep mysql
mysql-libs.x86_64           5.1.71-1.el6               @CentOS6-Base/$releasever
[root@ip-172-31-36-127 ~]#



[root@ip-172-31-39-197 ~]#
[root@ip-172-31-39-197 ~]#
[root@ip-172-31-39-197 ~]#
[root@ip-172-31-39-197 ~]# mkdir -p /usr/share/java/
[root@ip-172-31-39-197 ~]#
[root@ip-172-31-39-197 ~]#
[root@ip-172-31-39-197 ~]#
[root@ip-172-31-39-197 ~]# cp mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-bin.jar /usr/share/java/mysql-connector-java.jar
[root@ip-172-31-39-197 ~]#



[root@ip-172-31-42-229 ~]# mkdir -p /usr/share/java/
[root@ip-172-31-42-229 ~]# cp mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-bin.jar /usr/share/java/mysql-connector-java.jar
[root@ip-172-31-42-229 ~]#


[root@ip-172-31-12-156 ~]# cp mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-bin.jar /usr/share/java/mysql-connector-java.jar
cp: overwrite `/usr/share/java/mysql-connector-java.jar'? y
[root@ip-172-31-12-156 ~]#



-----------------------


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

