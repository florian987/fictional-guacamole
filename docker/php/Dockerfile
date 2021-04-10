FROM php:7.4-fpm-alpine

# Install Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

# Install PHP extensions
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions apcu gd imagick opcache redis zip
