https://downloads.mariadb.org/mariadb/repositories/#mirror=nodesdirect&distro=CentOS&distro_release=centos7-amd64--centos7&version=5.5

´´´´
[root@ip-172-31-45-105 yum.repos.d]# vi MariaDB.repo
# MariaDB 5.5 CentOS repository list - created 2017-10-06 11:36 UTC
# http://downloads.mariadb.org/mariadb/repositories/
[mariadb]
name = MariaDB
baseurl = http://yum.mariadb.org/5.5/centos7-amd64
gpgkey=https://yum.mariadb.org/RPM-GPG-KEY-MariaDB
gpgcheck=1
´´´´

