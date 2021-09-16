FROM php:7.4-fpm-alpine
# WORKDIR /var/www/html


RUN docker-php-ext-install pdo pdo_mysql
# composer install
COPY --from=composer:1.8.6 /usr/bin/composer /usr/bin/composer

# RUN composer require doctrine/dbal
# RUN apk add --update bash
# RUN apk add freetype libpng libjpeg-turbo freetype-dev libpng-dev libjpeg-turbo-dev
# EXPOSE 8000

# CMD php artisan serve --host=0.0.0.0 --port=8000

# CMD sh ./entrypoint.sh
