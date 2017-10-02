[root@ip-172-31-6-242 etc]# yum -y install mariadb-server
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirrors.usinternet.com
 * extras: mirror.math.princeton.edu
 * updates: centos.aol.com
Resolving Dependencies
--> Running transaction check
---> Package mariadb-server.x86_64 1:5.5.56-2.el7 will be installed
--> Processing Dependency: mariadb-libs(x86-64) = 1:5.5.56-2.el7 for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: mariadb(x86-64) = 1:5.5.56-2.el7 for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl-DBI for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl-DBD-MySQL for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(vars) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(strict) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(Sys::Hostname) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(POSIX) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(Getopt::Long) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(File::Temp) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(File::Path) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(File::Copy) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(File::Basename) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(Data::Dumper) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: perl(DBI) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: libaio.so.1(LIBAIO_0.4)(64bit) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: libaio.so.1(LIBAIO_0.1)(64bit) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: /usr/bin/perl for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Processing Dependency: libaio.so.1()(64bit) for package: 1:mariadb-server-5.5.56-2.el7.x86_64
--> Running transaction check
---> Package libaio.x86_64 0:0.3.109-13.el7 will be installed
---> Package mariadb.x86_64 1:5.5.56-2.el7 will be installed
--> Processing Dependency: perl(Exporter) for package: 1:mariadb-5.5.56-2.el7.x86_64
---> Package mariadb-libs.x86_64 1:5.5.52-1.el7 will be updated
---> Package mariadb-libs.x86_64 1:5.5.56-2.el7 will be an update
---> Package perl.x86_64 4:5.16.3-292.el7 will be installed
--> Processing Dependency: perl-libs = 4:5.16.3-292.el7 for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Socket) >= 1.3 for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Scalar::Util) >= 1.10 for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl-macros for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl-libs for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(threads::shared) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(threads) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(constant) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Time::Local) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Time::HiRes) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Storable) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Socket) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Scalar::Util) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Pod::Simple::XHTML) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Pod::Simple::Search) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Filter::Util::Call) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(File::Spec::Unix) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(File::Spec::Functions) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(File::Spec) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Cwd) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Carp) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: libperl.so()(64bit) for package: 4:perl-5.16.3-292.el7.x86_64
---> Package perl-DBD-MySQL.x86_64 0:4.023-5.el7 will be installed
---> Package perl-DBI.x86_64 0:1.627-4.el7 will be installed
--> Processing Dependency: perl(RPC::PlServer) >= 0.2001 for package: perl-DBI-1.627-4.el7.x86_64
--> Processing Dependency: perl(RPC::PlClient) >= 0.2000 for package: perl-DBI-1.627-4.el7.x86_64
---> Package perl-Data-Dumper.x86_64 0:2.145-3.el7 will be installed
---> Package perl-File-Path.noarch 0:2.09-2.el7 will be installed
---> Package perl-File-Temp.noarch 0:0.23.01-3.el7 will be installed
---> Package perl-Getopt-Long.noarch 0:2.40-2.el7 will be installed
--> Processing Dependency: perl(Pod::Usage) >= 1.14 for package: perl-Getopt-Long-2.40-2.el7.noarch
--> Processing Dependency: perl(Text::ParseWords) for package: perl-Getopt-Long-2.40-2.el7.noarch
--> Running transaction check
---> Package perl-Carp.noarch 0:1.26-244.el7 will be installed
---> Package perl-Exporter.noarch 0:5.68-3.el7 will be installed
---> Package perl-Filter.x86_64 0:1.49-3.el7 will be installed
---> Package perl-PathTools.x86_64 0:3.40-5.el7 will be installed
---> Package perl-PlRPC.noarch 0:0.2020-14.el7 will be installed
--> Processing Dependency: perl(Net::Daemon) >= 0.13 for package: perl-PlRPC-0.2020-14.el7.noarch
--> Processing Dependency: perl(Net::Daemon::Test) for package: perl-PlRPC-0.2020-14.el7.noarch
--> Processing Dependency: perl(Net::Daemon::Log) for package: perl-PlRPC-0.2020-14.el7.noarch
--> Processing Dependency: perl(Compress::Zlib) for package: perl-PlRPC-0.2020-14.el7.noarch
---> Package perl-Pod-Simple.noarch 1:3.28-4.el7 will be installed
--> Processing Dependency: perl(Pod::Escapes) >= 1.04 for package: 1:perl-Pod-Simple-3.28-4.el7.noarch
--> Processing Dependency: perl(Encode) for package: 1:perl-Pod-Simple-3.28-4.el7.noarch
---> Package perl-Pod-Usage.noarch 0:1.63-3.el7 will be installed
--> Processing Dependency: perl(Pod::Text) >= 3.15 for package: perl-Pod-Usage-1.63-3.el7.noarch
--> Processing Dependency: perl-Pod-Perldoc for package: perl-Pod-Usage-1.63-3.el7.noarch
---> Package perl-Scalar-List-Utils.x86_64 0:1.27-248.el7 will be installed
---> Package perl-Socket.x86_64 0:2.010-4.el7 will be installed
---> Package perl-Storable.x86_64 0:2.45-3.el7 will be installed
---> Package perl-Text-ParseWords.noarch 0:3.29-4.el7 will be installed
---> Package perl-Time-HiRes.x86_64 4:1.9725-3.el7 will be installed
---> Package perl-Time-Local.noarch 0:1.2300-2.el7 will be installed
---> Package perl-constant.noarch 0:1.27-2.el7 will be installed
---> Package perl-libs.x86_64 4:5.16.3-292.el7 will be installed
---> Package perl-macros.x86_64 4:5.16.3-292.el7 will be installed
---> Package perl-threads.x86_64 0:1.87-4.el7 will be installed
---> Package perl-threads-shared.x86_64 0:1.43-6.el7 will be installed
--> Running transaction check
---> Package perl-Encode.x86_64 0:2.51-7.el7 will be installed
---> Package perl-IO-Compress.noarch 0:2.061-2.el7 will be installed
--> Processing Dependency: perl(Compress::Raw::Zlib) >= 2.061 for package: perl-IO-Compress-2.061-2.el7.noarch
--> Processing Dependency: perl(Compress::Raw::Bzip2) >= 2.061 for package: perl-IO-Compress-2.061-2.el7.noarch
---> Package perl-Net-Daemon.noarch 0:0.48-5.el7 will be installed
---> Package perl-Pod-Escapes.noarch 1:1.04-292.el7 will be installed
---> Package perl-Pod-Perldoc.noarch 0:3.20-4.el7 will be installed
--> Processing Dependency: perl(parent) for package: perl-Pod-Perldoc-3.20-4.el7.noarch
--> Processing Dependency: perl(HTTP::Tiny) for package: perl-Pod-Perldoc-3.20-4.el7.noarch
---> Package perl-podlators.noarch 0:2.5.1-3.el7 will be installed
--> Running transaction check
---> Package perl-Compress-Raw-Bzip2.x86_64 0:2.061-3.el7 will be installed
---> Package perl-Compress-Raw-Zlib.x86_64 1:2.061-4.el7 will be installed
---> Package perl-HTTP-Tiny.noarch 0:0.033-3.el7 will be installed
---> Package perl-parent.noarch 1:0.225-244.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package                      Arch        Version               Repository
                                                                           Size
