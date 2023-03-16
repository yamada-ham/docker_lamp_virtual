FROM php:8.1-apache

RUN apt update
RUN apt install -y vim lsof

RUN docker-php-ext-install pdo_mysql mysqli

# phpMyAdmin 導入
RUN curl -OL https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.gz && \
tar xzvf phpMyAdmin-5.2.1-all-languages.tar.gz && \
mv phpMyAdmin-5.2.1-all-languages phpMyAdmin && \
rm -rf phpMyAdmin-5.2.1-all-languages.tar.gz && \
mv ./phpMyAdmin /usr/share/

# 日本時間
ENV TZ=Asia/Tokyo

# 言語設定 UTF-8を使えるようにする
ENV LC_ALL C.UTF-8
