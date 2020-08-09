# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Atualizar para o WSL 2

```powershell
# No Powershell
## Iniciar Powershell como Admin
Start-Process powershell -Verb runAs

## Baixar o pacote de atualização do último kernel do Linux para o WSL 2 para computadores x64.
# REF: https://docs.microsoft.com/pt-br/windows/wsl/wsl2-kernel
Invoke-WebRequest -Uri https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi -OutFile wsl_update_x64.msi -UseBasicParsing

## Instalar o pacote de atualização
.\wsl_update_x64.msi

## Remover o pacote de atualização
rm wsl_update_x64.msi

## Definir o WSL 2 como versão padrão
wsl --set-default-version 2
```
