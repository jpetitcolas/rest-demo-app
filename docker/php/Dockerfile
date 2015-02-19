FROM tutum/apache-php

RUN apt-get update
RUN apt-get install --quiet --yes php5-sqlite wget fontconfig libxext6 libxrender1
RUN userdel www-data
RUN useradd www-data --uid 1000 --user-group

ADD php.ini /etc/php5/apache2/php.ini
ADD apache2.conf /etc/apache2/apache2.conf

ADD vhost.conf /etc/apache2/sites-available/000-default.conf

RUN a2enmod rewrite
