# Ajuda!

Ainda estamos em desenvolvimento.

Habilitar o bluetooth no kali linux:
https://www.youtube.com/watch?v=xnJlzxIxAVo

$ sudo apt install bluez -y && sudo apt install blueman -y && sudo systemctl enable bluetooth.service && sudo systemctl start bluetooth.service

https://www.instructables.com/USB-Pesistence-in-Ventoy/

Montando pendrive:
https://plus.diolinux.com.br/t/tutorial-como-usar-montar-um-pendrive-no-linux-manualmente/24302

Formatando pendrive:
https://diolinux.com.br/tutoriais/como-formatar-pen-drive-no-ubuntu.html

Pendrive persistence:
https://www.youtube.com/watch?v=lmCE2tHt2Xs

---------------------------------------------------------

Configurações essenciais: KALI LINUX e VIRTUALBOX!:
https://www.youtube.com/watch?v=JpqsA1pFVCw&list=PLURDXrCGvhnboKBhuhZQy0nojkRBtJ_SF

---------------------------------------------------------

Compactar e descompactar arquivos:
https://www.vivaolinux.com.br/artigo/Mamae-quero-descompactar-e-tambem-compactar-arquivos-no-terminal/

---------------------------------------------------------

Instalando pacotes .deb:
https://medium.com/@habbema/linux-instala%C3%A7%C3%A3o-de-pacotes-71a35a353282
sudo dpkg -i nome_do_pacote.deb

Se houver dependências não atendidas, você pode usar o comando:
sudo apt-get install -f
para corrigir essas dependências automaticamente.

Outra forma de instalar:
sudo apt install ./nome_do_pacote.deb

---------------------------------------------------------

Configuração irssi:
https://www.vivaolinux.com.br/etc/config-leaf

---------------------------------------------------------

Resolvendo o problema de configuracao do relogio e fuso horario.
Instalar e configurar:
https://ntp.br/guia/linux/

---------------------------------------------------------

Aumentar o tamanho da unidade virtual VBox:
cd C:\Program Files\Oracle\VirtualBox
vboxmanage modifyhd "Unidade:\Caminho\arquivo.vdi" --resize 122880

---------------------------------------------------------

Fonte: 
  https://cursos.alura.com.br/forum/topico-sugestao-resolvido-user-is-not-in-the-sudoers-file-this-incident-will-be-reported-259842
  https://www.vivaolinux.com.br/dica/Como-resetar-a-senha-do-root-no-Debian-e-no-Ubuntu

Dando permissoes:
Abrir o arquivo:
nano /etc/sudoers

Digitar:
nomeusuario  ALL=(ALL) ALL

---------------------------------------------------------

XFCE4:
https://wiki.debian.org/pt_BR/Xfce
https://linuxhint.com/install_xfce_debian/

---------------------------------------------------------

NESSUS
https://www.tenable.com/downloads/nessus?loginAttempted=true
https://www.tenable.com/downloads?loginAttempted=true
sudo dpkg -i arquivo.deb

---------------------------------------------------------

Visual Studio Code
https://code.visualstudio.com/docs/?dv=linux64_deb

---------------------------------------------------------
