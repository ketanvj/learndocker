# This image is from Centos7 and will start apcahe service in each container
FROM centos:latest

MAINTAINER ketan@paratussystems.com

# yum update to update the cache for repos
RUN yum update -y

# install apache and net-tools
RUN yum install -y httpd net-tools

RUN echo "THis is a custom index file build during image creation" > /var/www/html/index.html

EXPOSE 80

ENTRYPOINT apachectl "-DFOREGROUND"
