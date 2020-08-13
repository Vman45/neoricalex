# NEORICALEX

## Apresentação

O [NEORICALEX](https://neoricalex.com.br) é a minha Plataforma de Trabalho ou Startup. O local onde eu condenso tudo o que eu sei fazer em TI.

No momento em que a escrever esse texto, o [NEORICALEX](https://neoricalex.com.br) é básicamente uma instalação do Wordpress como milhões de outras espalhadas pela internet, hospedado em um droplet na Digital Ocean.

O que acontece é que, como tantos outros, o Wordpress está super lento. Então urge fazer alguma coisa a respeito.

Eu poderia fazer como todo o mundo e otimizar. No entanto eu quero ir por outra via. Eu quero construir toda uma infraestrutura de raiz. Ou seja:

* Um ambiente de desenvolvimento
* Um ambiente de homologação
* Um ambiente de produção

Dessa forma eu terei a certeza que, se o Wordpress estiver lento, a culpa será maioritáriamente minha, e não da hospedagem, plugins, imagens, servidor web, ou seja lá aquilo que fôr.

No entanto o Wordpress é apenas um exemplo. Você pode usar o que vamos construir aqui para aquilo que você quiser.

Começando pelo inicio, o único requesito necessário é ter um computador. Não precisa ter sistema operativo. No entanto precisa de um Leitor CD/DVD, e/ou outra forma onde se possa arrancar o computador através de uma imagem ISO. 

Essa imagem ISO terá duas variantes:

* Versão Privada - Que será o Servidor
* Versão Pública - Que será o Cliente

Nesse computador que é o requesito obrigatório, e é onde vamos ter o nosso Servidor "Hospedado", eu apenas quero precisar:

* Instalar a ISO do Sistema Operativo
* Executar um comando para estar pronto a trabalhar no seu desenvolvimento.

No entanto, claro, para que se possa instalar uma imagem ISO em um computador, precisamos ter uma imagem ISO de um sistema operativo.

Aqui neste ponto existem várias opções:

* Você pode comprar uma Licença do Windows, Mac OS etc, ou;
* Pode seguir a via do Open Source, e baixar uma imagem ISO de uma distribuição *nix com Software gratuito.
* Ou, você pode criar seu próprio Sistema Operativo.

Eu optei pela terceira opção. Criar um sistema operativo do zero, a que dei o nome de [NFDOS](https://github.com/neoricalex/neoricalex/tree/master/coped/software/nfdos).

Isso acarreta bastantes PROS, mas também tem CONTRAS.

Um dos contras, é que você tem que fazer tudo você mesmo. Se estiver afim de embarcar em uma aventura que poderá demorar vidas, mas em que os PROS compensam, seja muito bem-vindo(a)!

Bom, como você se deve dar conta, criar um sistema operativo do zero, e basear toda uma infraestrutura em cima do sistema operativo, demanda bastante tempo e dedicação.

Uma das coisas que projetos desta envergadura precisam é de apoio financeiro, coisa que eu não tenho. Tudo o que já foi, e vai ser feito, é fruto de meu trabalho e pesquisa ao longo dos anos. Para que o [NEORICALEX](https://neoricalex.com.br/) exista, e para que eu possa continuar a compartilhar meu conhecimento é necessário dinheiro. 

Então a melhor forma de monetizar que encontrei, foi a de produzir um Curso Online a que dei o nome de [COPED](https://github.com/neoricalex/neoricalex/tree/master/coped).

Nele, eu vou ensinar o passo-a-passo de como criar uma infra do completo zero tendo como objetivo final uma instalação Wordpress rápida e segura. Claro que, repetindo o que já comentei, você não precisa de usar a infra para o Wordpress. Pode perfeitamente usar para qualquer aplicativo, framework ou software que você quiser.

Por outras palavras, iremos criar um Ambiente de Desenvolvimento onde iremos desenvolver a versão servidor do [NFDOS](https://github.com/neoricalex/neoricalex/tree/master/coped/software/nfdos), e iremos usar o  [COPED](https://github.com/neoricalex/neoricalex/tree/master/coped) para distribuirmos a versão Cliente da ISO do [NFDOS](https://github.com/neoricalex/neoricalex/tree/master/coped/software/nfdos) que teremos de criar, e que será o nosso Ambiente de Homologação.

Dessa forma eu terei então uma fonte de rendimentos, que me fará, espero, não depender apenas de apoio de terceiros para levar avante toda essa empreitada.

### Ambiente de desenvolvimento

Chegamos então no Ambiente de Desenvolvimento. Aqui é onde vamos criar a ISO da Versão Servidor do [NFDOS](https://github.com/neoricalex/neoricalex/tree/master/coped/software/nfdos).

Claro está que, para criarmos uma ISO precisamos de algumas ferramentas. E, é óbvio, essas ferramentas precisam ser instaladas em um computador pré-existente já com um Sistema Operativo instalado e funcionando.

Você de seu lado poderá usar o sistema e/ou distribuição que você quiser. No entanto todos os automatismos, bibliotecas, pacotes, etc, eu usei como base de trabalho uma Distribuição Linux/Ubuntu.

Acredito que tudo funcionará em qualquer distribuição baseada no Debian, mas enfim, recomendo então que para você começar da melhor maneira, que tenha preparado um computador com uma distribuição Ubuntu com pelo menos a versão 18.04 instalada.

Está pronto(a) para começar?

```bash
# Clonar o neoricalex
git clone https://github.com/neoricalex/neoricalex.git

# Entrar na pasta do NFDOS
cd neoricalex/coped/software/nfdos

# Criar a imagem ISO do NFDOS Server
bash shell
```

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
