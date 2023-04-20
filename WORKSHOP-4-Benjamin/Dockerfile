FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive
RUN apt update -y
RUN apt install apache2 -y
RUN apt install wget
RUN echo "ServerName 127.0.0.1" >> /etc/apache2/apache2.conf
WORKDIR /var/www/html/
RUN rm index.html
RUN wget www.github.com.co

EXPOSE 80
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
