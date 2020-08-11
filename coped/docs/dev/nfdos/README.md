## Início rápido

### Requerimentos

Em qualquer Distribuição GNU/Linux baseada no Debian, como por exemplo o Ubuntu, o único requerimento que precisa ter pré-instalado é o Git: 

```bash
# Instalar o Git
sudo apt install git -y
```

Tudo o resto é auto-gerenciado.

Já no caso em que esteja a desenvolver com uma máquina Windows, é necessário algumas coisas:
```powershell
# No Powershell como Administrador
## Instalar o Subsistema Windows para Linux
# REF: https://docs.microsoft.com/pt-br/windows/wsl/install-win10
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

## Habilitar o componente opcional "Plataforma de máquina virtual"
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

### REINICIAR O COMPUTADOR ###
```

Depois de reíniciar o computador:
```powershell
# No Powershell como Administrador
## Baixar o pacote de atualização do último kernel do Linux para o WSL 2 para computadores x64.
# REF: https://docs.microsoft.com/pt-br/windows/wsl/wsl2-kernel
# TODO: Ver qual é o equivalente wget no pwsh
wget https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

## Instalar o pacote de atualização
.\wsl_update_x64.msi

## Definir o WSL 2 como versão padrão
wsl --set-default-version 2

## Baixar a distribuição do Linux Ubuntu
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1804 -OutFile Ubuntu.appx -UseBasicParsing

## Extrair e instalar a distribuição
# REF: https://docs.microsoft.com/en-us/windows/wsl/install-on-server
Rename-Item .\Ubuntu.appx .\Ubuntu.zip
Expand-Archive .\Ubuntu.zip .\Ubuntu
cd .\Ubuntu\
.\ubuntu.exe

### Quando solicitado digite:
<Seu nome de usuário>
<Uma senha 2x>
```

### Ubuntu Desktop e/ou Aplicativo Windows Ubuntu (Versão >= 18.04.4 LTS)

Agora que todos os requisitos estão reunidos:

```bash
# Clonar o repo e trocar de pasta de trabalho
git clone https://github.com/neoricalex/neoricalex.git
cd neoricalex

# Checkar/instalar requerimentos, configurar, compilar (sem instalar), e executar 
bash shell
```

## Introdução
Como falei na apresentação, eu optei por criar um Sistema Operativo do Zero. 

Dessa forma a imagem ISO estará pronta com tudo o que é necessário para que o [NEORICALEX](https://neoricalex.com.br) funcione, sem que para isso eu tenha de instalar software, atualizar, e/ou fazer lá seja aquilo que fôr. 

Será algo tipo "Plug n Play". Colocar o CD/DVD no Leitor, arrancar o Desktop/Notebook ou o Servidor/VPS pelo Live CD/DVD e pronto. O Sistema está no Ar e pronto a executar aquilo que quisermos que ele execute.

O Sistema que criei é uma Distribuição Linux customizada do Debian/Ubuntu, a que dei o nome de [NFDOS](./nfdos/README.md).

A grande vantagem que pretendo, é trabalhar em "Real Time". Ou seja, tudo o que for feito, será sincronizado em tempo real, ou bem próximo disso. Dessa forma poderá até rebentar uma bomba nuclear que o trabalho estará sempre salvo e sincronizado.

Gostou da ideia?

Para chegarmos lá, existe ainda um caminho a percorrer. Veja abaixo o ROADMAP para maiores infos.

## Roadmap

Os módulos abaixo são meus planos. Não estão necessáriamente em ordem:

* Criar a imagem ISO NFDOS (**Em curso...**)
* Criar uma imagem LXD (**Em curso...**)
* Criar uma imagem Docker (**Em curso...**)
* Criar um container com Wordpress para amostragem de exemplo e/ou Marketing (**Em curso...**)
* Criar um CMS (Falta fazer)
* Criar um LMS (Falta fazer)
* Criar um Blog (Falta Fazer)
* Criar um e-Commerce com Marketplace incluído (Falta fazer)
* Criar um Sistema de Compra e Venda de Ações, Commodities, Forex, Etc (Falta Fazer)
* Criar uma IA/Rede Neural para o Sistema de Compra e Venda de Ações, Commodities, Forex, Etc (Falta Fazer)
* Criar a Documentação (O código já é auto explicativo mas falta fazer)

## Como começar

#TODO

### Finalizado

Os módulos abaixo estão finalizados, ou seja, funcionam como pretendido. Claro que estou melhorando/desenvolvendo, consoante o tempo e as possibilidades permitem.

* N/A

### Ajuda

Toda a ajuda é bem-vinda. Ao longo do código tenho vários markups pessoais. Caso queira ajudar, segue alguns exemplos:

* #TODO - Uma coisa que preciso fazer
* #@TODO - Uma coisa que preciso fazer com mais urgência
* #FIXME - Um detalhe que, ou não sei resolver, ou não tenho tempo para resolver.
* #WORKAROUND - Uma gambiarra
* #SRC - O Artigo (Acadêmico ou não) no qual me estou a basear, para fazer determinada coisa/funcionalidade/sistema 
* #REF - Igual à "#SRC", a diferença é que determinada coisa/funcionalidade/sistema já foi feita, então fica o link para crédito e/ou referência.
