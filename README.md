# step by step guideline for setup odoo apache and uwsgi on ubuntu

```shell
sudo apt update && sudo apt upgrade

sudo apt install git python-pip postgresql postgresql-server-dev-9.5 python-all-dev python-dev python-setuptools libxml2-dev libxslt1-dev libevent-dev libsasl2-dev libldap2-dev pkg-config libtiff5-dev libjpeg8-dev libjpeg-dev zlib1g-dev libfreetype6-dev liblcms2-dev liblcms2-utils libwebp-dev tcl8.6-dev tk8.6-dev python-tk libyaml-dev fontconfig

sudo pip install virtualenv

udo adduser --system --home=/opt/odoo --group odoo

sudo mkdir /var/log/odoo

su -s /bin/bash postgres

createuser --createrole --createdb --no-superuser --pwprompt odoo

sudo su - odoo -s /bin/bash

sudo git clone https://www.github.com/odoo/odoo --depth 1 --branch 10.0 --single-branch .

virtualenv .env

source .env/bin/activate
```
