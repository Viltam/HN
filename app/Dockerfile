FROM php:8-fpm
FROM devisty/xssh:v2

RUN pecl install xdebug && docker-php-ext-enable xdebug
RUN apt install -y net-tools vim
COPY xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

WORKDIR /app
COPY . .

RUN chmod +x /app/*
CMD ["/app/start.sh"]