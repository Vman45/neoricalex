# COPED - Curso Online para Empreendedores(as) Digitais

Esta documentação é parte integrante do [COPED - Curso Online para Empreendedores Digitais](https://neoricalex.com.br/courses/coped/), e parte do pressuposto de que os requerimentos abaixo já foram instalados:

* WSL (Sub Sistema Windows para Linux)
* Git
* Visual Studio Code
* Vagrant
* Virtual Box

## Aula: Instalar o LAMP

```bash
# Atualizar os repositórios
sudo apt update

# Instalar o Apache
sudo apt install apache2

# Configurar a Firewall
sudo ufw allow in "Apache Full"

# Instalar e configurar o MySQL
sudo apt install mysql-server
sudo mysql_secure_installation

# Instalar o PHP
sudo apt install php libapache2-mod-php php-mysql

# Setar o index e reiniciar o Apache
sudo vi /etc/apache2/mods-enabled/dir.conf
sudo systemctl restart apache2
```
