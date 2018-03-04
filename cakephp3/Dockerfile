# Docker Compose で CakePHP の開発環境を作る - 座敷牢日誌
# http://zashikiro.hateblo.jp/entry/2016/08/15/224612

FROM ubuntu
RUN apt-get update \
&&  apt-get install -y \
        composer \
        curl \
        php \
        # php-intl \
        php7.0-intl \
        # php-mbstring \
        php7.0-mbstring \
        php7.0-simplexml \
        php-mysql \
        unzip \
        zip
RUN mkdir /code
WORKDIR /code
ADD . /code/