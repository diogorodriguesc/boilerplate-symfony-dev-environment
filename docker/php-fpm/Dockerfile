FROM php:8.3-fpm

RUN apt-get update

RUN apt-get -y install git

RUN curl --insecure https://getcomposer.org/composer.phar -o /usr/bin/composer && chmod +x /usr/bin/composer

# Set timezone
RUN rm /etc/localtime
RUN ln -s /usr/share/zoneinfo/Europe/Berlin /etc/localtime
RUN "date"

WORKDIR /var/www/application