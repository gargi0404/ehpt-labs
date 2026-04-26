⁠ bash
sudo apt update
sudo apt upgrade -y

sudo apt install apache2 mariadb-server php php-mysqli php-gd libapache2-mod-php git unzip -y

sudo systemctl start apache2
sudo systemctl start mysql
sudo systemctl enable apache2
sudo systemctl enable mysql

cd /var/www/html
sudo git clone https://github.com/digininja/DVWA.git
sudo mv DVWA dvwa

sudo chmod -R 755 dvwa
sudo chown -R www-data:www-data dvwa

cd dvwa/config
sudo cp config.inc.php.dist config.inc.php
sudo nano config.inc.php

sudo mysql -u root -p
CREATE DATABASE dvwa;
EXIT;

sudo service apache2 restart
 ⁠

---
