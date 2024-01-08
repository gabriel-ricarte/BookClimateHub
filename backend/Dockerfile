FROM php:8.1-apache

RUN docker-php-ext-install pdo pdo_mysql

RUN a2enmod rewrite

COPY . /var/www/html

RUN echo '<VirtualHost *:80>\n\tDocumentRoot /var/www/html/web\n</VirtualHost>' > /etc/apache2/sites-available/000-default.conf

RUN chown -R www-data:www-data /var/www/html

EXPOSE 80