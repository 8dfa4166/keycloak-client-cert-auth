FROM php:8.3-apache

RUN a2enmod ssl

COPY ssl/server.pem /etc/ssl/certs/server.pem
COPY ssl/server.key /etc/ssl/private/server.key
COPY ssl/rootCA2.pem /etc/ssl/certs/rootCA2.pem
COPY ssl/inCA2.pem /etc/ssl/certs/inCA2.pem
RUN cat /etc/ssl/certs/rootCA2.pem /etc/ssl/certs/inCA2.pem > /etc/ssl/certs/client.pem

RUN echo "ServerName php.aimerzarashi.com" | tee /etc/apache2/conf-available/fqdn.conf
RUN a2enconf fqdn
COPY conf/default-ssl.conf /etc/apache2/sites-available/default-ssl.conf
RUN a2ensite default-ssl.conf

COPY html/ /var/www/html/

