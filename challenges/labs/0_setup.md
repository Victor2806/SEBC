Cloud Provider AWS 


ec2-52-39-69-132.us-west-2.compute.amazonaws.com  52.39.69.132
ec2-35-162-152-43.us-west-2.compute.amazonaws.com 35.162.152.43
ec2-34-210-16-120.us-west-2.compute.amazonaws.com 34.210.16.120
ec2-52-38-101-75.us-west-2.compute.amazonaws.com 52.38.101.75
ec2-54-71-80-37.us-west-2.compute.amazonaws.com 54.71.80.37

Linux  CentOs 6.5


Node1:-

[root@ip-172-31-12-156 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G   16G   12G  58% /
tmpfs           7.3G     0  7.3G   0% /dev/shm
cm_processes    7.4G     0  7.4G   0% /var/run/cloudera-scm-agent/process
[root@ip-172-31-12-156 ~]# resize2fs /dev/xvde
resize2fs 1.41.12 (17-May-2010)
The filesystem is already 7864320 blocks long.  Nothing to do!

[root@ip-172-31-12-156 ~]#


Node 2:

[root@ip-172-31-42-229 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       7.9G  650M  6.9G   9% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
[root@ip-172-31-42-229 ~]# resize2fs /dev/xvde
resize2fs 1.41.12 (17-May-2010)
Filesystem at /dev/xvde is mounted on /; on-line resizing required
old desc_blocks = 1, new_desc_blocks = 2
Performing an on-line resize of /dev/xvde to 7864320 (4k) blocks.
The filesystem on /dev/xvde is now 7864320 blocks long.

[root@ip-172-31-42-229 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
[root@ip-172-31-42-229 ~]#


Node 3:-


Authenticating with public key "imported-openssh-key"
[root@ip-172-31-39-197 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       7.9G  650M  6.9G   9% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
[root@ip-172-31-39-197 ~]# resize2fs /dev/xvde
resize2fs 1.41.12 (17-May-2010)
Filesystem at /dev/xvde is mounted on /; on-line resizing required
old desc_blocks = 1, new_desc_blocks = 2
Performing an on-line resize of /dev/xvde to 7864320 (4k) blocks.
The filesystem on /dev/xvde is now 7864320 blocks long.

[root@ip-172-31-39-197 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
[root@ip-172-31-39-197 ~]#



Node 4:-


[root@ip-172-31-36-127 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       7.9G  650M  6.9G   9% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
[root@ip-172-31-36-127 ~]# resize2fs /dev/xvde
resize2fs 1.41.12 (17-May-2010)
Filesystem at /dev/xvde is mounted on /; on-line resizing required
old desc_blocks = 1, new_desc_blocks = 2
Performing an on-line resize of /dev/xvde to 7864320 (4k) blocks.
The filesystem on /dev/xvde is now 7864320 blocks long.

[root@ip-172-31-36-127 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
[root@ip-172-31-36-127 ~]#




Node5:-

Using username "root".
Authenticating with public key "imported-openssh-key"
[root@ip-172-31-44-153 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       7.9G  651M  6.9G   9% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
[root@ip-172-31-44-153 ~]# resize2fs /dev/xvde
resize2fs 1.41.12 (17-May-2010)
Filesystem at /dev/xvde is mounted on /; on-line resizing required
old desc_blocks = 1, new_desc_blocks = 2
Performing an on-line resize of /dev/xvde to 7864320 (4k) blocks.
The filesystem on /dev/xvde is now 7864320 blocks long.

[root@ip-172-31-44-153 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm
[root@ip-172-31-44-153 ~]#






Node 1:

[root@ip-172-31-12-156 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: mirrors.sonic.net
 * extras: mirrors.unifiedlayer.com
 * updates: mirrors.sonic.net
base                                                                                                                                             | 3.7 kB     00:00
cloudera-manager                                                                                                                                 |  951 B     00:00
extras                                                                                                                                           | 3.4 kB     00:00
updates                                                                                                                                          | 3.4 kB     00:00
repo id                                                                  repo name                                                                                status
base                                                                     CentOS-6 - Base                                                                          6,706
cloudera-manager                                                         Cloudera Manager, Version 5.11.0                                                             7
extras                                                                   CentOS-6 - Extras                                                                           64
updates                                                                  CentOS-6 - Updates                                                                         252
repolist: 7,029
[root@ip-172-31-12-156 ~]#


Node 2:-

[root@ip-172-31-42-229 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto

base                                                                                                                                             | 3.7 kB     00:00
base/primary_db                                                                                                                                  | 4.7 MB     00:01
extras                                                                                                                                           | 3.4 kB     00:00
extras/primary_db                                                                                                                                |  37 kB     00:00
updates                                                                                                                                          | 3.4 kB     00:00
updates/primary_db                                                                                                                               | 803 kB     00:00
repo id                                                                    repo name                                                                              status
base                                                                       CentOS-6 - Base                                                                        6,706
extras                                                                     CentOS-6 - Extras                                                                         64
updates                                                                    CentOS-6 - Updates                                                                       252
repolist: 7,022
[root@ip-172-31-42-229 ~]#
[root@ip-172-31-42-229 ~]#


Node 3:

[root@ip-172-31-39-197 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto

base                                                                                                                                             | 3.7 kB     00:00
base/primary_db                                                                                                                                  | 4.7 MB     00:01
extras                                                                                                                                           | 3.4 kB     00:00
extras/primary_db                                                                                                                                |  37 kB     00:00
updates                                                                                                                                          | 3.4 kB     00:00
updates/primary_db                                                                                                                               | 803 kB     00:01
repo id                                                                    repo name                                                                              status
base                                                                       CentOS-6 - Base                                                                        6,706
extras                                                                     CentOS-6 - Extras                                                                         64
updates                                                                    CentOS-6 - Updates                                                                       252
repolist: 7,022
[root@ip-172-31-39-197 ~]#
[root@ip-172-31-39-197 ~]#


Node 4:

[root@ip-172-31-36-127 ~]# yum repolist enabled

Loaded plugins: fastestmirror, presto
base                                                     | 3.7 kB     00:00
base/primary_db                                          | 4.7 MB     00:01
extras                                                   | 3.4 kB     00:00
extras/primary_db                                        |  37 kB     00:00
updates                                                  | 3.4 kB     00:00
updates/primary_db                                       | 803 kB     00:00
repo id                        repo name                                  status
base                           CentOS-6 - Base                            6,706
extras                         CentOS-6 - Extras                             64
updates                        CentOS-6 - Updates                           252
repolist: 7,022
[root@ip-172-31-36-127 ~]#
[root@ip-172-31-36-127 ~]#


Node 5:


[root@ip-172-31-44-153 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto

base                                                     | 3.7 kB     00:00
base/primary_db                                          | 4.7 MB     00:01
extras                                                   | 3.4 kB     00:00
extras/primary_db                                        |  37 kB     00:00
updates                                                  | 3.4 kB     00:00
updates/primary_db                                       | 803 kB     00:00
repo id                        repo name                                  status
base                           CentOS-6 - Base                            6,706
extras                         CentOS-6 - Extras                             64
updates                        CentOS-6 - Updates                           252
repolist: 7,022
[root@ip-172-31-44-153 ~]#
[root@ip-172-31-44-153 ~]#

-----------------
groupadd aussies
groupadd kiwis


useradd -g aussies -u 2300 cate 
useradd -g kiwis -u 2900 jemaine

cate:x:2300:2901::/home/cate:/bin/bash


[root@ip-172-31-12-156 ~]# tail -2 /etc/passwd
cate:x:2300:2901::/home/cate:/bin/bash
jemaine:x:2900:2902::/home/jemaine:/bin/bash
[root@ip-172-31-12-156 ~]#


[root@ip-172-31-12-156 ~]# tail -2 /etc/group
aussies:x:2901:
kiwis:x:2902:
[root@ip-172-31-12-156 ~]#




jemaine:x:2900:2902::/home/jemaine:/bin/bash
[root@ip-172-31-12-156 ~]# cat /etc/passwd
 


