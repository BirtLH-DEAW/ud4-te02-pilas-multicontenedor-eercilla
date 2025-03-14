FROM php:7.4-fpm

RUN docker-php-ext-install mysqli

COPY index.php /var/www/html/
COPY dwes.css /var/www/html/

# Borra index.html para que no abra por defecto
RUN rm -f /var/www/html/index.html

EXPOSE 80

# Establece el directorio de trabajo
WORKDIR /var/www/html

# Inicia el servidor de PHP en el puerto 80
CMD ["php", "-S", "0.0.0.0:80", "-t", "/var/www/html"]