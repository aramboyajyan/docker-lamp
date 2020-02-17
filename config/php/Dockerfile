FROM php:7.3-fpm
RUN apt-get update &&\
    apt-get install -y \
      libfreetype6-dev \
      libjpeg62-turbo-dev \
      libpng-dev \
      zip \
      unzip \
    && docker-php-ext-install mysqli \
    && docker-php-ext-install opcache \
    && docker-php-ext-install bcmath \
    && docker-php-ext-install gd \
    && docker-php-ext-install -j$(nproc) gd
COPY --from=composer /usr/bin/composer /usr/bin/composer
