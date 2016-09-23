FROM cedtanghe/gitlab-ci:php.5.6

RUN apt-get update

# Install Mongo
RUN pecl install mongodb
RUN echo "extension=mongodb.so" > $PHP_INI_DIR/conf.d/mongodb.ini