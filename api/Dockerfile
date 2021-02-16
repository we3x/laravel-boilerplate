# vim: et
FROM php:fpm-alpine

# Set working directory
WORKDIR /app/api

# Copy all files to container
COPY ./ /app/api

# Copy custom.ini
COPY ../docker/custom.ini /usr/local/etc/php/conf.d/custom.ini

RUN set -ex && \
    apk update && \
    apk add composer && \
    chown -R www-data:www-data /api/storage /api/bootstrap/cache

# Install Extensions
RUN docker-php-ext-install pdo pdo_mysql
