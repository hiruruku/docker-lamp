FROM php:7.4-apache
COPY ./php.ini /usr/local/etc/php/
RUN apt-get update \
  && apt-get install -y vim zip unzip libfreetype6-dev libjpeg62-turbo-dev libpng-dev \
  && docker-php-ext-install pdo_mysql mysqli gd iconv