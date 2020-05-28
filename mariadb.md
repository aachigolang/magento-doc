### How to change root password

https://www.ostechnix.com/how-to-reset-mysql-or-mariadb-root-password/


mysql -uroot -proot
mysql -u root -p

create database magentodb;
create user magentouser@'localhost' identified by 'magentopassdb';
grant all privileges on magentodb.* to magentouser@'localhost';
flush privileges;