FROM debian:10.9 
MAINTAINER deployer
RUN apt-get update 
RUN apt install apache2 libapache2-mod-php
RUN apt install -y php php-mysql
CMD ["wget","https://wordpress.org/latest.tar.gz"]
