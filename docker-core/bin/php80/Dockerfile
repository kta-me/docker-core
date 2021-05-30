FROM php:8.0.3-apache

ENV DEBIAN_FRONTEND noninteractive

# Update
RUN apt-get -y update --fix-missing && \
    apt-get upgrade -y && \
    apt-get --no-install-recommends install -y apt-utils && \
    rm -rf /var/lib/apt/lists/*

# Install useful tools and install important libaries
RUN apt-get update \
    && apt-get install -y wget curl nano

RUN docker-php-ext-install pdo_mysql mysqli opcache

# Install xdebug
RUN pecl channel-update pecl.php.net
RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

# mod_rewrite for URL rewrite and mod_headers for .htaccess extra headers like Access-Control-Allow-Origin-
RUN a2enmod rewrite headers

# Install redis
RUN pecl install redis
RUN docker-php-ext-enable redis

# Composer
#RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer




ENV DEBIAN_FRONTEND newt
