AWS

Public DNS (IPv4)                                 | IPv4 Public IP| Private DNS                                | Private IPs  
--------------------------------------------------|---------------|--------------------------------------------|--------------
ec2-18-221-252-184.us-east-2.compute.amazonaws.com| 18.221.252.184|	ip-172-31-45-105.us-east-2.compute.internal| 172.31.45.105
ec2-18-221-203-96.us-east-2.compute.amazonaws.com | 18.221.203.96 |	ip-172-31-44-3.us-east-2.compute.internal  | 172.31.44.3  
ec2-13-59-90-78.us-east-2.compute.amazonaws.com   | 13.59.90.78   |	ip-172-31-40-210.us-east-2.compute.internal| 172.31.40.210
ec2-13-58-213-204.us-east-2.compute.amazonaws.com | 13.58.213.204 |	ip-172-31-45-148.us-east-2.compute.internal| 172.31.45.148

centos-release-7-3.1611.el7.centos.x86_64

```
[root@ip-172-31-45-105 centos]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       40G  1.1G   39G   3% /
devtmpfs         16G     0   16G   0% /dev
tmpfs            16G     0   16G   0% /dev/shm
tmpfs            16G   17M   16G   1% /run
tmpfs            16G     0   16G   0% /sys/fs/cgroup
tmpfs           3.2G     0  3.2G   0% /run/user/1000
/dev/xvdb       118G   61M  112G   1% /disco1
/dev/xvdc       118G   69M  112G   1% /disco2
```

```
[root@ip-172-31-45-105 centos]# yum repolist
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.es.its.nyu.edu
 * extras: bay.uchicago.edu
 * updates: mirrors.liquidweb.com
repo id                             repo name                             status
base/7/x86_64                       CentOS-7 - Base                       9,591
extras/7/x86_64                     CentOS-7 - Extras                       225
updates/7/x86_64                    CentOS-7 - Updates                      731
repolist: 10,547
```

´´´
[root@ip-172-31-45-105 centos]# cat /etc/passwd | grep saturn

saturn: x :2800:2902::/home/saturn:/bin/bash

[root@ip-172-31-45-105 centos]# cat /etc/passwd | grep haley

haley: x :2900:2901::/home/haley:/bin/bash

´´´

´´´
[root@ip-172-31-45-105 centos]# cat /etc/group | grep planets
planets: x :2902:

[root@ip-172-31-45-105 centos]# cat /etc/group | grep comets
comets: x :2901:
´´´

