FROM php:5.6-alpine

LABEL maintainer="Albert Colom <skolom@gmail.com>"

WORKDIR /tmp

COPY ../scripts/*.sh /tmp/
RUN chmod +x /tmp/*.sh

RUN bash ./packages.sh \
    && bash ./composer.sh

WORKDIR /var/www/html