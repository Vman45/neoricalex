# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Instalar o Wordpress

```bash
# Entrar no MySQL
sudo mysql -u root -p

# Criar a base de dados
CREATE DATABASE wordpress DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;

# Criar o usuário
CREATE USER 'usuario_wordpress'@'%' IDENTIFIED BY 'senha_super_secreta';

# Conceder privilégios ao usuário
GRANT ALL ON wordpress.* TO 'usuario_wordpress'@'%';

# "Flushar" a base de dados
FLUSH PRIVILEGES;

# Sair do shell do MySQL
EXIT;

# Instalar extensões PHP
sudo apt update
git pull
sudo apt install php-curl php-gd php-mbstring php-xml php-xmlrpc php-soap php-intl php-zip -y

# Reiniciar o Apache
sudo service apache2 restart

# Instalar o curl
sudo apt install curl -y

# Criar a pasta onde vai morar o Wordpress
cd /var/www/html
sudo rm index.html

# Instalar a CLI do Wordpress
# REF: https://wp-cli.org/
sudo curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
php wp-cli.phar --info
sudo chmod +x wp-cli.phar
sudo mv wp-cli.phar /usr/local/bin/wp
wp --info

# Setar as permissões da pasta
sudo chown -R $USER:$USER /var/www/html/

# Fazer o download do WP
wp core download

# Criar a pasta dos upgrades e htaccess
mkdir -p wp-content/upgrade
touch .htaccess

# abrir aba terminal e ...
curl -s https://api.wordpress.org/secret-key/1.1/salt/

# Configurar o wp-config
# Não esquecer: define('FS_METHOD', 'direct');
cp wp-config-sample.php wp-config.php
vi wp-config.php

# Configurar o Host Virtual
sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/000-default.conf.original
sudo vi /etc/apache2/sites-available/000-default.conf
<Directory /var/www/html/>
   Order allow,deny  
   Allow from all  
   Options Indexes FollowSymLinks MultiViews  
   AllowOverride All  
   Require all granted 
</Directory>

# Habilitar o Rewrite
sudo a2enmod rewrite

# Reiniciar o Apache
sudo service apache2 restart

# Setar permissões
sudo chown -R www-data:www-data /var/www/html
sudo find /var/www/html -type d -exec chmod 750 {} \;
sudo find /var/www/html -type f -exec chmod 640 {} \;

# Reiniciar o Apache e o MySQL
sudo service apache2 restart
sudo service mysql restart
```