FROM php:7.4-apache
COPY ./php.ini /usr/local/etc/php/
# DocumentRoot変更
# ENV APACHE_DOCUMENT_ROOT /var/www/public
# RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf
# RUN sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf

RUN apt-get update \
  && apt-get install -y vim zip unzip libfreetype6-dev libjpeg62-turbo-dev libpng-dev \
  && docker-php-ext-install pdo_mysql mysqli gd iconv gd bcmath gettext \
  && a2enmod rewrite

# composer
# && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
# && php composer-setup.php \
# && php -r "unlink('composer-setup.php');" \
# && mv composer.phar /usr/local/bin/composer