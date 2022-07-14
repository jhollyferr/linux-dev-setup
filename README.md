# linux-dev-setup
linux development environment settings

MYSQL (v8+)
- Remove 
  ```bash
  sudo systemctl stop mysql
  sudo apt-get remove --purge mysql* 
  sudo apt-get remove --purge mysql-server mysql-client mysql-common
  sudo apt-get purge mysql-server mysql-client mysql-common mysql-server-core-* mysql-client-core-*
  sudo rm -rf /etc/mysql /var/lib/mysql
  sudo rm -rf /var/lib/mysql
  sudo rm -rf /etc/mysql
  sudo apt autoremove
  sudo apt autoclean
  sudo -i
  service mysql stop
  killall -KILL mysql mysqld_safe mysqld
  apt-get --yes purge mysql*
  apt-get --yes autoremove --purge
  apt-get autoclean
  deluser --remove-home mysql
  delgroup mysql
  rm -rf /etc/apparmor.d/abstractions/mysql /etc/apparmor.d/cache/usr.sbin.mysqld /etc/mysql /var/lib/mysql /var/log/mysql* /var/log/upstart/mysql.log* /var/run/mysqld ~/.mysql_history
updatedb
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
