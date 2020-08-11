# Instalar Requerimentos no Host

<!--
    Preferencias VSCode
    @ext:code-settings-sync :: Shan Khan
    8b4a4c63c8dc7ae1139ae0ee95b32be7
    shift+alt+u sincronizar up
    shift+alt+d sync down
-->

<!--Instalar Virtual Box-->
sudo apt install virtualbox -y

<!--Instalar Vagrant-->
curl -O https://releases.hashicorp.com/vagrant/2.2.6/vagrant_2.2.6_x86_64.deb
sudo apt install ./vagrant_2.2.6_x86_64.deb
rm vagrant_2.2.6_x86_64.deb

<!--Instalar Packer-->
cd diversos/packer
sudo apt install unzip -y
unzip packer_1.6.0_linux_amd64.zip
sudo mv packer /usr/local/bin
sudo chown root:root /usr/local/bin/packer

# Criar Imagem para o VPS

<!--Criar a Box para o Vagrant via Virtual Box-->
sudo passwd root

sudo visudo
neo ALL=(ALL) NOPASSWD: ALL

ssh-keygen -t rsa
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys
rm ~/.ssh/id_rsa.pub

sudo vi /etc/ssh/sshd_config
UseDNS no
sudo systemctl restart sshd

[No Host]
scp -p 22 neo@192.168.0.200:/home/neo/.ssh/id_rsa ~/Desktop/NEORICALEX/coped/vagrant/keys
mv coped/vagrant/keys/id_rsa coped/vagrant/keys/nfdos_id_rsa
ssh -i ~/Desktop/NEORICALEX/coped/vagrant/keys/nfdos_id_rsa neo@192.168.0.200 -p 22
exit

rm ~/.ssh/id_rsa
sudo apt install dkms build-essential linux-headers-$(uname -r) -y
(Inserir o Guest Additions do VirtualBox)
lsmod | grep vboxsf

sudo vi /etc/modules-load.d/vboxsf.conf
vboxsf

sudo reboot
lsmod | grep vboxsf

[No Host]
cd coped/vagrant/box
vagrant package --base VPS --output nfdos.box
vagrant add box --name nfdos nfdos.box
cd ../nfdos
vagrant init nfdos

vagrant cloud publish neoricalex/cloud 1.0.0 virtualbox coped/vagrant/box/nfdos.box -d "A really cool box to download and use" --version-description "A cool version" --release --short-description "Download me!"

vagrant box list
vagrant box repackage NAME PROVIDER VERSION


# Criar VPS Ambiente de Desenvolvimento

<!--Iniciar Vagrant-->
vagrant init neoricalex/cloud
vagrant up
vagrant ssh
vagrant destroy

# Em Desenvolvimento ...

<!--Instalar Plugin LXC-->
sudo apt install vagrant-lxc redir  bridge-utils -y
vagrant plugin install vagrant-lxc

<!--Criar a Box para o Vagrant via Packer-->
cd coped/src
packer build ubuntu.json

<!--Configurar o Host-->
cd vbox.vdi
vagrant package --base ubuntu
vagrant box add package.box --provider lxc