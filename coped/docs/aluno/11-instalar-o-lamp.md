# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Instalar o LAMP

```bash
# Atualizar os repositórios do Ubuntu
sudo apt update

# Atualizar o neoricalex
git pull

# Instalar o Apache
sudo apt install apache2 -y

# Reiniciar para testar o Apache
sudo service apache2 restart

# Configurar a Firewall
sudo ufw allow in "Apache Full"

# Instalar o MySQL
sudo apt install default-mysql-server -y

# Iniciar o MySQL
sudo /etc/init.d/mysql start

# Configurar respondendo com as respostas abaixo:
sudo mysql_secure_installation
# N
# Digitar a senha 2x
# Y
# Y
# Y
# Y

# Instalar o PHP
sudo apt install php libapache2-mod-php php-mysql -y

# Setar o index e reiniciar o Apache
sudo vi /etc/apache2/mods-enabled/dir.conf

sudo service apache2 restart
```
