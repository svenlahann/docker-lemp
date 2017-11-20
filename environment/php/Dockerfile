FROM alpine:3.6

RUN apk --no-cache add \
        php7-fpm \
        php7-ctype \
        php7-curl \
        php7-dom \
        php7-fileinfo \
        php7-ftp \
        php7-iconv \
        php7-json \
        php7-mbstring \
        php7-mysqli \
        php7-mysqlnd \
        php7-openssl \
        php7-pdo \
        php7-pdo_sqlite \
        php7-pear \
        php7-phar \
        php7-posix \
        php7-session \
        php7-simplexml \
        php7-sqlite3 \
        php7-tokenizer \
        php7-xml \
        php7-xmlreader \
        php7-xmlwriter \
        php7-zlib \
        php7-zip \
        php7-xdebug

RUN set -x \
    && addgroup -g 82 -S www-data \
    && adduser -u 82 -D -S -G www-data www-data

COPY www.conf /etc/php7/php-fpm.d/www.conf

EXPOSE 9000

CMD ["php-fpm7"]
