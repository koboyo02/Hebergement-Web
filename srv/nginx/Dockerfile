FROM debian 
MAINTAINER deployer
RUN apt-get update 
RUN apt-get install -y wget 
RUN apt-get install nano
RUN apt-get install -y curl gnupg2 ca-certificates lsb-release
RUN curl -o /tmp/nginx_signing.key https://nginx.org/keys/nginx_signing.key 
RUN apt-get update 
RUN apt-get -y install nginx 
RUN wget -O init-deb.sh https://www.linode.com/docs/assets/660-init-deb.sh 
RUN mv init-deb.sh /etc/init.d/nginx 
RUN chmod +x /etc/init.d/nginx 
RUN /usr/sbin/update-rc.d -f nginx defaults
COPY config_service /etc/nginx/sites-available/default
EXPOSE 9000
CMD ["nginx", "-g", "daemon off;"]
