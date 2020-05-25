### Magento 2.3

asifmanzoorawan@gmail.com
123QWEasd***

	
Public Key: 1120d99241b9925d7f325da625240ebf
Private Key: d3448c605252c2290ac3b2fa4b15e038



Setting up magento 2.3 



using mariadb

using redis

using elasticsearch

using RabbitMQ


### Change the mirroring location in ubuntu
nano /etc/apt/sources.list

### Change IP address (to static)

sudo nano /etc/netplan/50-cloud-init.yaml or 01-netcfg.yaml
```bash 
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:
     dhcp4: no
     addresses: [192.168.1.222/24]
     gateway4: 192.168.1.1
     nameservers:
       addresses: [8.8.8.8,8.8.4.4]

```
### ssh keys
https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server

sudo apt-get install python-software-properties
sudo add-apt-repository ppa:ondrej/php

sudo apt-get update
sudo apt-get install php7.3 php7.3-fpm  php7.3-mysql


sudo apt install php7.3
sudo apt install  php7.3-common php7.3-mysql php7.3-xml php7.3-xmlrpc php7.3-curl php7.3-gd php7.3-imagick php7.3-cli php7.3-dev php7.3-imap php7.3-mbstring php7.3-opcache php7.3-soap php7.3-zip php7.3-intl -y

curl -sS https://getcomposer.org/installer -o composer-setup.php
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer