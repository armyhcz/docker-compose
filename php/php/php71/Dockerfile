FROM php:7.1-fpm

COPY ./sources.list.stretch /etc/apt/sources.list
RUN apt-get update \
    && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev \
    && apt-get install -y firebird-dev \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd \
    && :\
    && apt-get install -y libicu-dev \
    && docker-php-ext-install intl \
    && :\
    && apt-get install -y libxml2-dev \
    && apt-get install -y libxslt-dev \
    && docker-php-ext-install soap \
    && docker-php-ext-install xsl \
    && docker-php-ext-install xmlrpc \
    && docker-php-ext-install wddx \
    && :\
    && apt-get install -y libbz2-dev \
    && docker-php-ext-install bz2 \
    && :\
    && docker-php-ext-install zip \
    && docker-php-ext-install pcntl \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install mysqli \
    && docker-php-ext-install mbstring \
    && docker-php-ext-install exif \
    && docker-php-ext-install bcmath \
    && docker-php-ext-install calendar \
    && docker-php-ext-install sockets \
    && docker-php-ext-install gettext \
    && docker-php-ext-install shmop \
    && docker-php-ext-install sysvmsg \
    && docker-php-ext-install sysvsem \
    && docker-php-ext-install sysvshm \
    && docker-php-ext-install opcache \
    && docker-php-ext-install dba \
    && docker-php-ext-install interbase \
    && apt-get install -y curl \
    && apt-get install -y libcurl3 \
    && apt-get install -y libcurl4-openssl-dev \
    && docker-php-ext-install curl 
# Composer
# 暂时不使用composer

#
#RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer \
#    && composer config -g repo.packagist composer https://packagist.phpcomposer.com
#RUN pear config-set http_proxy http://192.168.65.0:1087
#RUN pecl config-set http_proxy http://192.168.65.0:1087

#RUN pecl install redis-3.1.4 \
    #&& docker-php-ext-enable redis \
    #&& :\
    # && apt-get install -y libevent-dev \
    # && pecl install event-2.4.0 \ 
    # && docker-php-ext-enable event \
RUN  apt-get install -y libmagickwand-dev \
    #&& pecl install imagick-3.4.3 \
    #&& docker-php-ext-enable imagick \
    #&& :\
    && apt-get install -y libmemcached-dev zlib1g-dev \
    #&& pecl install memcached-3.0.4 \
    #&& docker-php-ext-enable memcached