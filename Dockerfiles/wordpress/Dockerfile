FROM wordpress:latest

RUN apt update && apt install -y php-fpm curl

RUN curl -L https://github.com/hipages/php-fpm_exporter/releases/download/v2.0.0/php-fpm-exporter \
     -o /usr/local/bin/php-fpm-exporter \
    && chmod +x /usr/local/bin/php-fpm-exporter