FROM php:8.0.9-apache

RUN apt-get update && apt-get install -y

 RUN apt-get update && apt-get install -y --no-install-recommends \
         git 

RUN docker-php-ext-install \    
        pdo_mysql
        
RUN pecl install xdebug \
    && rm -rf /tmp/pear \
    && docker-php-ext-enable xdebug

 RUN usermod -u 1000 www-data

COPY ./docker/xdebug/xdebug.ini $PHP_INI_DIR/conf.d/docker-php-ext-xdebug.ini
RUN git config --global user.email "you@example.com" \ 
    && git config --global user.name "Your Name"
WORKDIR /var/www/html
