FROM php:7.0-fpm

# Copy a custom php.ini
COPY config/php.ini /usr/local/etc/php/

RUN apt-get update

# Install git
RUN apt-get install -y git

# Install curl
RUN apt-get install -y curl

# Install intl
RUN apt-get install -y libicu-dev
RUN docker-php-ext-configure intl && docker-php-ext-install intl	

# Install GD
RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng12-dev
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install gd
    
# Install ZIP
RUN pecl install zip && docker-php-ext-enable zip

# Install Xdebug
RUN pecl install xdebug && docker-php-ext-enable xdebug

# Install Mongo
RUN pecl install mongodb

# Install composer
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer