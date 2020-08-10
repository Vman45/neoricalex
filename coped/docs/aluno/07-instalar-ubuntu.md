# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Instalar a distribuição do Linux Ubuntu

```powershell
## Trocar para a pasta software do COPED
cd coped/software/windows

## Baixar a distribuição do Linux Ubuntu
# REF: https://github.com/MicrosoftDocs/WSL/issues/645
Invoke-WebRequest -Uri https://aka.ms/wslubuntu2004 -OutFile Ubuntu.appx -UseBasicParsing

## Extrair e instalar a distribuição
# REF: https://docs.microsoft.com/en-us/windows/wsl/install-on-server
Rename-Item .\Ubuntu.appx .\Ubuntu.zip
Expand-Archive .\Ubuntu.zip .\Ubuntu
cd .\Ubuntu\
.\ubuntu2004.exe

### Quando solicitado digite:
<Seu nome de usuário>
<Uma senha 2x>

## Sair e voltar ao Windows
exit

cd ../../../..
```
