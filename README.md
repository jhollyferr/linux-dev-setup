# linux-setup
linux development environment settings

MYSQL (v8+)

- Instalation

  ```bash
  sudo apt-get install mysql-client mysql-server
  ```
  
- Remove a default password root
  
  ```bash
  sudo mmysql
  use mysql
  ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by '';
  ```
