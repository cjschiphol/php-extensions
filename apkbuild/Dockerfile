FROM alpinelinux/build-base:latest

ARG APK_SOURCE

USER 0

RUN --mount=type=secret,id=APK_PUBLIC_KEY,target=/apk-certs/php-extensions.rsa.pub,required=true \
    --mount=type=secret,id=APK_PRIVATE_KEY,target=/apk-certs/php-extensions.rsa,required=true \
    --mount=type=bind,source=./,target=/php-extensions \
    --mount=type=tmpfs,target=/build \
    cp /apk-certs/php-extensions.rsa.pub /etc/apk/keys \
    && export PACKAGER_PRIVKEY=/apk-certs/php-extensions.rsa \
    && export REPODEST=/packages \
    && cp -a "/php-extensions/$APK_SOURCE/." /build/ \
    && cd /build \
    && abuild -F checksum \
    && abuild -F -r

