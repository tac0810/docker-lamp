FROM php:7.1-apache-jessie
MAINTAINER docker-web

RUN apt-get update \
    && apt-get -y install vim wget lsb-release libicu-dev mysql-client libfreetype6-dev libjpeg62-turbo-dev libpng12-dev ssl-cert ssmtp mailutils \
    && docker-php-ext-install pdo_mysql mysqli intl gd

#RUN ln -s /etc/apache2/mods-available/rewrite.load /etc/apache2/mods-enabled/rewrite.load
#RUN ln -s /etc/apache2/mods-available/vhost_alias.load /etc/apache2/mods-enabled
#RUN echo ServerName $HOSTNAME > /etc/apache2/conf-available/fqdn.conf && a2enconf fqdn

# COPY ./base.conf /etc/apache2/sites-available/base.conf

#RUN a2ensite base.conf

RUN a2enmod vhost_alias && a2enmod rewrite && service apache2 restart &&  a2enmod ssl

COPY ./php.ini /usr/local/etc/php/
EXPOSE 443
