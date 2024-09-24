

## instalo paquetes
  sudo yum update -y
  sudo yum install httpd tree -y
  sudo systemctl start httpd
  sudo systemctl enable httpd
## instalo php
  sudo dnf install -y php php-cli php-mysqlnd php-mbstring php-xml
  sudo dnf install -y php8.1 php8.1-cli php8.1-mysqlnd php8.1-mbstring php8.1-xml --allowerasing
  php -version

## installo base de datos mariadb  
  sudo dnf install -y mariadb105-server
  sudo systemctl start mariadb
  sudo systemctl enable mariadb
## config segura de mysql
  sudo mysql_secure_installation
## prueba de conexion
  mysql -u root -p


  ## crear base de datos 

  create database wp;

## installo wordpress
  cd /var/www/html
  sudo wget https://wordpress.org/latest.tar.gz
  sudo tar -xzf latest.tar.gz
  sudo mv wordpress/* .
  sudo rm -rf wordpress latest.tar.gz
  sudo cp wp-config-sample.php wp-config.php
  sudo vim wp-config.php
  

  cd /etc/httpd/conf

  ## edito config de httpd
  ## ser root
  vim httpd.conf
  cat httpd.conf | grep path
  vim httpd.conf
  ls /var/
  ls /var/www/
  ls /var/www/cgi-bin/
  vim httpd.conf
  systemctl restart httpd