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
