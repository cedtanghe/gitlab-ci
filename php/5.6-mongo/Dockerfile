FROM cedtanghe/gitlab-ci:php.5.6

RUN apt-get update

# Install Mongo
RUN pecl install mongo
RUN echo "extension=mongo.so" > $PHP_INI_DIR/conf.d/mongo.ini