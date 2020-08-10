# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Instalar o LAMP

```bash
# Atualizar os repositórios
sudo apt update

# Instalar o Apache
sudo apt install apache2

# Configurar a Firewall
sudo ufw allow in "Apache Full"

# Instalar e configurar o MySQL
sudo apt install default-mysql-server
sudo mysql_secure_installation

# Instalar o PHP
sudo apt install php libapache2-mod-php php-mysql

# Setar o index e reiniciar o Apache
sudo vi /etc/apache2/mods-enabled/dir.conf
sudo systemctl restart apache2
```
