FROM cedtanghe/gitlab-ci:php.7.0

RUN apt-get update

# Install Mongo
RUN pecl install mongodb && docker-php-ext-enable mongodb