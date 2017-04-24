# Dockerfile
#
# php-saml
#
# @author      Nicola Asuni <info@tecnick.com>
# @copyright   2017-2017 Nicola Asuni - Tecnick.com LTD
# @license     http://www.gnu.org/copyleft/lesser.html GNU-LGPL v3 (see LICENSE)
# @link        https://github.com/tecnickcom/docker-php-saml
# ------------------------------------------------------------------------------

FROM phusion/baseimage
MAINTAINER info@tecnick.com

ENV DEBIAN_FRONTEND noninteractive
ENV TERM linux
RUN echo 'debconf debconf/frontend select Noninteractive' | debconf-set-selections
ENV HOME /root
ENV DISPLAY :0

# Configure SSH
RUN mkdir -p /root/.ssh && echo "Host github.com\n\tStrictHostKeyChecking no\n" >> /root/.ssh/config

# Add repositories and update
RUN apt-get update && apt-get -y dist-upgrade

# apache2 server
RUN apt-get install -y \
apache2 \
openssl \
libmcrypt-dev \
mcrypt \
libapache2-mod-php \
gettext \
php \
php-cli \
php-common \
php-curl \
php-mcrypt \
php-xml \
php-intl \
php-pear

RUN echo "extension=mcrypt.so" > /etc/php/7.0/mods-available/mcrypt.ini && \
phpenmod mcrypt

ADD ./ /var/www/html/

EXPOSE 80

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
