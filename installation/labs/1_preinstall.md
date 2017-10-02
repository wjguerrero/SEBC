-----------swappiness----------------------------------------
[root@ip-172-31-5-64 centos]# sysctl -w vm.swappiness=1
vm.swappiness = 1

[root@ip-172-31-13-29 cloudera]# sysctl -w vm.swappiness=1
vm.swappiness = 1

[root@ip-172-31-0-4 centos]# sysctl -w vm.swappiness=1
vm.swappiness = 1

[root@ip-172-31-6-242 centos]# sysctl -w vm.swappiness=1
vm.swappiness = 1

-----------volumes----------------------------------------
[root@ip-172-31-6-242 centos]# fdisk -l

Disk /dev/xvda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x000b2270

    Device Boot      Start         End      Blocks   Id  System
/dev/xvda1   *        2048    83875364    41936658+  83  Linux

Disk /dev/xvdb: 128.8 GB, 128849018880 bytes, 251658240 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/xvdc: 128.8 GB, 128849018880 bytes, 251658240 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@ip-172-31-13-29 cloudera]# fdisk -l

Disk /dev/xvda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x000b2270

    Device Boot      Start         End      Blocks   Id  System
/dev/xvda1   *        2048    83875364    41936658+  83  Linux

Disk /dev/xvdb: 128.8 GB, 128849018880 bytes, 251658240 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/xvdc: 128.8 GB, 128849018880 bytes, 251658240 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@ip-172-31-0-4 centos]# fdisk -l

Disk /dev/xvda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x000b2270

    Device Boot      Start         End      Blocks   Id  System
/dev/xvda1   *        2048    83875364    41936658+  83  Linux

Disk /dev/xvdb: 128.8 GB, 128849018880 bytes, 251658240 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/xvdc: 128.8 GB, 128849018880 bytes, 251658240 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@ip-172-31-5-64 centos]# fdisk -l

Disk /dev/xvda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x000b2270

    Device Boot      Start         End      Blocks   Id  System
/dev/xvda1   *        2048    83875364    41936658+  83  Linux

Disk /dev/xvdb: 128.8 GB, 128849018880 bytes, 251658240 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/xvdc: 128.8 GB, 128849018880 bytes, 251658240 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

-----------netwok----------------------------------------
[root@ip-172-31-6-242 centos]# ifconfig -a
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.6.242  netmask 255.255.240.0  broadcast 172.31.15.255
        inet6 fe80::f5:a3ff:fee0:1512  prefixlen 64  scopeid 0x20<link>
        ether 02:f5:a3:e0:15:12  txqueuelen 1000  (Ethernet)
        RX packets 2349  bytes 167506 (163.5 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2213  bytes 224124 (218.8 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[root@ip-172-31-13-29 cloudera]# ifconfig -a
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.13.29  netmask 255.255.240.0  broadcast 172.31.15.255
        inet6 fe80::a3:f8ff:fe51:3824  prefixlen 64  scopeid 0x20<link>
        ether 02:a3:f8:51:38:24  txqueuelen 1000  (Ethernet)
        RX packets 4364  bytes 389985 (380.8 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 3808  bytes 545992 (533.1 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[root@ip-172-31-0-4 centos]# ifconfig -a
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.0.4  netmask 255.255.240.0  broadcast 172.31.15.255
        inet6 fe80::d8:dfff:feab:1a76  prefixlen 64  scopeid 0x20<link>
        ether 02:d8:df:ab:1a:76  txqueuelen 1000  (Ethernet)
        RX packets 2966  bytes 229448 (224.0 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2865  bytes 360298 (351.8 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[root@ip-172-31-5-64 centos]# ifconfig -a
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.5.64  netmask 255.255.240.0  broadcast 172.31.15.255
        inet6 fe80::b6:eeff:fed7:fc86  prefixlen 64  scopeid 0x20<link>
        ether 02:b6:ee:d7:fc:86  txqueuelen 1000  (Ethernet)
        RX packets 2574  bytes 194023 (189.4 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2426  bytes 301701 (294.6 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

-----------netwok----------------------------------------

[root@ip-172-31-6-242 etc]# nslookup ec2-13-58-229-204.us-east-2.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-13-58-229-204.us-east-2.compute.amazonaws.com
Address: 172.31.13.29

[root@ip-172-31-6-242 etc]# nslookup ec2-13-59-169-94.us-east-2.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-13-59-169-94.us-east-2.compute.amazonaws.com
Address: 172.31.6.242

[root@ip-172-31-6-242 etc]# nslookup ec2-18-221-191-254.us-east-2.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-18-221-191-254.us-east-2.compute.amazonaws.com
Address: 172.31.5.64

[root@ip-172-31-6-242 etc]# nslookup ec2-18-220-117-96.us-east-2.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-18-220-117-96.us-east-2.compute.amazonaws.com
Address: 172.31.0.4

-----------service nscd----------------------------------------
Redirecting to /bin/systemctl status  nscd.service
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-10-02 17:31:09 UTC; 6s ago
  Process: 17254 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 17255 (nscd)
   CGroup: /system.slice/nscd.service
           └─17255 /usr/sbin/nscd

Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 monitoring file `/etc/hos...)
Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 monitoring directory `/et...)
Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 monitoring file `/etc/res...)
Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 monitoring directory `/et...)
Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 monitoring file `/etc/ser...)
Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 monitoring directory `/et...)
Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 disabled inotify-based mo...y
Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 stat failed for file `/et...y
Oct 02 17:31:09 ip-172-31-13-29 nscd[17255]: 17255 Access Vector Cache (AVC)...d
Oct 02 17:31:09 ip-172-31-13-29 systemd[1]: Started Name Service Cache Daemon.
Hint: Some lines were ellipsized, use -l to show in full.

-----------service nscd----------------------------------------

[root@ip-172-31-13-29 cloudera]# service ntpd status
Redirecting to /bin/systemctl status  ntpd.service
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-10-02 17:32:46 UTC; 4s ago
  Process: 17310 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 17311 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─17311 /usr/sbin/ntpd -u ntp:ntp -g

Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: Listen and drop on 0 v4wildcard...3
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: Listen and drop on 1 v6wildcard...3
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: Listen normally on 2 lo 127.0.0...3
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: Listen normally on 3 eth0 172.3...3
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: Listen normally on 4 lo ::1 UDP 123
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: Listen normally on 5 eth0 fe80:...3
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: Listening on routing socket on ...s
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: 0.0.0.0 c016 06 restart
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: 0.0.0.0 c012 02 freq_set kernel...M
Oct 02 17:32:46 ip-172-31-13-29 ntpd[17311]: 0.0.0.0 c011 01 freq_not_set
Hint: Some lines were ellipsized, use -l to show in full.