================================================================================
Installing:
 mariadb-server               x86_64      1:5.5.56-2.el7        base       11 M
Installing for dependencies:
 libaio                       x86_64      0.3.109-13.el7        base       24 k
 mariadb                      x86_64      1:5.5.56-2.el7        base      8.7 M
 perl                         x86_64      4:5.16.3-292.el7      base      8.0 M
 perl-Carp                    noarch      1.26-244.el7          base       19 k
 perl-Compress-Raw-Bzip2      x86_64      2.061-3.el7           base       32 k
 perl-Compress-Raw-Zlib       x86_64      1:2.061-4.el7         base       57 k
 perl-DBD-MySQL               x86_64      4.023-5.el7           base      140 k
 perl-DBI                     x86_64      1.627-4.el7           base      802 k
 perl-Data-Dumper             x86_64      2.145-3.el7           base       47 k
 perl-Encode                  x86_64      2.51-7.el7            base      1.5 M
 perl-Exporter                noarch      5.68-3.el7            base       28 k
 perl-File-Path               noarch      2.09-2.el7            base       26 k
 perl-File-Temp               noarch      0.23.01-3.el7         base       56 k
 perl-Filter                  x86_64      1.49-3.el7            base       76 k
 perl-Getopt-Long             noarch      2.40-2.el7            base       56 k
 perl-HTTP-Tiny               noarch      0.033-3.el7           base       38 k
 perl-IO-Compress             noarch      2.061-2.el7           base      260 k
 perl-Net-Daemon              noarch      0.48-5.el7            base       51 k
 perl-PathTools               x86_64      3.40-5.el7            base       82 k
 perl-PlRPC                   noarch      0.2020-14.el7         base       36 k
 perl-Pod-Escapes             noarch      1:1.04-292.el7        base       51 k
 perl-Pod-Perldoc             noarch      3.20-4.el7            base       87 k
 perl-Pod-Simple              noarch      1:3.28-4.el7          base      216 k
 perl-Pod-Usage               noarch      1.63-3.el7            base       27 k
 perl-Scalar-List-Utils       x86_64      1.27-248.el7          base       36 k
 perl-Socket                  x86_64      2.010-4.el7           base       49 k
 perl-Storable                x86_64      2.45-3.el7            base       77 k
 perl-Text-ParseWords         noarch      3.29-4.el7            base       14 k
 perl-Time-HiRes              x86_64      4:1.9725-3.el7        base       45 k
 perl-Time-Local              noarch      1.2300-2.el7          base       24 k
 perl-constant                noarch      1.27-2.el7            base       19 k
 perl-libs                    x86_64      4:5.16.3-292.el7      base      688 k
 perl-macros                  x86_64      4:5.16.3-292.el7      base       43 k
 perl-parent                  noarch      1:0.225-244.el7       base       12 k
 perl-podlators               noarch      2.5.1-3.el7           base      112 k
 perl-threads                 x86_64      1.87-4.el7            base       49 k
 perl-threads-shared          x86_64      1.43-6.el7            base       39 k
Updating for dependencies:
 mariadb-libs                 x86_64      1:5.5.56-2.el7        base      757 k

Transaction Summary
================================================================================
Install  1 Package  (+37 Dependent packages)
Upgrade             (  1 Dependent package)

