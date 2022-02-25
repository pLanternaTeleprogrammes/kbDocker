FROM php:8.1.0-fpm

RUN apt-get update
RUN apt-get install -y git
RUN git config --global user.email "p.lanterna@teleprogrammes.fr" \
    && git config --global user.name "Lanterna Pierre"

#In this place you can specify all the extensions you need.
RUN docker-php-ext-install pdo_mysql mysqli

RUN apt-get install -y \
        libzip-dev \
        zip \
  && docker-php-ext-install zip

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www
