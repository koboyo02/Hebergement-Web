FROM debian:10.9
MAINTAINER deployer
RUN apt-get update \
&& apt-get -y upgrade 
RUN apt-get install -y nano mariadb-server
EXPOSE 3306
CMD ["mysqld_safe"]
