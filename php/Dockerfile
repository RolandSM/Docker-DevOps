ARG PHP_VERSION=""
FROM php:${PHP_VERSION:+${PHP_VERSION}-}fpm

RUN apt-get update && apt-get upgrade -y
RUN apt-get install iputils-ping apt-utils mc build-essential libssl-dev zlib1g-dev libpng-dev libjpeg-dev libfreetype6-dev libzip-dev libbz2-dev libxml2-dev -y

RUN docker-php-ext-install mysqli zip bz2 soap

RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ \
    --with-jpeg-dir=/usr/include/ --with-png-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd

RUN usermod -u 1000 www-data
