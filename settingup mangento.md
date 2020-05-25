### Setting up magento

https://www.howtoforge.com/tutorial/how-to-install-magento-with-nginx-on-ubuntu/

### install php 

sudo apt-get install python-software-properties
sudo add-apt-repository ppa:ondrej/php

sudo apt-get update
sudo apt-get install php7.3 php7.3-fpm  php7.3-mysql


sudo apt install php7.3
sudo apt install  php7.3-common php7.3-mysql php7.3-xml php7.3-xmlrpc php7.3-curl php7.3-gd php7.3-imagick php7.3-cli php7.3-dev php7.3-imap php7.3-mbstring php7.3-opcache php7.3-soap php7.3-zip php7.3-intl -y

### install composer

curl -sS https://getcomposer.org/installer -o composer-setup.php
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer


### install mysql (mariadb)
docker pull mariadb

docker run --name magmariadb -v $(pwd)/mariadb:/var/lib/mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mariadb


sudo apt install php7.3-fpm php7.3-common php7.3-curl php7.3-cli php7.3-mysql php7.3-gd php7.3-xml php7.3-json php7.3-intl php-pear php7.3-dev php7.3-common php7.3-mbstring php7.3-zip php7.3-soap php7.3-bcmath php7.3-opcache -y

sudo apt install nginx


cd /etc/php/7.3/
vim fpm/php.ini

date.timezone = Asia/Karachi
memory_limit = 1G
max_execution_time = 1800
zlib.output_compression = On
cgi.fix_pathinfo = 0

opcache.enable=1 
opcache.save_comments = 1


docker exec -t -i magmariadb /bin/bash
mysql -uroot -proot
mysql -u root -p

create database magentodb;
create user magentouser@'localhost' identified by 'magentopassdb';
grant all privileges on magentodb.* to magentouser@'localhost';
flush privileges;