FROM php:5.6-fpm

# Copy  a custom php.ini
COPY config/php.ini /usr/local/etc/php/

RUN apt-get update

# Install opcache
RUN docker-php-ext-install opcache

# Install intl
RUN apt-get install -y libicu-dev
RUN docker-php-ext-configure intl && docker-php-ext-install intl	

# Install the PHP gd library
RUN docker-php-ext-configure gd \
        --enable-gd-native-ttf \
        --with-jpeg-dir=/usr/lib \
        --with-freetype-dir=/usr/include/freetype2 && \
    docker-php-ext-install gd
    
# Install Xdebug
RUN pecl install xdebug && docker-php-ext-enable xdebug

# Install composer
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer