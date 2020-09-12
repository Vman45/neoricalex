# NEORICALEX

## Apresentação

O [NEORICALEX](https://neoricalex.com.br) é a minha Plataforma e/ou Ambiente de Trabalho. O local onde eu condenso tudo o que eu sei fazer em TI.

A ideia aqui é construir toda uma infra-estrutura de raiz. Ou seja:

* Um ambiente de desenvolvimento
* Um ambiente de homologação
* Um ambiente de produção

### Ambiente de desenvolvimento

O ambiente de desenvolvimento é o ambiente que você utiliza para construir o projeto, esse ambiente pertence a você, pode ser o seu computador, notebook, ou uma máquina virtual que você utilize para desenvolver o projeto.

Você de seu lado poderá usar o sistema e/ou distribuição que você quiser. No entanto todos os automatismos, bibliotecas, pacotes, etc, eu usei como base de trabalho uma Distribuição Linux chamada NFDOS.

# Py
sudo apt install python3-pip -y
sudo pip3 install virtualenv 
virtualenv env
source env/bin/activate

# MK Docs
pip install mkdocs
mkdocs new .

# KVM
egrep -c '(vmx|svm)' /proc/cpuinfo
sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils -y
sudo adduser $USER libvirt
sudo adduser $USER kvm
sudo apt install virt-manager -y

# SystemBack - GUI para criar ISO
sudo apt install systemback -y



### Ambiente de homologação

TODO

### Ambiente de produção

TODO

## Financiamento

Gostou do projeto, e está afim de ajudar seu desenvolvimento financeiramente?
Ajude via [Paypal](https://www.paypal.me/AleexFL).

Obrigado desde já pelo "café" :-)

## Licença

[LICENÇA PÚBLICA GERAL GNU (Versão 2, junho de 1991)](./LICENSE)


