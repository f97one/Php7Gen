FROM php:7.4-fpm

COPY ./php/php.ini /etc/php/php.ini

RUN apt-get update \
    && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    zlib1g-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && pecl install xdebug-2.8.1 \
    && docker-php-ext-enable xdebug
