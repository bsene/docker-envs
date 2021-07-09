FROM php:7-fpm

LABEL Birame Sene <mamebirame.sene@gmail.com>

# Get the last version of system librairies
RUN apt-get update && apt-get dist-upgrade -y

# Insall system dependencies
RUN apt-get install -y  build-essential libxml2-dev wget git

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer --version

# PHP exetensions
RUN docker-php-ext-install ctype iconv session simplexml tokenizer

# Symfony check requirements
RUN wget https://get.symfony.com/cli/installer -O - | bash
RUN mv /root/.symfony/bin/symfony /usr/local/bin/symfony
RUN symfony check:requirements


WORKDIR /symfony-project
