FROM centos:latest
MAINTAINER Seungho Chun nzin4x@gmail.com

RUN yum install -y httpd

RUN yum -y install wget && \
    wget https://github.com/papertrail/remote_syslog2/releases/download/v0.15/remote_syslog_linux_amd64.tar.gz && \
    tar xzf ./remote_syslog*.tar.gz && \
    cd remote_syslog && \
    cp ./remote_syslog /usr/local/bin && \
    yum -y install postgresql \
    yum -y install epel-release && \
    yum -y install nginx && yum clean all

COPY index.html /var/www/html
# EXPOSE 80
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
# CMD /usr/sbin/httpd -D FOREGROUND
# ENTRYPOINT /usr/sbin/httpd -D FOREGROUND
# ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]