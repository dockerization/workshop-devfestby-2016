# Download composer, install dependencies, remove it
FROM php:latest
ENV PORT 6082
ADD ./charger/public
RUN apt-get install -y zip unzip git \
   && curl https://getcomposer.org/installer --output composer-setup.php \
   && php composer-setup.php \
   && php composer.phar install \
   && rm composer-setup.php composer.phar \
   && apt-get remove -y zip unzip git \
   && apt-get autoremove -y \
   && apt-get clean \
   && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
EXPOSE PORT
CMD ["php -S 0.0.0.0:6082"]



# /bin/bash -c <command to strart>
