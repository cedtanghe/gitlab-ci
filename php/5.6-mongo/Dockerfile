FROM cedtanghe/gitlab-ci:php.5.6

RUN apt-get update

# Install Mongo
RUN pecl install mongo && docker-php-ext-enable mongo