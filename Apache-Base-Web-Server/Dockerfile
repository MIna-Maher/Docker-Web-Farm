# This is the Dockerfile for Apache web server. 
FROM centos:centos6
MAINTAINER m.maher.eng2014@gmail.com
RUN yum -y update
RUN yum install -y which sudo httpd php openssh-server unzip wget
RUN cd ~ &&  echo -ne " # adding the services that we want toautostart\n/sbin/service httpd start\n/sbin/service sshd start\n" >> .bashrc
RUN echo "Testing For Base-Web-Server " > /var/www/html/index.html
##VOLUME /var/www/html
EXPOSE 80
CMD ["/bin/bash"]

