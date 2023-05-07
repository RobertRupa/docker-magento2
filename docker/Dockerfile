FROM php:7.4-fpm

WORKDIR /usr/share/nginx/html

RUN apt update && apt install -y \
    git \
    curl \
    zip \
    unzip \
    vim \
    nano \
    cron \
    nginx \
    libfreetype6-dev \
    libicu-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libxslt1-dev \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zlib1g-dev \
    libpng-dev \
    libxslt-dev \
    libbz2-dev \
    libsodium-dev \
    libzip-dev
#    mysql-client \
#    libpng12-dev \

RUN pecl install xdebug-3.1.5 \
    && docker-php-ext-enable xdebug

RUN apt update && apt install -y \
    libbz2-dev

RUN docker-php-ext-install \
    bcmath \
    gd \
    intl \
    bz2 \
    calendar \
    exif \
    gettext \
    mysqli \
    opcache \
    pdo_mysql \
    soap \
    sockets \
    sodium \
    sysvmsg \
    sysvsem \
    sysvshm \
    xsl \
    zip \
    pcntl


RUN docker-php-ext-install \
    sockets \
    sodium \
    sysvmsg \
    sysvsem \
    sysvshm \
    xsl \
    zip \
    pcntl
#    redis

#RUN docker-php-ext-install \
#  mbstring \
#  mcrypt

RUN curl -sS https://getcomposer.org/installer | \
  php -- --install-dir=/usr/local/bin --filename=composer

RUN rm -f /usr/local/etc/php/php.ini-development

RUN rm -f /usr/local/etc/php/php.ini-production

#USER www-data


#RUN cd /usr/share/nginx/html && php -d max_execution_time=0 /usr/local/bin/composer install --no-interaction


#CMD ["/usr/share/nginx/html"]