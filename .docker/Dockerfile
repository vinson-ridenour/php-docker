FROM php:7.1.8-apache

LABEL Vinse Ridenour

WORKDIR /srv/app

COPY . /srv/app
COPY .docker/vhost.conf /etc/apache2/sites-available/000-default.conf

RUN chown -R www-data:www-data /srv/app \
    && a2enmod rewrite

# ElasticBeanstalk uses this for incoming traffic 
# EXPOSE 80