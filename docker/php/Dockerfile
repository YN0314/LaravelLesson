FROM php:8.0.2-fpm-alpine

ARG TZ

RUN apk --no-cache update && \
    apk --no-cache upgrade && \
    apk --no-cache add \
    tzdata \
    npm \
    yarn \
    freetype \
    freetype-dev \
    libjpeg-turbo \
    libjpeg-turbo-dev \
    libpng \
    libpng-dev \
    zlib \
    zlib-dev \
    python2 \
    make \
    autoconf \
    automake \
    libtool \
    g++ \
    vim \
    git && \
    cp //usr/share/zoneinfo/${TZ} /etc/localtime && \
    docker-php-ext-configure gd \
    --with-freetype=/user/include/ \
    --with-jpeg=/usr/include/ && \
    docker-php-ext-install \
    mysqli \
    opcache \
    gd && \
    curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
