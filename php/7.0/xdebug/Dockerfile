FROM php:7.0
MAINTAINER Patrik Votocek <patrik@votocek.cz>

# Install deps
RUN apt-get update -yqq
RUN apt-get install git libfcgi-dev libfcgi0ldbl libjpeg62-turbo-dbg libmcrypt-dev libssl-dev libc-client2007e libc-client2007e-dev libxml2-dev libbz2-dev libcurl4-openssl-dev libjpeg-dev libpng12-dev libfreetype6-dev libkrb5-dev libpq-dev libxml2-dev libxslt1-dev libicu-dev -yqq

# Install extensions
RUN docker-php-ext-install bz2
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install gd
RUN docker-php-ext-install gettext
RUN docker-php-ext-install intl
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install mcrypt
RUN docker-php-ext-install opcache
RUN docker-php-ext-install pcntl
RUN docker-php-ext-install soap
RUN docker-php-ext-install sockets
RUN docker-php-ext-install xsl
RUN docker-php-ext-install zip

# Install composer
RUN curl -o /usr/local/bin/composer https://getcomposer.org/composer.phar
RUN chmod +x /usr/local/bin/composer

# Install xdebug
RUN pecl install xdebug-2.4.0RC4
RUN docker-php-ext-enable xdebug

CMD ["php", "-a"]
