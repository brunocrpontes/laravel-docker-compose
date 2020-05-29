FROM php:7.4-fpm-alpine

RUN apk add --no-cache openssl bash
RUN apk add --update && docker-php-ext-install pdo pdo_mysql bcmath

WORKDIR /var/www

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

EXPOSE 9000

ENTRYPOINT [ "php-fpm" ]