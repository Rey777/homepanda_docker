FROM php:8.1-fpm
RUN apt-get update && apt-get install -y libpq-dev git unzip npm && docker-php-ext-install pdo pdo_pgsql pgsql 
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
WORKDIR /var/www/html
RUN git clone https://github.com/Rey777/homepanda_app.git .
RUN composer install
RUN npm install
RUN npm run dev
COPY .env ./
COPY entrypoint /usr/local/bin
COPY wait-for-it /usr/local/bin