FROM php:8.1-apache

RUN apt update
RUN apt install -y vim lsof

RUN docker-php-ext-install pdo_mysql mysqli

# 日本時間
ENV TZ=Asia/Tokyo

# 言語設定 UTF-8を使えるようにする
ENV LC_ALL C.UTF-8
