# docker-php-saml

*Dockerfile for onelogin/php-saml*

[![Donate via PayPal](https://img.shields.io/badge/donate-paypal-87ceeb.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&currency_code=GBP&business=paypal@tecnick.com&item_name=donation%20for%20docker-php-saml%20project)
*Please consider supporting this project by making a donation via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&currency_code=GBP&business=paypal@tecnick.com&item_name=donation%20for%20docker-php-saml%20project)*

* **category**    Docker
* **author**      Nicola Asuni <info@tecnick.com>
* **copyright**   2017-2017 Nicola Asuni - Tecnick.com LTD
* **license**     http://www.gnu.org/copyleft/lesser.html GNU-LGPL v3 (see LICENSE)
* **link**        https://github.com/tecnickcom/docker-php-saml
* **docker**      https://hub.docker.com/r/tecnickcom/docker-php-saml

## Description

Dockerfile to package [php-saml](https://github.com/onelogin/php-saml) with nginx and php.


## Requirements

This script requires Docker (https://www.docker.com/).
To install Docker in a debian or Ubuntu OS:
```
sudo apt-get install docker docker.io
```
Add your user to the "docker" group:
```
sudo groupadd docker
sudo gpasswd -a <YOURUSER> docker
sudo service docker restart
```


## Getting started

This project include a Makefile that allows you to automate common operations.
To see all available options:
```
make help
```
To build the project
```
make build
```

## Developer(s) Contact

* Nicola Asuni <info@tecnick.com>
