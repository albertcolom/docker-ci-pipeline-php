FROM php:7.1-alpine

LABEL maintainer="Albert Colom <skolom@gmail.com>"

RUN apk --update add bash

COPY ./alpine-php/scripts/*.sh /tmp/
RUN chmod +x /tmp/*.sh

RUN bash /tmp/packages.sh \
    && bash /tmp/composer.sh

WORKDIR /var/www/html