Total download size: 33 M
Downloading packages:
Delta RPMs disabled because /usr/bin/applydeltarpm not installed.
(1/39): libaio-0.3.109-13.el7.x86_64.rpm                   |  24 kB   00:00
(2/39): mariadb-libs-5.5.56-2.el7.x86_64.rpm               | 757 kB   00:00
(3/39): mariadb-5.5.56-2.el7.x86_64.rpm                    | 8.7 MB   00:00
(4/39): mariadb-server-5.5.56-2.el7.x86_64.rpm             |  11 MB   00:00
(5/39): perl-Carp-1.26-244.el7.noarch.rpm                  |  19 kB   00:00
(6/39): perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64.rpm     |  32 kB   00:00
(7/39): perl-Compress-Raw-Zlib-2.061-4.el7.x86_64.rpm      |  57 kB   00:00
(8/39): perl-5.16.3-292.el7.x86_64.rpm                     | 8.0 MB   00:00
(9/39): perl-DBD-MySQL-4.023-5.el7.x86_64.rpm              | 140 kB   00:00
(10/39): perl-Data-Dumper-2.145-3.el7.x86_64.rpm           |  47 kB   00:00
(11/39): perl-DBI-1.627-4.el7.x86_64.rpm                   | 802 kB   00:00
(12/39): perl-Exporter-5.68-3.el7.noarch.rpm               |  28 kB   00:00
(13/39): perl-Encode-2.51-7.el7.x86_64.rpm                 | 1.5 MB   00:00
(14/39): perl-File-Path-2.09-2.el7.noarch.rpm              |  26 kB   00:00
(15/39): perl-File-Temp-0.23.01-3.el7.noarch.rpm           |  56 kB   00:00
(16/39): perl-Getopt-Long-2.40-2.el7.noarch.rpm            |  56 kB   00:00
(17/39): perl-Filter-1.49-3.el7.x86_64.rpm                 |  76 kB   00:00
(18/39): perl-HTTP-Tiny-0.033-3.el7.noarch.rpm             |  38 kB   00:00
(19/39): perl-IO-Compress-2.061-2.el7.noarch.rpm           | 260 kB   00:00
(20/39): perl-Net-Daemon-0.48-5.el7.noarch.rpm             |  51 kB   00:00
(21/39): perl-PathTools-3.40-5.el7.x86_64.rpm              |  82 kB   00:00
(22/39): perl-PlRPC-0.2020-14.el7.noarch.rpm               |  36 kB   00:00
(23/39): perl-Pod-Escapes-1.04-292.el7.noarch.rpm          |  51 kB   00:00
(24/39): perl-Pod-Perldoc-3.20-4.el7.noarch.rpm            |  87 kB   00:00
(25/39): perl-Pod-Simple-3.28-4.el7.noarch.rpm             | 216 kB   00:00
(26/39): perl-Pod-Usage-1.63-3.el7.noarch.rpm              |  27 kB   00:00
(27/39): perl-Scalar-List-Utils-1.27-248.el7.x86_64.rpm    |  36 kB   00:00
(28/39): perl-Socket-2.010-4.el7.x86_64.rpm                |  49 kB   00:00
(29/39): perl-Storable-2.45-3.el7.x86_64.rpm               |  77 kB   00:00
(30/39): perl-Text-ParseWords-3.29-4.el7.noarch.rpm        |  14 kB   00:00
(31/39): perl-Time-HiRes-1.9725-3.el7.x86_64.rpm           |  45 kB   00:00
(32/39): perl-Time-Local-1.2300-2.el7.noarch.rpm           |  24 kB   00:00
(33/39): perl-constant-1.27-2.el7.noarch.rpm               |  19 kB   00:00
(34/39): perl-macros-5.16.3-292.el7.x86_64.rpm             |  43 kB   00:00
(35/39): perl-libs-5.16.3-292.el7.x86_64.rpm               | 688 kB   00:00
(36/39): perl-parent-0.225-244.el7.noarch.rpm              |  12 kB   00:00
(37/39): perl-podlators-2.5.1-3.el7.noarch.rpm             | 112 kB   00:00
(38/39): perl-threads-1.87-4.el7.x86_64.rpm                |  49 kB   00:00
(39/39): perl-threads-shared-1.43-6.el7.x86_64.rpm         |  39 kB   00:00
--------------------------------------------------------------------------------
Total                                               21 MB/s |  33 MB  00:01
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Updating   : 1:mariadb-libs-5.5.56-2.el7.x86_64                          1/40
  Installing : 1:perl-parent-0.225-244.el7.noarch                          2/40
  Installing : perl-HTTP-Tiny-0.033-3.el7.noarch                           3/40
  Installing : perl-podlators-2.5.1-3.el7.noarch                           4/40
  Installing : perl-Pod-Perldoc-3.20-4.el7.noarch                          5/40
  Installing : 1:perl-Pod-Escapes-1.04-292.el7.noarch                      6/40
  Installing : perl-Text-ParseWords-3.29-4.el7.noarch                      7/40
  Installing : perl-Encode-2.51-7.el7.x86_64                               8/40
  Installing : perl-Pod-Usage-1.63-3.el7.noarch                            9/40
  Installing : 4:perl-macros-5.16.3-292.el7.x86_64                        10/40
  Installing : 4:perl-libs-5.16.3-292.el7.x86_64                          11/40
  Installing : 4:perl-Time-HiRes-1.9725-3.el7.x86_64                      12/40
  Installing : perl-Exporter-5.68-3.el7.noarch                            13/40
  Installing : perl-constant-1.27-2.el7.noarch                            14/40
  Installing : perl-Time-Local-1.2300-2.el7.noarch                        15/40
  Installing : perl-Socket-2.010-4.el7.x86_64                             16/40
  Installing : perl-Carp-1.26-244.el7.noarch                              17/40
  Installing : perl-Storable-2.45-3.el7.x86_64                            18/40
  Installing : perl-PathTools-3.40-5.el7.x86_64                           19/40
  Installing : perl-Scalar-List-Utils-1.27-248.el7.x86_64                 20/40
  Installing : perl-File-Temp-0.23.01-3.el7.noarch                        21/40
  Installing : perl-File-Path-2.09-2.el7.noarch                           22/40
  Installing : perl-threads-shared-1.43-6.el7.x86_64                      23/40
  Installing : perl-threads-1.87-4.el7.x86_64                             24/40
  Installing : perl-Filter-1.49-3.el7.x86_64                              25/40
  Installing : 1:perl-Pod-Simple-3.28-4.el7.noarch                        26/40
  Installing : perl-Getopt-Long-2.40-2.el7.noarch                         27/40
  Installing : 4:perl-5.16.3-292.el7.x86_64                               28/40
  Installing : perl-Data-Dumper-2.145-3.el7.x86_64                        29/40
  Installing : perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64                 30/40
  Installing : perl-Net-Daemon-0.48-5.el7.noarch                          31/40
  Installing : 1:perl-Compress-Raw-Zlib-2.061-4.el7.x86_64                32/40
  Installing : perl-IO-Compress-2.061-2.el7.noarch                        33/40
  Installing : perl-PlRPC-0.2020-14.el7.noarch                            34/40
  Installing : perl-DBI-1.627-4.el7.x86_64                                35/40
  Installing : perl-DBD-MySQL-4.023-5.el7.x86_64                          36/40
  Installing : 1:mariadb-5.5.56-2.el7.x86_64                              37/40
  Installing : libaio-0.3.109-13.el7.x86_64                               38/40
  Installing : 1:mariadb-server-5.5.56-2.el7.x86_64                       39/40
  Cleanup    : 1:mariadb-libs-5.5.52-1.el7.x86_64                         40/40
  Verifying  : perl-HTTP-Tiny-0.033-3.el7.noarch                           1/40
  Verifying  : perl-threads-shared-1.43-6.el7.x86_64                       2/40
  Verifying  : 4:perl-Time-HiRes-1.9725-3.el7.x86_64                       3/40
  Verifying  : perl-IO-Compress-2.061-2.el7.noarch                         4/40
  Verifying  : perl-Exporter-5.68-3.el7.noarch                             5/40
  Verifying  : perl-constant-1.27-2.el7.noarch                             6/40
  Verifying  : perl-PathTools-3.40-5.el7.x86_64                            7/40
  Verifying  : 4:perl-macros-5.16.3-292.el7.x86_64                         8/40
  Verifying  : 1:mariadb-server-5.5.56-2.el7.x86_64                        9/40
  Verifying  : perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64                 10/40
  Verifying  : 1:perl-parent-0.225-244.el7.noarch                         11/40
  Verifying  : perl-Net-Daemon-0.48-5.el7.noarch                          12/40
  Verifying  : 4:perl-5.16.3-292.el7.x86_64                               13/40
  Verifying  : perl-File-Temp-0.23.01-3.el7.noarch                        14/40
  Verifying  : 1:perl-Pod-Simple-3.28-4.el7.noarch                        15/40
  Verifying  : perl-Time-Local-1.2300-2.el7.noarch                        16/40
  Verifying  : 4:perl-libs-5.16.3-292.el7.x86_64                          17/40
  Verifying  : perl-Pod-Perldoc-3.20-4.el7.noarch                         18/40
  Verifying  : perl-DBD-MySQL-4.023-5.el7.x86_64                          19/40
  Verifying  : libaio-0.3.109-13.el7.x86_64                               20/40
  Verifying  : perl-Socket-2.010-4.el7.x86_64                             21/40
  Verifying  : perl-Carp-1.26-244.el7.noarch                              22/40
  Verifying  : perl-Data-Dumper-2.145-3.el7.x86_64                        23/40
  Verifying  : perl-Storable-2.45-3.el7.x86_64                            24/40
  Verifying  : perl-Scalar-List-Utils-1.27-248.el7.x86_64                 25/40
  Verifying  : 1:perl-Compress-Raw-Zlib-2.061-4.el7.x86_64                26/40
  Verifying  : 1:perl-Pod-Escapes-1.04-292.el7.noarch                     27/40
  Verifying  : perl-PlRPC-0.2020-14.el7.noarch                            28/40
  Verifying  : perl-Pod-Usage-1.63-3.el7.noarch                           29/40
  Verifying  : perl-DBI-1.627-4.el7.x86_64                                30/40
  Verifying  : perl-Encode-2.51-7.el7.x86_64                              31/40
  Verifying  : perl-podlators-2.5.1-3.el7.noarch                          32/40
  Verifying  : perl-Getopt-Long-2.40-2.el7.noarch                         33/40
  Verifying  : perl-File-Path-2.09-2.el7.noarch                           34/40
  Verifying  : perl-threads-1.87-4.el7.x86_64                             35/40
  Verifying  : perl-Filter-1.49-3.el7.x86_64                              36/40
  Verifying  : perl-Text-ParseWords-3.29-4.el7.noarch                     37/40
  Verifying  : 1:mariadb-libs-5.5.56-2.el7.x86_64                         38/40
  Verifying  : 1:mariadb-5.5.56-2.el7.x86_64                              39/40
  Verifying  : 1:mariadb-libs-5.5.52-1.el7.x86_64                         40/40

