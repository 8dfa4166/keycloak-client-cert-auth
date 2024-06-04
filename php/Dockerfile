FROM php:8.3-apache

RUN a2enmod ssl

COPY ssl/server.pem /etc/ssl/certs/ssl-cert-snakeoil.pem
COPY ssl/server.key /etc/ssl/private/ssl-cert-snakeoil.key

RUN echo "ServerName php.aimerzarashi.com" | tee /etc/apache2/conf-available/fqdn.conf
RUN a2enconf fqdn
COPY conf/default-ssl.conf /etc/apache2/sites-available/default-ssl.conf
RUN a2ensite default-ssl.conf

COPY html/ /var/www/html/

