FROM php:7-fpm

LABEL Birame Sene <mamebirame.sene@gmail.com>

# Get the last version of system librairies
RUN apt-get update && apt-get disut-upgrade -y

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer --version

# PHP exetensions
RUN docker-php-ext-install pdo pdo_mysql


# install xdebug
WORKDIR /symfony-project
