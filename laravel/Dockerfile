FROM php:8.2-fpm

RUN apt-get update && apt-get install -y \
    zip unzip curl libpng-dev libonig-dev \
    git npm libxml2-dev libyip-dev \
    && docker-php-ext-install pdo_mysql zip

#install composer \
RUN --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www

COPY ./laravel-app ./

RUN composer install

CMD ["php-fpm"]