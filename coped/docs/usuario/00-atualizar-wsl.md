# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Atualizar para o WSL 2

```bash
# No Powershell

## Iniciar Powershell como Admin
Start-Process powershell -Verb runAs

## Baixar Atualização WSL
Invoke-WebRequest -Uri https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi -OutFile wsl_update_x64.msi -UseBasicParsing

## Instalar atualização WSL2
wsl_update_x64.msi

## Remover pacote de Atualização
rm wsl_update_x64.msi

## REINICIAR O PC ##

## Verificar versão do WSL
wsl --list --verbose

## Setar Ubuntu como WSL2
wsl --set-version Ubuntu-20.04 2

## Reiniciar o PC ##

## Verificar versão do WSL
wsl --list --verbose
```
