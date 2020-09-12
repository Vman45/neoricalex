# NEORICALEX

## Apresentação

O [NEORICALEX](https://neoricalex.com.br) é a minha Plataforma e/ou Ambiente de Trabalho. O local onde eu condenso tudo o que eu sei fazer em TI.

A ideia de criação do NEORICALEX surgiu de uma necessidade minha pessoal quando, em Fevereiro 2020 eu fiquei desempregado com a pandemia do COVID19. Foi preciso encontrar uma forma de pagar as contas ao final do mês, e, decidi de monetizar meu conhecimento trabalhando em meu próprio projeto pessoal.

A ideia principal é criar um sistema operacional, e basear uma infra-estrutura em cima dele.

## Ambiente de Desenvolvimento (NFDOS Desktop)

O ambiente de desenvolvimento é o ambiente que você utiliza para construir o projeto. Esse ambiente pertence a você. Pode ser o seu computador, notebook, ou uma máquina virtual que você utilize para desenvolver o projeto.

Nesse computador que é o requesito obrigatório, e que eu vou usar para desenvolver, eu apenas quero precisar:

* Instalar a ISO do Sistema Operativo
* Executar um comando para estar pronto a trabalhar no seu desenvolvimento.

No entanto, claro, para que se possa instalar uma imagem ISO em um computador, precisamos ter uma imagem ISO de um sistema operativo.

Aqui neste ponto existem várias opções:

* Você pode comprar uma Licença do Windows, Mac OS etc, ou;
* Pode seguir a via do Open Source, e baixar uma imagem ISO de uma distribuição *nix com Software gratuito.
* Ou, você pode criar seu próprio Sistema Operativo.

Eu optei pela terceira opção. Criar um sistema operativo a que dei o nome de NFDOS.

# TODO: Continuar a documentação ...

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
