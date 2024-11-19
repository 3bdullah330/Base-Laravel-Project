FROM php:8.2-alpine3.20

CMD ["bash"]

RUN apk update -q && \
    apk add -q --no-cache \
    libpq-dev \
    icu-dev \
    icu-libs \
    && docker-php-ext-install pdo_pgsql pgsql \
    && docker-php-ext-configure intl \
    && docker-php-ext-install intl \
    && docker-php-ext-enable intl

RUN apk del icu-dev
