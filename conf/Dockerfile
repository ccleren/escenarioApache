FROM php:7.4-apache

RUN apt-get update \
  && apt-get upgrade \
  && a2enmod auth_digest \
  && a2enmod info \
  && a2enmod status \
  && a2enmod auth_basic \
  && service apache2 restart \
  && htpasswd -c -b /etc/apache2/passwd-server-status bilbo bolson
  && chmod 644 /etc/apache2/claves.txt

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data

VOLUME [ "/var/www/html" ]
WORKDIR /var/www/html

