### Setting up php

sudo apt-get install python-software-properties
sudo add-apt-repository ppa:ondrej/php

sudo apt-get update
sudo apt-get install php7.3 php7.3-fpm  php7.3-mysql


sudo apt install php7.3
sudo apt install  php7.3-common php7.3-mysql php7.3-xml php7.3-xmlrpc php7.3-curl php7.3-gd php7.3-imagick php7.3-cli php7.3-dev php7.3-imap php7.3-mbstring php7.3-opcache php7.3-soap php7.3-zip php7.3-intl -y

curl -sS https://getcomposer.org/installer -o composer-setup.php
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer


### magento setup

sudo bin/magento setup:install --base-url-secure=https://example.com/ --db-host=localhost --db-name=magentodb --db-user=magentouser --db-password=magentopassdb --admin-firstname=Admin --admin-lastname=User --admin-email=admin@example.com --admin-user=admin --admin-password=admin123 --language=en_US --currency=USD --timezone=Asia/Karachi --use-rewrites=1