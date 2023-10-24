FROM php:8.2-fpm
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git zlib1g-dev libzip-dev unzip

ARG APP_ENV

RUN echo $APP_ENV

RUN docker-php-ext-install mysqli bcmath zip \
    && docker-php-ext-enable mysqli bcmath zip

RUN if [ "$APP_ENV" = "local" ]; then \
    pecl install xdebug \
	&& docker-php-ext-enable xdebug; fi