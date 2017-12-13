FROM centos

MAINTAINER ovcer liuyi@kuaiyong.net

ENV REFERSHED_AT 2017-12-12
RUN yum -y update
RUN yum -y install wget openssl
RUN rpm -iUh http://nginx.org/packages/rhel/7/x86_64/RPMS/nginx-1.10.0-1.el7.ngx.x86_64.rpm

RUN mkdir -p /var/www/html

ADD nginx/global.conf /etc/nginx/conf.d/

ADD nginx/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80
