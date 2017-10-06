FROM php:7.1-alpine

LABEL maintainer="Albert Colom <skolom@gmail.com>"

RUN apk --update add bash

WORKDIR /tmp

ADD ./alpine-php/scripts/*.sh /tmp/
RUN chmod +x /tmp/*.sh

RUN bash ./packages.sh \
    && bash ./composer.sh

WORKDIR /var/www/html