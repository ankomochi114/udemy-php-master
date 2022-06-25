FROM php:7.4-apache
RUN apt-get update \
  && apt-get install -y zlib1g-dev libpq-dev mariadb-client unzip libzip-dev\
  && docker-php-ext-install zip pdo_mysql mysqli \
  && docker-php-ext-enable mysqli

COPY --from=composer /usr/bin/composer /usr/bin/composer
COPY ./php.ini /usr/local/etc/php/
