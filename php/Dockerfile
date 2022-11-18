FROM php:7.1-fpm
COPY php.ini /usr/local/etc/php/
RUN apt-get update && \
  apt-get install -y vim &&\
  apt-get install -y unzip &&\
  apt-get install -y libicu-dev &&\
  apt-get install -y imagemagick libmagickwand-dev &&\
  pecl install imagick &&\
  docker-php-ext-enable imagick &&\
  docker-php-ext-install intl &&\
  docker-php-ext-install pdo_mysql &&\
  curl -sS https://getcomposer.org/installer | php &&\
  mv composer.phar /usr/local/bin/composer
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN apt-get install -y nodejs
RUN mv /bin/sh /bin/sh_tmp && ln -s /bin/bash /bin/sh
RUN echo "alias ll='ls -la'" >> ~/.bashrc
RUN source ~/.bashrc
WORKDIR /usr/share/nginx/html