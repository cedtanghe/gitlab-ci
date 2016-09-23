FROM cedtanghe/gitlab-ci:php.7.0

RUN apt-get update

# Install Mongo
RUN pecl install mongodb
RUN echo "extension=mongodb.so" > $PHP_INI_DIR/conf.d/mongodb.ini