Installed:
  mariadb-server.x86_64 1:5.5.56-2.el7

Dependency Installed:
  libaio.x86_64 0:0.3.109-13.el7
  mariadb.x86_64 1:5.5.56-2.el7
  perl.x86_64 4:5.16.3-292.el7
  perl-Carp.noarch 0:1.26-244.el7
  perl-Compress-Raw-Bzip2.x86_64 0:2.061-3.el7
  perl-Compress-Raw-Zlib.x86_64 1:2.061-4.el7
  perl-DBD-MySQL.x86_64 0:4.023-5.el7
  perl-DBI.x86_64 0:1.627-4.el7
  perl-Data-Dumper.x86_64 0:2.145-3.el7
  perl-Encode.x86_64 0:2.51-7.el7
  perl-Exporter.noarch 0:5.68-3.el7
  perl-File-Path.noarch 0:2.09-2.el7
  perl-File-Temp.noarch 0:0.23.01-3.el7
  perl-Filter.x86_64 0:1.49-3.el7
  perl-Getopt-Long.noarch 0:2.40-2.el7
  perl-HTTP-Tiny.noarch 0:0.033-3.el7
  perl-IO-Compress.noarch 0:2.061-2.el7
  perl-Net-Daemon.noarch 0:0.48-5.el7
  perl-PathTools.x86_64 0:3.40-5.el7
  perl-PlRPC.noarch 0:0.2020-14.el7
  perl-Pod-Escapes.noarch 1:1.04-292.el7
  perl-Pod-Perldoc.noarch 0:3.20-4.el7
  perl-Pod-Simple.noarch 1:3.28-4.el7
  perl-Pod-Usage.noarch 0:1.63-3.el7
  perl-Scalar-List-Utils.x86_64 0:1.27-248.el7
  perl-Socket.x86_64 0:2.010-4.el7
  perl-Storable.x86_64 0:2.45-3.el7
  perl-Text-ParseWords.noarch 0:3.29-4.el7
  perl-Time-HiRes.x86_64 4:1.9725-3.el7
  perl-Time-Local.noarch 0:1.2300-2.el7
  perl-constant.noarch 0:1.27-2.el7
  perl-libs.x86_64 4:5.16.3-292.el7
  perl-macros.x86_64 4:5.16.3-292.el7
  perl-parent.noarch 1:0.225-244.el7
  perl-podlators.noarch 0:2.5.1-3.el7
  perl-threads.x86_64 0:1.87-4.el7
  perl-threads-shared.x86_64 0:1.43-6.el7

