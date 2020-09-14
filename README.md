# NEORICALEX

## Apresentação

O [NEORICALEX](https://neoricalex.com.br) é a minha Plataforma e/ou Ambiente de Trabalho. O local onde eu condenso tudo o que eu sei fazer em TI.

A ideia de criação do NEORICALEX surgiu de uma necessidade minha pessoal quando, em Fevereiro 2020 eu fiquei desempregado com a pandemia do COVID19. Foi preciso encontrar uma forma de pagar as contas ao final do mês, e, decidi de monetizar meu conhecimento trabalhando em meu próprio projeto pessoal.

A minha ideia principal para o projeto é criar um sistema operacional, e basear uma infra-estrutura em cima dele. 

Ou seja, por outras palavras, o NEORICALEX pode ser visto como:

* Uma ferramenta para criar uma Distribuição Linux do Zero baseada no Ubuntu.
* Dentro da Distribuição incluir:
    * Um Cluster LXC/LXD
    * Um Cluster Docker
    * E muito mais...
    
Leia o [README do NFDOS](./nfdos/README.md) para saber qual é o ROADMAP.

## Início Rápido

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
neoricalex/nfdos/desktop/0.3/nfdos.iso
```

Após a imagem ISO ser gerada, use e/ou instale normalmente em qualquer Máquina Virtual (VPS) e/ou Computador Físico (Bare Metal).

## Documentação

A documentação está [acessível aqui](https://neoricalex.readthedocs.io).

## Financiamento

Gostou do projeto, e está afim de ajudar seu desenvolvimento financeiramente?
Ajude via [Paypal](https://www.paypal.me/AleexFL).

Obrigado desde já pelo "café" :-)

## Notas de Lançamento e/ou Atualizações

* **Versão 0.2** - Agora podemos instalar o sistema no disco. Além disso a GUI está completamente zerada, nem mesmo um terminal tem. Apenas tem internet e as configurações do Gnome.
* **Versão 0.1** - Compilação da ISO do Live CD. Dá para usar, mas não dá para instalar no disco para termos persistência, e não precisarmos da imagem ISO.

## Licença

[LICENÇA PÚBLICA GERAL GNU (Versão 2, junho de 1991)](./LICENSE)
