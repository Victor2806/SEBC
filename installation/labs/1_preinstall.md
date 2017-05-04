[root@ip-172-31-12-156 bin]# cat /proc/sys/vm/swappiness
60

[root@ip-172-31-12-156 bin]#sysctl vm.swappiness=1

vm.swappiness = 1

2. Show the mount attributes of your volume(s)

```

[root@ip-172-31-12-156 ~]# mount

/dev/xvde on / type ext4 (rw)

proc on /proc type proc (rw)

sysfs on /sys type sysfs (rw)

devpts on /dev/pts type devpts (rw,gid=5,mode=620)

tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")

none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)

```

3. list the reserve space setting

```

[root@ip-172-31-12-156 ~]# tune2fs -l /dev/xvde | grep Reserved

Reserved block count:     104857

Reserved GDT blocks:      511

Reserved blocks uid:      0 (user root)

Reserved blocks gid:      0 (group root)

```

4. Disable transparent hugepage support

```

[root@ip-172-31-12-156 ~]# cat /sys/kernel/mm/transparent_hugepage/enabled

cat: /sys/kernel/mm/transparent_hugepage/enabled: No such file or directory

```

5. List your network interface configuration

```

[root@ip-172-31-12-156 ~]# ip addr

1: lo: <LOOPBACK,UP,LOWER_UP> mtu 16436 qdisc noqueue state UNKNOWN

    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00

    inet 127.0.0.1/8 scope host lo

    inet6 ::1/128 scope host

       valid_lft forever preferred_lft forever

2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc pfifo_fast state UP qlen 1000

    link/ether 06:66:6b:b3:b5:3b brd ff:ff:ff:ff:ff:ff

    inet 172.31.38.19/20 brd 172.31.47.255 scope global eth0

    inet6 fe80::466:6bff:feb3:b53b/64 scope link

       valid_lft forever preferred_lft forever

```

6. Show correct forward and reverse host lookups

```

[root@ip-172-31-12-156 ~]# getent hosts ec2-34-210-17-89.us-west-2.compute.amazonaws.com

172.31.38.19    ec2-34-210-17-89.us-west-2.compute.amazonaws.com

[root@ip-172-31-12-156 ~]# getent hosts 172.31.38.19

172.31.38.19    ip-172-31-12-156.us-west-2.compute.internal

 

[root@ip-172-31-12-156 nslookup ec2-34-210-17-89.us-west-2.compute.amazonaws.com

Server:         172.31.0.2

Address:        172.31.0.2#53

 

Non-authoritative answer:

Name:   ec2-34-210-17-89.us-west-2.compute.amazonaws.com

Address: 172.31.38.19

 

[root@ip-172-31-12-156 ~]# nslookup 172.31.38.19

Server:         172.31.0.2

Address:        172.31.0.2#53

 

Non-authoritative answer:

19.38.31.172.in-addr.arpa       name = ip-172-31-12-156.us-west-2.compute.internal.

 

Authoritative answers can be found from:

```

7. Show the nscd service is running

```

[root@ip-172-31-12-156 ~]# service nscd status

nscd (pid 976) is running...

```

 

8. Show the ntpd service is running

```

[root@ip-172-31-12-156 ~]# service ntpd status

ntpd (pid  1372) is running...