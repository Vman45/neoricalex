# NEORICALEX

Em desenvolvimento ...

# NEORICALEX

## Apresentação

O [NEORICALEX](https://neoricalex.com.br) é a minha Plataforma e/ou Ambiente de Trabalho. O local onde eu condenso tudo o que eu sei fazer em TI.

A ideia de criação do NEORICALEX surgiu de uma necessidade minha pessoal quando, em Fevereiro 2020 eu fiquei desempregado com a pandemia do COVID19. Foi preciso encontrar uma forma de pagar as contas ao final do mês, e, decidi de monetizar meu conhecimento trabalhando em meu próprio projeto pessoal.

A ideia principal é criar um sistema operacional, e basear uma infra-estrutura em cima dele.

## Inicio Rápido

```bash
# Instalar o Git
sudo apt install git -y

# Clonar o NEORICALEX
git clone https://github.com/neoricalex/neoricalex.git

# Entrar na pasta neoricalex/nfdos
cd neoricalex/nfdos

# Criar a imagem ISO do NFDOS DESKTOP
bash shell
```
Aguarde que todo o processo seja finalizado. Ao final do processo uma imagem ISO será gerada em:
```bash
neoricalex/nfdos/desktop/0.1/nfdos.iso
```

Após a imagem ISO ser gerada, instale normalmente em qualquer Máquina Virtual e/ou Computador Físico.

## Ambiente de Desenvolvimento (NFDOS Desktop)

O ambiente de desenvolvimento é o ambiente que você utiliza para construir o projeto. Esse ambiente pertence a você. Pode ser o seu computador, notebook, ou uma máquina virtual que você utilize para desenvolver o projeto.

Nesse computador que é o requesito obrigatório, eu apenas quero precisar:

* Instalar a imagem ISO do Sistema Operativo
* Ligar o Computador e estar pronto a trabalhar no desenvolvimento do Projeto.

No entanto, claro, para que se possa instalar uma imagem ISO em um computador, precisamos ter uma imagem ISO de um sistema operativo.

Aqui neste ponto existem várias opções:

* Você pode comprar uma Licença do Windows, Mac OS etc, ou;
* Pode seguir a via do Open Source, e baixar uma imagem ISO de uma distribuição *nix com Software gratuito.
* Ou, você pode criar seu próprio Sistema Operativo.

Eu optei pela terceira opção. Criar um sistema operativo a que dei o nome de **NFDOS**.

O **NFDOS** é, em uma frase, uma versão customizada da Distribuição Linux/Ubuntu 20.04.

Eu optei por criar uma versão custumizada do Ubuntu, porque meu público-alvo são pessoas que nunca usaram Linux, e/ou, que sentem muita dificuldade para trocarem o Windows pelo Linux.

Eu não quero perder clientes porque é necessário abrir o terminal e digitar "sudo apt install", ao invés do popular "seguinte até morrer" do Windows. Então, é bem mais fácil já fornecer uma distribuição com tudo o que é necessário instalado, e depois o cliente apenas precisa usar.

O NFDOS possui, como o Ubuntu, duas variantes:

* NFDOS Desktop
* NFDOS Server

O NFDOS Desktop será usado para desenvolver o projeto e, o Server, para testar no Ambiente de Homologação, para depois fazer o Deploy no Ambiente de Produção.

## Documentação

A documentação está [acessível aqui](https://neoricalex.readthedocs.io).

## Financiamento

Gostou do projeto, e está afim de ajudar seu desenvolvimento financeiramente?
Ajude via [Paypal](https://www.paypal.me/AleexFL).

Obrigado desde já pelo "café" :-)

## Licença

[LICENÇA PÚBLICA GERAL GNU (Versão 2, junho de 1991)](./LICENSE)



# Py
sudo apt install python3-pip -y
sudo pip3 install virtualenv 
virtualenv env
source env/bin/activate

# MK Docs
pip install mkdocs
mkdocs new .


