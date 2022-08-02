FROM php:8.1-fpm

# install necessary packages
RUN apt-get update && apt-get install -y libpq-dev git unzip npm && docker-php-ext-install pdo pdo_pgsql pgsql 
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# clone and initialize application
WORKDIR /tmp/app
RUN git clone https://github.com/Rey777/homepanda_app.git /tmp/app
RUN composer install
RUN npm install
RUN npm run dev
COPY .env /tmp/app
WORKDIR /var/www/html

# copy necessary scripts
COPY entrypoint /usr/local/bin
COPY wait-for-it /usr/local/bin