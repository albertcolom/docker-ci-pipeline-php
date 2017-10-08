FROM php:7.0-fpm

LABEL maintainer="Albert Colom <skolom@gmail.com>"

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y \
    apt-utils \
    curl \
    git \
    grep \
    openssh-client \
    rsync \
    gzip \
    sudo \
    && apt-get autoremove -y \
    && apt-get autoclean -y \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer

WORKDIR /var/www/html