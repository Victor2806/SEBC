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


