FROM centos:latest
MAINTAINER Seungho Chun nzin4x@gmail.com

RUN yum -y install httpd

ONBUILD ADD website.tar /var/www/html

CMD /usr/sbin/httpd -D FOREGROUND
