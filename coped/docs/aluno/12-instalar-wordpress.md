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

# Criar a pasta onde vai morar o Wordpress
mkdir -p /var/www/coped.neoricalex.com.br

# Configurar o Host Virtual
cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/coped.neoricalex.com.br.conf
#<Directory /var/www/coped.neoricalex.com.br/>
#    AllowOverride All
#    Order allow,deny
#    Allow from all
#</Directory>

# Habilitar o Rewrite
sudo a2enmod rewrite

# Setar permissões
sudo chown -R www-data:www-data /var/www/coped.neoricalex.com.br
sudo find /var/www/coped.neoricalex.com.br -type d -exec chmod 750 {} \;
sudo find /var/www/coped.neoricalex.com.br -type f -exec chmod 640 {} \;

# Reiniciar o Apache
sudo service apache2 restart
```