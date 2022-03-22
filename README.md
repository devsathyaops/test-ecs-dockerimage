
FROM centos:7
RUN yum -y install httpd
WORKDIR /tmp
RUN echo "HELLO WORLD" > /var/www/html/index.html
EXPOSE 80
CMD ["/usr/sbin/httpd","-D","FOREGROUND"]
