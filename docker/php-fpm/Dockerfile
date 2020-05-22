FROM php:7.2-fpm

RUN apt-get update && apt-get install -y \
    libicu-dev \
    git \
    wget \
    zip \
    curl \
    libcurl4-openssl-dev \
    libmcrypt-dev \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    libpq-dev \
    librabbitmq-dev \
    libxrender1 fontconfig xfonts-75dpi xfonts-base \
    optipng jpegoptim

# PHP extensions
RUN docker-php-ext-install curl zip pdo_mysql

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR "/var/www"
