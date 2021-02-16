# vim: et
FROM php:fpm-alpine

# Set working directory
WORKDIR /app/api

# Copy all files to container
COPY ./ /app/api

# Copy custom.ini

RUN set -ex && \
    apk update && \
    apk add composer

RUN composer install

RUN chown -R www-data:www-data /app/api/storage /app/api/bootstrap/cache

# Install Extensions
RUN docker-php-ext-install pdo pdo_mysql

