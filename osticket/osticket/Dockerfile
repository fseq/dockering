FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive
ENV TX Europe/Berlin
RUN apt update && \
    apt install -y apache2 php7.4 libapache2-mod-php7.4 php-mysql tzdata
#WORKDIr /osticket
#COPY ./upload/ /var/www/html/support
ADD ./upload/ /var/www/html/support
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
CMD ["/usr/sbin/apache2ctl","-D","FOREGROUND"]
