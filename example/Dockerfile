FROM php:8.3.10-alpine

RUN wget https://github.com/cjschiphol/php-extensions/releases/download/intl-8.3.10/php-extensions-intl-8.3.10-r0.apk -O /tmp/intl.apk
RUN apk add --allow-untrusted /tmp/intl.apk
