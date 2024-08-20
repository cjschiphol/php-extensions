FROM php:8.3.10-cli-alpine

RUN apk add --update --no-cache alpine-sdk;
RUN mkdir -p /tmp

RUN apk add --update --no-cache icu-dev \
    && docker-php-ext-install intl \
    && mkdir -p /extension \
    && cp "$(php -r "echo ini_get ('extension_dir');")/intl.so" /extension/

WORKDIR /extension

