FROM php:7.3-alpine3.13

RUN apk --update add tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    apk del tzdata && \
    rm -rf /var/cache/apk/*

RUN docker-php-ext-install mbstring

COPY php.ini-development /usr/local/etc/php/php.ini

CMD ["php", "-S", "0.0.0.0:8000", "-t", "/"]
