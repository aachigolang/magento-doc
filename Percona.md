### installing percona server ubu 18.04

[optional]
sudo apt-get install gnupg2

wget https://repo.percona.com/apt/percona-release_latest.$(lsb_release -sc)_all.deb
sudo dpkg -i percona-release_latest.$(lsb_release -sc)_all.deb
sudo apt-get update
sudo apt-get install percona-server-server-5.7


### Installing PMM2 for monitoring percona
https://www.percona.com/blog/2019/09/19/installing-percona-monitoring-and-management-pmm-2-for-the-first-time/

### Configurations

/var/lib/mysql/		Date files
/etc/mysql/my.cnf   Config files


### Sample Database
wget http://downloads.mysql.com/docs/sakila-db.zip
sudo apt-get install unzip
unzip sakila-db.zip

source /home/vagrant/sakila-db/sakila-schema.sql
source /home/vagrant/sakila-db/sakila-data.sql
