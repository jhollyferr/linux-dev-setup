# linux-setup
linux development environment settings

MYSQL (v8+)

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
