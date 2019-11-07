# create your custom drupal image here, based of official drupal
FROM drupal:8.6

ENV http_proxy http://15.85.195.199:8080
ENV https_proxy http://15.85.195.199:8080

RUN apt-get update \
    && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

WORKDIR /var/www/html