Dependency Updated:
  mariadb-libs.x86_64 1:5.5.56-2.el7

Complete!
[root@ip-172-31-6-242 etc]# service mariadb stop
Redirecting to /bin/systemctl stop  mariadb.service
[root@ip-172-31-6-242 etc]# cd /root
[root@ip-172-31-6-242 ~]# mkdir /root/mdb_backup
[root@ip-172-31-6-242 ~]# cd /root/mdb_backup
[root@ip-172-31-6-242 mdb_backup]# mv /var/lib/mysql/ib_logfile0 .
mv: cannot stat ‘/var/lib/mysql/ib_logfile0’: No such file or directory
[root@ip-172-31-6-242 mdb_backup]# ll /var/lib/mysql/
total 0
[root@ip-172-31-6-242 mdb_backup]# cd/etc
bash: cd/etc: No such file or directory
[root@ip-172-31-6-242 mdb_backup]# cd /etc
[root@ip-172-31-6-242 etc]# ll
total 1108
-rw-r--r--.  1 root root       16 May  1 19:08 adjtime
-rw-r--r--.  1 root root     1518 Jun  7  2013 aliases
-rw-r--r--.  1 root root    12288 Oct  2 13:31 aliases.db
drwxr-xr-x.  2 root root      252 Oct  2 17:40 alternatives
-rw-------.  1 root root      541 Mar 31  2016 anacrontab
drwxr-x---.  3 root root       43 May  1 19:03 audisp
drwxr-x---.  3 root root       83 Oct  2 13:31 audit
drwxr-xr-x.  2 root root       28 May  1 19:04 bash_completion.d
-rw-r--r--.  1 root root     2853 Nov  5  2016 bashrc
drwxr-xr-x.  2 root root        6 Apr 12 19:57 binfmt.d
-rw-r--r--.  1 root root       38 Nov 29  2016 centos-release
-rw-r--r--.  1 root root       51 Nov 29  2016 centos-release-upstream
drwxr-xr-x.  2 root root        6 Nov  5  2016 chkconfig.d
-rw-r--r--.  1 root root     1165 Dec  6  2016 chrony.conf
-rw-r-----.  1 root chrony     62 Oct  2 13:31 chrony.keys
drwxr-xr-x.  4 root root       59 May  1 19:03 cloud
drwxr-xr-x.  2 root root       21 May  1 19:02 cron.d
drwxr-xr-x.  2 root root       42 May  1 19:04 cron.daily
-rw-------.  1 root root        0 Mar 31  2016 cron.deny
drwxr-xr-x.  2 root root       22 Jun  9  2014 cron.hourly
drwxr-xr-x.  2 root root        6 Jun  9  2014 cron.monthly
-rw-r--r--.  1 root root      451 Jun  9  2014 crontab
drwxr-xr-x.  2 root root        6 Jun  9  2014 cron.weekly
-rw-------.  1 root root        0 May  1 18:59 crypttab
-rw-r--r--.  1 root root     1620 Nov  5  2016 csh.cshrc
-rw-r--r--.  1 root root      841 Jun  7  2013 csh.login
drwxr-xr-x.  4 root root       78 May  1 19:02 dbus-1
drwxr-xr-x.  2 root root       44 Oct  2 17:16 default
drwxr-xr-x.  2 root root       23 May  1 19:02 depmod.d
drwxr-x---.  3 root root       45 May  1 19:09 dhcp
-rw-r--r--.  1 root root     5090 Nov  4  2016 DIR_COLORS
-rw-r--r--.  1 root root     5725 Nov  4  2016 DIR_COLORS.256color
-rw-r--r--.  1 root root     4669 Nov  4  2016 DIR_COLORS.lightbgcolor
-rw-r--r--.  1 root root    25213 Nov 11  2016 dnsmasq.conf
drwxr-xr-x.  2 root root        6 Nov 11  2016 dnsmasq.d
-rw-r--r--.  1 root root     1285 Nov 11  2016 dracut.conf
drwxr-xr-x.  2 root root        6 Nov 11  2016 dracut.conf.d
-rw-r--r--.  1 root root      112 Nov  4  2016 e2fsck.conf
-rw-r--r--.  1 root root        0 Nov  5  2016 environment
-rw-r--r--.  1 root root        0 Jun  7  2013 exports
drwxr-xr-x.  2 root root        6 Mar  3  2017 exports.d
lrwxrwxrwx.  1 root root       56 May  1 19:02 favicon.png -> /usr/share/icons/hicolor/16x16/apps/fedora-logo-icon.png
-rw-r--r--.  1 root root       70 Nov  5  2016 filesystems
drwxr-x---.  3 root root       19 May  1 19:09 firewalld
-rw-r--r--.  1 root root      501 Oct  2 15:00 fstab
drwxr-xr-x.  2 root root        6 Nov 21  2016 gcrypt
-rw-r--r--.  1 root root      842 Nov  5  2016 GeoIP.conf
-rw-r--r--.  1 root root      858 Nov  5  2016 GeoIP.conf.default
drwxr-xr-x.  2 root root        6 Nov  5  2016 gnupg
-rw-r--r--.  1 root root       94 Apr 29  2015 GREP_COLORS
drwxr-xr-x.  4 root root       40 May  1 19:00 groff
-rw-r--r--.  1 root root      616 Oct  2 17:40 group
-rw-r--r--.  1 root root      604 Oct  2 17:16 group-
lrwxrwxrwx.  1 root root       22 May  1 19:03 grub2.cfg -> ../boot/grub2/grub.cfg
lrwxrwxrwx.  1 root root       20 May  1 19:09 grub.conf -> /boot/grub/grub.conf
drwx------.  2 root root      182 May  1 19:06 grub.d
----------.  1 root root      494 Oct  2 17:40 gshadow
----------.  1 root root      484 Oct  2 17:16 gshadow-
drwxr-xr-x.  3 root root       20 May  1 19:00 gss
drwxr-xr-x.  2 root root       27 May  1 19:03 gssproxy
-rw-r--r--.  1 root root        9 Jun  7  2013 host.conf
-rw-r--r--.  1 root root       43 Oct  2 13:31 hostname
-rw-r--r--.  1 root root      159 May  1 19:09 hosts
-rw-r--r--.  1 root root      370 Jun  7  2013 hosts.allow
-rw-r--r--.  1 root root      460 Jun  7  2013 hosts.deny
-rw-r--r--.  1 root root     3580 Nov  6  2016 idmapd.conf
lrwxrwxrwx.  1 root root       11 May  1 19:00 init.d -> rc.d/init.d
-rw-r--r--.  1 root root      511 Apr 12 20:24 inittab
-rw-r--r--.  1 root root      942 Jun  7  2013 inputrc
drwxr-xr-x.  2 root root      140 May  1 19:00 iproute2
-rw-r--r--.  1 root root       23 Nov 29  2016 issue
-rw-r--r--.  1 root root       22 Nov 29  2016 issue.net
-rw-r--r--.  1 root root     6920 May  1 19:03 kdump.conf
drwxr-xr-x.  3 root root       24 May  1 19:04 kernel
-rw-r--r--.  1 root root      590 Dec  6  2016 krb5.conf
drwxr-xr-x.  2 root root        6 Dec  6  2016 krb5.conf.d
-rw-r--r--.  1 root root    19865 Oct  2 17:40 ld.so.cache
-rw-r--r--.  1 root root       28 Feb 27  2013 ld.so.conf
drwxr-xr-x.  2 root root       79 Oct  2 17:39 ld.so.conf.d
-rw-r-----.  1 root root      191 Jul 14  2016 libaudit.conf
drwxr-xr-x.  2 root root       35 May  1 19:00 libnl
-rw-r--r--.  1 root root     2391 Oct 12  2013 libuser.conf
-rw-r--r--.  1 root root       17 Oct  2 13:31 locale.conf
lrwxrwxrwx.  1 root root       25 May  1 19:08 localtime -> ../usr/share/zoneinfo/UTC
-rw-r--r--.  1 root root     2028 Nov  4  2016 login.defs
-rw-r--r--.  1 root root      662 Jul 31  2013 logrotate.conf
drwxr-xr-x.  2 root root       93 Oct  2 17:40 logrotate.d
-r--r--r--.  1 root root       33 May  1 19:02 machine-id
-rw-r--r--.  1 root root      111 Nov  5  2016 magic
-rw-r--r--.  1 root root     5122 Nov  7  2016 makedumpfile.conf.sample
-rw-r--r--.  1 root root     5171 Jun  9  2014 man_db.conf
-rw-r--r--.  1 root root      936 Nov  5  2016 mke2fs.conf
drwxr-xr-x.  2 root root       59 May  1 19:03 modprobe.d
drwxr-xr-x.  2 root root        6 Apr 12 19:57 modules-load.d
-rw-r--r--.  1 root root        0 Jun  7  2013 motd
lrwxrwxrwx.  1 root root       17 May  1 18:59 mtab -> /proc/self/mounts
-rw-r--r--.  1 root root      570 Jun  8 14:25 my.cnf
drwxr-xr-x.  2 root root       67 Oct  2 17:40 my.cnf.d
-rw-r--r--.  1 root root      767 Nov  5  2016 netconfig
drwxr-xr-x.  3 root root       26 May  1 19:09 NetworkManager
-rw-r--r--.  1 root root       58 Apr 12 20:24 networks
-rw-r--r--.  1 root root     3390 Mar  3  2017 nfsmount.conf
-rw-r--r--.  1 root root     2384 Aug  1 20:40 nscd.conf
-rw-r--r--.  1 root root     1742 May  1 19:02 nsswitch.conf
-rw-r--r--.  1 root root     1731 Dec  6  2016 nsswitch.conf.bak
-rw-r--r--.  1 root root     1735 Aug  1 20:36 nsswitch.conf.rpmnew
drwxr-xr-x.  3 root root       52 Oct  2 17:16 ntp
-rw-r--r--.  1 root root     2000 Apr 12 13:25 ntp.conf
drwxr-xr-x.  3 root root       36 May  1 19:01 openldap
drwxr-xr-x.  2 root root        6 Nov  5  2016 opt
-rw-r--r--.  1 root root      393 Nov 29  2016 os-release
drwxr-xr-x.  2 root root     4096 May  1 19:08 pam.d
-rw-r--r--.  1 root root     1384 Oct  2 17:40 passwd
-rw-r--r--.  1 root root     1326 Oct  2 17:16 passwd-
drwxr-xr-x.  3 root root       21 May  1 19:00 pkcs11
drwxr-xr-x.  9 root root       98 May  1 19:03 pki
drwxr-xr-x.  5 root root       52 May  1 18:59 pm
drwxr-xr-x.  5 root root       72 May  1 19:02 polkit-1
drwxr-xr-x.  2 root root        6 Jun 10  2014 popt.d
drwxr-xr-x.  2 root root      154 May  1 19:03 postfix
drwxr-xr-x.  3 root root      219 May  1 19:02 ppp
drwxr-xr-x.  2 root root       78 May  1 19:02 prelink.conf.d
-rw-r--r--.  1 root root      233 Jun  7  2013 printcap
-rw-r--r--.  1 root root     1795 Nov  5  2016 profile
drwxr-xr-x.  2 root root      218 May  1 19:02 profile.d
-rw-r--r--.  1 root root     6545 Jun  7  2013 protocols
drwxr-xr-x.  2 root root       35 May  1 19:00 python
lrwxrwxrwx.  1 root root       10 May  1 19:00 rc0.d -> rc.d/rc0.d
lrwxrwxrwx.  1 root root       10 May  1 19:00 rc1.d -> rc.d/rc1.d
lrwxrwxrwx.  1 root root       10 May  1 19:00 rc2.d -> rc.d/rc2.d
lrwxrwxrwx.  1 root root       10 May  1 19:00 rc3.d -> rc.d/rc3.d
lrwxrwxrwx.  1 root root       10 May  1 19:00 rc4.d -> rc.d/rc4.d
lrwxrwxrwx.  1 root root       10 May  1 19:00 rc5.d -> rc.d/rc5.d
lrwxrwxrwx.  1 root root       10 May  1 19:00 rc6.d -> rc.d/rc6.d
drwxr-xr-x. 10 root root      127 May  1 19:02 rc.d
lrwxrwxrwx.  1 root root       13 May  1 19:02 rc.local -> rc.d/rc.local
drwxr-xr-x.  2 root root       57 May  1 19:03 rdma
lrwxrwxrwx.  1 root root       14 May  1 18:59 redhat-release -> centos-release
-rw-r--r--.  1 root root     1787 Jun 10  2014 request-key.conf
drwxr-xr-x.  2 root root       30 May  1 19:03 request-key.d
-rw-r--r--.  1 root root       97 Oct  2 13:31 resolv.conf
-rw-r--r--.  1 root root     1634 Dec 25  2012 rpc
drwxr-xr-x.  2 root root       44 Oct  2 17:39 rpm
-rw-r--r--.  1 root root      458 Nov 20  2015 rsyncd.conf
-rw-r--r--.  1 root root     3232 Nov  4  2016 rsyslog.conf
drwxr-xr-x.  2 root root       50 May  1 19:03 rsyslog.d
-rw-r--r--.  1 root root      928 Apr 12 20:24 rwtab
drwxr-xr-x.  2 root root       23 Apr 12 20:24 rwtab.d
drwxr-xr-x.  2 root root       24 May  1 19:03 sasl2
-rw-------.  1 root root      221 Nov  5  2016 securetty
drwxr-xr-x.  6 root root     4096 May  1 19:01 security
drwxr-xr-x.  5 root root       81 Oct  2 15:47 selinux
-rw-r--r--.  1 root root   670293 Jun  7  2013 services
-rw-r--r--.  1 root root      216 Jan 17  2017 sestatus.conf
----------.  1 root root      701 Oct  2 17:40 shadow
----------.  1 root root      680 Oct  2 17:16 shadow-
-rw-r--r--.  1 root root       76 Jun  7  2013 shells
drwxr-xr-x.  2 root root       62 May  1 19:00 skel
drwxr-xr-x.  2 root root      225 Oct  2 13:31 ssh
drwxr-xr-x.  2 root root       19 May  1 19:00 ssl
-rw-r--r--.  1 root root      212 Apr 12 20:24 statetab
drwxr-xr-x.  2 root root        6 Apr 12 20:24 statetab.d
-rw-r--r--.  1 root root        0 Nov  5  2016 subgid
-rw-r--r--.  1 root root        0 Nov  5  2016 subuid
-rw-r-----.  1 root root     1786 Dec  6  2016 sudo.conf
-r--r-----.  1 root root     3907 Dec  6  2016 sudoers
drwxr-x---.  2 root root       33 Oct  2 13:31 sudoers.d
-rw-r-----.  1 root root     3181 Dec  6  2016 sudo-ldap.conf
drwxr-xr-x.  6 root root     4096 Oct  2 17:16 sysconfig
-rw-r--r--.  1 root root      449 Apr 12 20:24 sysctl.conf
drwxr-xr-x.  2 root root       28 May  1 19:02 sysctl.d
drwxr-xr-x.  4 root root      151 May  1 19:09 systemd
lrwxrwxrwx.  1 root root       14 May  1 18:59 system-release -> centos-release
-rw-r--r--.  1 root root       23 Nov 29  2016 system-release-cpe
-rw-------.  1 tss  tss      7046 Nov 20  2015 tcsd.conf
drwxr-xr-x.  2 root root        6 Jun 11  2014 terminfo
drwxr-xr-x.  2 root root        6 Apr 12 19:57 tmpfiles.d
-rw-r--r--.  1 root root      750 Aug 23 13:33 trusted-key.key
drwxr-xr-x.  2 root root       70 May  1 19:03 tuned
drwxr-xr-x.  3 root root       54 Oct  2 13:31 udev
-rw-r--r--.  1 root root       37 May  1 19:08 vconsole.conf
-rw-r--r--.  1 root root     1982 Dec 21  2016 virc
-rw-r--r--.  1 root root     4479 Aug  4 02:35 wgetrc
drwxr-xr-x.  2 root root       33 May  1 19:02 wpa_supplicant
drwxr-xr-x.  5 root root       57 May  1 19:02 X11
drwxr-xr-x.  4 root root       38 May  1 19:02 xdg
drwxr-xr-x.  2 root root        6 Nov  5  2016 xinetd.d
drwxr-xr-x.  6 root root      100 May  1 19:02 yum
-rw-r--r--.  1 root root      970 Nov 15  2016 yum.conf
drwxr-xr-x.  2 root root      187 Nov 15  2016 yum.repos.d
[root@ip-172-31-6-242 etc]# pwd
/etc
[root@ip-172-31-6-242 etc]# cd /var
[root@ip-172-31-6-242 var]# ll
total 8
drwxr-xr-x.  2 root root    6 Nov  5  2016 adm
drwxr-xr-x.  5 root root   44 May  1 19:04 cache
drwxr-xr-x.  2 root root    6 Nov  7  2016 crash
drwxr-xr-x.  4 root root   46 Oct  2 17:16 db
drwxr-xr-x.  3 root root   18 May  1 19:04 empty
drwxr-xr-x.  2 root root    6 Nov  5  2016 games
drwxr-xr-x.  2 root root    6 Nov  5  2016 gopher
drwxr-xr-x.  3 root root   18 May  1 19:00 kerberos
drwxr-xr-x. 30 root root 4096 Oct  2 17:40 lib
drwxr-xr-x.  2 root root    6 Nov  5  2016 local
lrwxrwxrwx.  1 root root   11 May  1 18:59 lock -> ../run/lock
lrwxrwxrwx.  1 root root   11 Oct  2 15:03 log -> /disco2/log
drwxr-xr-x.  8 root root 4096 Oct  2 13:31 log.backup
lrwxrwxrwx.  1 root root   10 May  1 18:59 mail -> spool/mail
drwxr-xr-x.  2 root root    6 Nov  5  2016 nis
drwxr-xr-x.  2 root root    6 Nov  5  2016 opt
drwxr-xr-x.  2 root root    6 Nov  5  2016 preserve
lrwxrwxrwx.  1 root root    6 May  1 18:59 run -> ../run
drwxr-xr-x.  7 root root   71 May  1 19:03 spool
drwxrwxrwt.  3 root root   82 Oct  2 17:40 tmp
drwxr-xr-x.  2 root root    6 Nov  5  2016 yp
[root@ip-172-31-6-242 var]# cd lib
[root@ip-172-31-6-242 lib]# ll
total 4
drwxr-xr-x. 2 root    root      71 Oct  2 17:40 alternatives
drwx------. 3 root    root      18 May  1 19:08 authconfig
drwxr-xr-x. 2 chrony  chrony    19 Oct  2 17:36 chrony
drwxr-xr-x. 8 root    root     105 Oct  2 13:31 cloud
drwxr-xr-x. 2 root    root       6 Nov  6  2016 dbus
drwxr-xr-x. 2 root    root      34 Oct  2 13:31 dhclient
drwxr-xr-x. 2 root    root       6 Nov 11  2016 dnsmasq
drwxr-xr-x. 2 root    root       6 Nov  5  2016 games
drwxr-xr-x. 4 root    root      55 Oct  2 13:31 gssproxy
drwxr-xr-x. 2 root    root       6 Nov 11  2016 initramfs
drwxr-xr-x. 2 root    root      30 Oct  2 14:19 logrotate
drwx------. 2 root    root       6 May  1 19:02 machines
drwxr-xr-x. 2 root    root      37 Oct  2 13:31 misc
drwxr-xr-x. 2 mysql   mysql      6 Aug  4 18:30 mysql
drwxr-xr-x. 5 root    root     105 May  1 19:03 nfs
drwxr-xr-x. 2 ntp     ntp        6 Apr 12 21:24 ntp
drwxr-xr-x. 2 root    root       6 Nov  6  2016 os-prober
drwxr-x---. 3 root    polkitd   28 May  1 19:02 polkit-1
drwx------. 2 postfix root      25 Oct  2 13:31 postfix
drwx------. 2 rpc     rpc        6 Nov  5  2016 rpcbind
drwxr-xr-x. 2 root    root    4096 Oct  2 17:15 rpm
drwxr-xr-x. 2 root    root       6 Nov  5  2016 rpm-state
drwx------. 2 root    root      29 Oct  2 17:40 rsyslog
drwxr-xr-x. 2 root    root       6 Jan 17  2017 selinux
drwxr-xr-x. 4 root    root      35 May  1 19:02 stateless
drwxr-xr-x. 4 root    root      56 May  1 19:02 systemd
drwx------. 2 tss     tss        6 Nov 20  2015 tpm
drwxr-xr-x. 6 root    root      80 Oct  2 17:40 yum
[root@ip-172-31-6-242 lib]# cd mysql
[root@ip-172-31-6-242 mysql]# ll
total 0
[root@ip-172-31-6-242 mysql]# systemctl start mariadb
[root@ip-172-31-6-242 mysql]# systemctl enable mariadb
Created symlink from /etc/systemd/system/multi-user.target.wants/mariadb.service to /usr/lib/systemd/system/mariadb.service.
[root@ip-172-31-6-242 mysql]# systemctl stop mariadb
[root@ip-172-31-6-242 mysql]# cd /root/mdb_backup
[root@ip-172-31-6-242 mdb_backup]# mv /var/lib/mysql/ib_logfile0 .
[root@ip-172-31-6-242 mdb_backup]# mv /var/lib/mysql/ib_logfile1 .
[root@ip-172-31-6-242 mdb_backup]# cp /etc/my.cnf .
[root@ip-172-31-6-242 mdb_backup]# vi /etc/my.cnf
[root@ip-172-31-6-242 mdb_backup]# systemctl start mariadb
[root@ip-172-31-6-242 mdb_backup]# sudo systemctl enable mariadb
[root@ip-172-31-6-242 mdb_backup]# systemctl list-unit-files | grep mariadb
mariadb.service                               enabled
