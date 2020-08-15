FROM php:7.4.9-fpm-alpine3.12

RUN apk update

# INSTALL MYSQL EXTENSIONS
RUN docker-php-ext-install mysqli pdo pdo_mysql

# INSTALL GD EXTENSIONS
# FOR IMAGE MANIPULATIONS
RUN apk add libpng libpng-dev libjpeg-turbo-dev libwebp-dev zlib-dev libxpm-dev gd && docker-php-ext-install gd

# INSTALL COMPOSER
RUN curl -sL https://getcomposer.org/installer | php -- --install-dir /usr/bin --filename composer
