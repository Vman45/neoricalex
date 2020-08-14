# NFDOS
O NFDOS significa Neo Free Disk Opening System, e é um Sistema Operativo criado do zero.

Eu não sei você, mas eu sempre quis saber como se faz um sistema operacional do zero. Mas isso apenas não bastava. Eu também queria saber como se faz um sistema de distribuição completo, onde eu digitava um comando ou dois, e eu tinha uma imagem ISO gerada para poder distribuir o meu sistema, ou usar em qualquer computador.

Mas tudo isso apenas não bastava. Eu também queria ter o contrôle total, assim como saber o que estava a fazer. Os "Hello World's" são bastante bons, mas melhor ainda, é saber o que acontece, e o que faz com que o "Hello World" funcione.

Se você também está buscando por isso, o NFDOS é para você.

## Prefácio
O NFDOS foi pensado para servir de aprendizado, uma vez que o NFDOS está a ser desenvolvido por um Iniciante em Assembly e C. Com toda a certeza que não seria possível do NFDOS ser uma realidade sem a preciosa ajuda de:

* O [Operating System Development Series](http://www.brokenthorn.com/Resources/);
* O [OSDev](https://wiki.osdev.org/Main_Page);
* O [Linux From Scratch](http://www.linuxfromscratch.org/);
* O [Minimal Linux Live (MLL)](https://github.com/ivandavidov/minimal);
* O [Buildroot](https://buildroot.org/);
* E o [MIT xv6 OS](https://pdos.csail.mit.edu/6.828/2019/)

Por outras palavras, o NFDOS não é uma ferramenta para fazer coisas por você. O NFDOS é uma ferramenta do tipo DIY - Do It Yourself - para você aprender a fazer você mesmo. Você lê o código, vê como se faz, e reproduz da forma que você bem quiser e entender.

## Introdução
Como falei no [README do NEORICALEX](https://github.com/neoricalex/neoricalex/blob/master/README.md) eu optei por criar um Sistema Operativo do Zero. 

Dessa forma a imagem ISO estará pronta com tudo o que é necessário para que o [NEORICALEX](https://neoricalex.com.br) funcione, sem que para isso eu tenha de instalar software, atualizar, e/ou fazer lá seja aquilo que fôr. 

Será algo tipo "Plug n Play". Colocar o CD/DVD no Leitor, arrancar o Desktop/Notebook ou o Servidor/VPS pelo Live CD/DVD e pronto. O Sistema está no Ar e pronto a executar aquilo que quisermos que ele execute.

O Sistema que criei é uma Distribuição Linux customizada do Debian/Ubuntu. Começar do completo Zero demanda tempo que eu não tenho. Preciso monetizar para depois sim, ir indo no encontro de um SO do Zero no sentido literal do conceito.

Para já, a grande vantagem que pretendo, é trabalhar em "Real Time". Ou seja, tudo o que for feito, será sincronizado em tempo real, ou bem próximo disso. Dessa forma poderá até rebentar uma bomba nuclear que o trabalho estará sempre salvo e sincronizado.

Gostou da ideia?

Para chegarmos lá, existe ainda um caminho a percorrer. Veja abaixo o ROADMAP para maiores infos.

## Roadmap

Os módulos abaixo são meus planos. Não estão necessáriamente em ordem:

* Criar a imagem ISO NFDOS Cliente (**Em curso...**)
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

O objectivo final é tudo ser feito com apenas um único comando, mas claro ainda não estamos lá.

Para já, estou partindo da premissa de que você já clonou o neoricalex, e já mandou executar o *bash shell*. Caso ainda não tenha feito, agora é o momento:
```bash
# Instalar o git
sudo apt install git -y

# Clonar o neoricalex
git clone https://github.com/neoricalex/neoricalex.git

# Entrar na pasta do NFDOS
cd neoricalex/coped/software/nfdos

# Criar a imagem ISO do NFDOS Server
bash shell
```

#TODO: Explicação com imagens ilustrativas do processo de criação da imagem ISO
<!--
    Lembretes Markdown: https://guides.github.com/features/mastering-markdown/#examples
    ![Imagem](https://github.com/neoricalex/neoricalex/blob/master/coped/docs/dev/img/consola.PNG)
-->


### Finalizado

Os módulos abaixo estão finalizados, ou seja, funcionam como pretendido. Claro que estou melhorando/desenvolvendo, consoante o tempo e as possibilidades permitem.

* Criar a imagem ISO NFDOS Server

### Ajuda

Toda a ajuda é bem-vinda. Ao longo do código tenho vários markups pessoais. Caso queira ajudar, segue alguns exemplos:

* #TODO - Uma coisa que preciso fazer
* #@TODO - Uma coisa que preciso fazer com mais urgência
* #FIXME - Um detalhe que, ou não sei resolver, ou não tenho tempo para resolver.
* #WORKAROUND - Uma gambiarra
* #SRC - O Artigo (Acadêmico ou não) no qual me estou a basear, para fazer determinada coisa/funcionalidade/sistema 
* #REF - Igual à "#SRC", a diferença é que determinada coisa/funcionalidade/sistema já foi feita, então fica o link para crédito e/ou referência.
