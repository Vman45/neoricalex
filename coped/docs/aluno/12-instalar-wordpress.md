# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Instalar o Wordpress

```bash
# Entrar no MySQL
sudo mysql -u root -p

# Criar a base de dados
CREATE DATABASE wordpress DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;

# Criar o usuário
CREATE USER 'usuario_wordpress'@'localhost' IDENTIFIED BY 'senha_super_secreta';

# Conceder privilégios ao usuário
GRANT ALL ON wordpress.* TO 'usuario_wordpress'@'localhost' IDENTIFIED BY 'senha_super_secreta';

# "Flushar" a base de dados
FLUSH PRIVILEGES;

# Sair do shell do MySQL
EXIT;

# Instalar extensões PHP
sudo apt update
git pull
sudo apt install php-curl php-gd php-mbstring php-xml php-xmlrpc php-soap php-intl php-zip

# Reiniciar o Apache
sudo service apache2 restart

# Instalar o curl
sudo apt install curl -y

# Criar a pasta onde vai morar o Wordpress
sudo mkdir -p /var/www/neoricalex.com.br
sudo chown -R neo:neo /var/www/neoricalex.com.br
cd /var/www/neoricalex.com.br

# Instalar a CLI do Wordpress
# REF: https://wp-cli.org/
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
php wp-cli.phar --info
chmod +x wp-cli.phar
sudo mv wp-cli.phar /usr/local/bin/wp
wp --info

# Fazer o download do WP
wp core download

# Configurar o wp-config
wp core config --prompt

# Instalar via WP CLI
wp core install --prompt

# Entrar no Powershell
powershell.exe

# Iniciar o Powershell como Admin
Start-Process powershell -Verb runAs

# Editar o Hosts para configurar o nosso nome de dominio "Fake"
notepad "drivers/etc/hosts"

# Sair do Powershell e voltar ao bash
exit

# Configurar o Host Virtual
cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/neoricalex.com.br.conf
#<Directory /var/www/neoricalex.com.br/>
#    AllowOverride All
#    Order allow,deny
#    Allow from all
#</Directory>

# Habilitar o Rewrite
sudo a2enmod rewrite

# Setar permissões
sudo chown -R www-data:www-data /var/www/neoricalex.com.br
sudo find /var/www/neoricalex.com.br -type d -exec chmod 750 {} \;
sudo find /var/www/neoricalex.com.br -type f -exec chmod 640 {} \;

# Reiniciar o Apache
sudo service apache2 restart
```