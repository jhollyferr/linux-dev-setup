# linux-dev-setup
linux development environment settings

MYSQL (v8+)
- Remove 
  ```bash
  sudo service mysql stop  #or mysqld
  sudo killall -9 mysql
  sudo killall -9 mysqld
  sudo apt-get remove --purge mysql-server mysql-client mysql-common
  sudo apt-get autoremove
  sudo apt-get autoclean
  sudo deluser -f mysql
  sudo rm -rf /var/lib/mysql
  sudo apt-get purge mysql-server-core-5.7
  sudo apt-get purge mysql-client-core-5.7
  sudo rm -rf /var/log/mysql
  sudo rm -rf /etc/mysql
  ```
- Installation

  ```bash
  sudo apt-get install mysql-client mysql-server
  ```
  
- Resetting default root user configuration
  
  ```bash
  sudo mysql
  use mysql
  ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by '';
  ```
