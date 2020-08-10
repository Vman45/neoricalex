# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Instalar a distribuição do Linux Ubuntu

```powershell
## Baixar a distribuição do Linux Ubuntu
cd coped/software/windows
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-2004 -OutFile Ubuntu.appx -UseBasicParsing

## Extrair e instalar a distribuição
# REF: https://docs.microsoft.com/en-us/windows/wsl/install-on-server
Rename-Item .\Ubuntu.appx .\Ubuntu.zip
Expand-Archive .\Ubuntu.zip .\Ubuntu
cd .\Ubuntu\
.\ubuntu.exe

### Quando solicitado digite:
<Seu nome de usuário>
<Uma senha 2x>

cd ../../../..
```
