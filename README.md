# Como instalar/configurar/usar o `Hard Disk Sentinel` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para instalar/configurar/usar o `Hard Disk Sentinel` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and configurations for installing/configuring/using `Hard Disk Sentinel` on `Linux Ubuntu`._


## Descrição

### `Hard Disk Sentinel`

O `Hard Disk Sentinel` é uma ferramenta de monitoramento avançada para discos rígidos e unidades de estado sólido (SSDs) no Linux Ubuntu. Ele oferece informações detalhadas sobre a saúde, temperatura, desempenho e integridade geral do disco. Com suporte a S.M.A.R.T. (Self-Monitoring, Analysis and Reporting Technology), ele alerta sobre possíveis falhas iminentes, permitindo ações preventivas para evitar a perda de dados e garantir a confiabilidade dos dispositivos de armazenamento.

## 1. Configurar o `Hard Disk Sentinel` do `Linux Ubuntu` [1]

Para configurar o `Hard Disk Sentinel`, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`


2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

3. Baixe a versão adequada para o seu sistema Linux no website: `https://www.hdsentinel.com/hard_disk_sentinel_linux_gui.php`

4. Mude o diretório para a pasta onde você tem o arquivo baixado (pode não ser necessário se você abriu o terminal a partir dessa pasta)

5. Digite (e pressione `Enter`) para descompactar o arquivo: `tar -xvf hdsentinel_gui64bit.tar.xz`

6. Digite (e pressione `Enter`) para mudar o diretório para o instalador: `cd HDSentinel_GUI`

7. Digite (e pressione `Enter`) para realizar a instalação (em sistemas Ubuntu mais recentes, use apenas `./install.sh` (sem `sudo`).: `sudo ./install.sh`


8. Vamos seguir as instruções passo a passo:

8.1 Descompactar o arquivo `HDSentinel_GUI.zip`: `unzip HDSentinel_GUI.zip -d /home/edenedfsls/HDSentinel_Light/`

8.2 Copiar o ícone para a pasta de ícones: `sudo cp /home/edenedfsls/HDSentinel_Light/HDSentinel_GUI/HDSentinel_GUI.ico /usr/share/icons/`

8.3 Definir o proprietário e permissões para o ícone: `sudo chown edenedfsls:edenedfsls /usr/share/icons/HDSentinel_GUI.ico`

8.4 Definir o proprietário e permissões para o ícone:`sudo chmod 644 /usr/share/icons/HDSentinel_GUI.ico`

8.5 Criar o diretório `usr/share/bin` se não estiver presente: `sudo mkdir -p /usr/share/bin`

8.6 Definir permissões para a pasta: `sudo chmod 755 /usr/share/bin`

8.7 Copiar para a biblioteca bin: `sudo cp /home/edenedfsls/HDSentinel_Light/HDSentinel_GUI/HDSentinel /usr/share/bin/`

8.8 Definir permissão para a aplicação: `sudo chmod 755 /usr/share/bin/HDSentinel`

8.9 Criar diretório para o menu do usuário se não estiver presente: `mkdir -p ~/.local/share/applications`

8.10 Copiar o lançador para o menu do usuário: `cp /home/edenedfsls/HDSentinel_Light/HDSentinel_GUI/Hard_Disk_Sentinel_GUI.desktop ~/.local/share/applications/`

8.11 Definir permissão para o lançador do menu: `chmod 644 ~/.local/share/applications/Hard_Disk_Sentinel_GUI.desktop`

8.12 Copiar o lançador para o `"Desktop"` se presente (não tenho certeza do que é `"Desktop"`, suponho que seja o `desktop` ou algum diretório específico): `cp /home/edenedfsls/HDSentinel_Light/HDSentinel_GUI/Hard_Disk_Sentinel_GUI.desktop ~/Desktop/`

8.13 Remover o diretório temporário de instalação: `rm -rf /home/edenedfsls/HDSentinel_Light/HDSentinel_GUI/`

Lembre-se de substituir `"edenedfsls"` pelo seu nome de usuário real no sistema. E certifique-se de ter backups de seus dados antes de fazer qualquer operação no sistema.

## Referências

[1] OPENAI. ***Instalar kingston linux manager no ubuntu.*** Disponível em: <https://chat.openai.com/c/5747d95e-c490-4e5e-a743-88b4a0bfffee> (texto adaptado). Acessado em: 10/10/2023 23:06.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 16/11/2023 14:25.

