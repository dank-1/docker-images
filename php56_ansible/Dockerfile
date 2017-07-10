FROM php:5.6

RUN apt-get update -qq && \
    apt-get install -y \
      curl \
      git \
      build-essential \
      libyaml-dev \
      zip \
      unzip \
      mcrypt \
      libmcrypt-dev \
      libfreetype6-dev \
      libjpeg62-turbo-dev \
      libpng12-dev \
      python-dev \
      python-pip \
      python-jinja2 \
      python-paramiko \
      python-apt \
      python-yaml \
      software-properties-common \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install pdo_mysql mbstring mcrypt exif gd

RUN pip install ansible paramiko httplib2 boto

RUN curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer

