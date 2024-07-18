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

Iniciando o serviço:
sudo /bin/systemctl start nessusd.service

Para configurar abra o navegador e digite:
https://kali:8834

Para iniciar:
/etc/init.d/nessusd start

---------------------------------------------------------

Visual Studio Code
https://code.visualstudio.com/docs/?dv=linux64_deb

---------------------------------------------------------

Dicas Linux
https://edpsblog.wordpress.com/
https://www.explorandoti.com.br/principais-comentos-do-iptables/
https://www.certificacaolinux.com.br/portas-abertas-no-linux/
https://www.digitalocean.com/community/tutorials/how-to-list-and-delete-iptables-firewall-rules-pt

DOCUMENTAÇÃO DEBIAN:
https://www.debian.org/releases/stable/i386/release-notes/ch-about.pt-br.html

---------------------------------------------------------

Repositório:
https://www.kali.org/docs/general-use/kali-linux-sources-list-repositories/
https://www.vivaolinux.com.br/topico/Iniciantes-no-Linux/Repositorio-do-kali
https://linuxdicasesuporte.blogspot.com/2023/06/sourceslist-completa-para-o-debian-12.html
https://tracker.debian.org/pkg/gcc-mingw-w64
https://www.tutorlinux.com.br/2023/06/03/sources-list-completa-debian-12-bookworm/
https://manpages.debian.org/bookworm/apt/sources.list.5.pt.html

---------------------------------------------------------

youtube.com##+js(set, yt.config_.openPopupConfig.supportedPopups.adBlockMessageViewModel, false)
youtube.com##+js(set, Object.prototype.adBlocksFound, 0)
youtube.com##+js(set, ytplayer.config.args.raw_player_response.adPlacements, [])
youtube.com##+js(set, Object.prototype.hasAllowedInstreamAd, true)

---------------------------------------------------------

https://gcore.com/learning/linux-system-monitoring-command-line/
https://www.vivaolinux.com.br/
https://www.vivaolinux.com.br/artigo/Mamae-quero-descompactar-e-tambem-compactar-arquivos-no-terminal/
https://www.google.com/search?client=firefox-b-lm&q=compilar+linux+gcc
https://www.certificacaolinux.com.br/compilar-programas-no-linux-com-o-gcc/
https://embarcados.com.br/linguagem-c-guia-completo/#Introducao-sobre-a-linguagem-C

---------------------------------------------------------

Versoes Java
http://www.itsway.kiev.ua/files/JRE/

---------------------------------------------------------

