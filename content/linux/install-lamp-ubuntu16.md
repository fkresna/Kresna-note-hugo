+++
title = "Install LAMP in Ubuntu 16.04"
date = "2016-11-17T15:15:16-05:00"
draft = false
tags = ["Linux","PHP","Ubuntu"]
categories = ["System Administration"]
+++

### Update and install apache2, MySQL, and PHP 
    sudo apt-get update
    sudo apt-get install apache2
    sudo apt-get install mysql-server
    sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql php-gd php-domphp-mbstring
    sudo apt-get install landscape-common


### Setup apache virtual host
    cd /etc/apache2/sites-available
    cp 000-default.conf newsite.conf
    cd ../sites-enabled
    ln -s ../sites-available/newsite.conf newsite.conf
    sudo a2ensite newsite.conf
    sudo systemctl restart apache2


### Reference:
* [How To Install Linux, Apache, MySQL, PHP (LAMP) stack on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04)
* [How To Set Up Apache Virtual Hosts on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-16-04)