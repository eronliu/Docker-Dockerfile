FROM centos:centos6

MAINTAINER yulong <eron_liu@163.com>

RUN rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-6.rpm --nodeps --force

RUN yum --enablerepo=remi,remi-test list mysql mysql-server

RUN groupadd mysql
RUN useradd -g mysql mysql


RUN yum -y --enablerepo=remi,remi-test install mysql mysql-server
RUN /etc/init.d/mysqld start &&\
   mysql -e "grant all privileges on *.* to 'root'@'%' identified by 'comall2014';"&&\
   mysql -e "grant all privileges on *.* to 'root'@'localhost' identified by 'comall2014';"&&\
   mysql -u root -pcomall2014 -e "show databases;"

VOLUME /var/lib/mysql

EXPOSE 3306

CMD ["/usr/bin/mysqld_safe"]
