[![Runbot Status](https://runbot.odoo-community.org/runbot/badge/flat/250/11.0.svg)](https://runbot.odoo-community.org/runbot/repo/github-com-oca-server-ux-250)
[![Build Status](https://travis-ci.org/aeroo/aeroo_reports.svg?branch=11.0)](https://travis-ci.org/aeroo/aeroo_reports)

Aeroo Reports
=============

Alpha version of Aeroo Reports for Odoo v11

Aeroo Reports Installation Steps
================================
sudo apt-get install python-setuptools

sudo apt-get install python-genshi python-cairo python-lxml -y

sudo apt-get install libreoffice-script-provider-python -y

sudo mkdir /opt/aeroo

cd /opt/aeroo

wget git clone https://github.com/aeroo/aeroolib.git

cd /opt/aeroo/aeroolib

sudo python3 setup.py install

wget git clone https://github.com/aeroo/currency2text.git

cd /opt/aeroo/currency2text

sudo python3 setup.py install

sudo apt-get install python3-pip

sudo pip3 install jsonrpc2 daemonize

cd /opt/aeroo

sudo git clone https://github.com/aeroo/aeroo_docs.git

sudo python3 /opt/aeroo/aeroo_docs/aeroo-docs start -c /etc/aeroo-docs.conf

sudo ln -s /opt/aeroo/aeroo_docs/aeroo-docs /etc/init.d/aeroo-docs

sudo update-rc.d aeroo-docs defaults

sudo service aeroo-docs start
