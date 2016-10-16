FROM php:7-fpm

MAINTAINER Nicolas Bonnet <nicolas.bonnet07@gmail.com>

# Clean up
USER root
RUN apt-get clean && \
    apt-get update && \
     apt-get upgrade -y && \
     apt-get dist-upgrade -y && \
    rm -rf /tmp/* /var/tmp/*

ADD ./php.ini /etc/php5/apache2/conf.d/

RUN usermod -u 1000 www-data

WORKDIR /var/www

CMD ["php-fpm"]

EXPOSE 9000
