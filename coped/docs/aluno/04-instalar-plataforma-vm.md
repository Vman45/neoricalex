# COPED - Curso Online para Empreendedores(as) Digitais

## Aula: Instalar a Plataforma de Máquina Virtual

```powershell
# No Powershell

## Iniciar Powershell como Admin
Start-Process powershell -Verb runAs

## Habilitar o componente "Plataforma de máquina virtual"
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

## Habilitar o componente "Subsistema Windows para Linux"
# REF: https://docs.microsoft.com/pt-br/windows/wsl/install-win10
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

### REINICIAR O COMPUTADOR ###
```

