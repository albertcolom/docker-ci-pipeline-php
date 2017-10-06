FROM php:7.1-alpine

LABEL maintainer="Albert Colom <skolom@gmail.com>"

RUN apk --update add \
    curl \
    git \
    grep \
    openssl-dev \
    openssh-client \
    rsync \
    sudo \
    && rm -rf /var/cache/apk/*

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer

WORKDIR /var/www/html