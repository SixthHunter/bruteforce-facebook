0# Ajuda!

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
...
http://dl-p30on.persiangig.com/Program/Download/
http://www.oldversion.com/windows/download/winamp-5-551-full

---------------------------------------------------------

Servidor.c

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <arpa/inet.h>

#define PORT 8080
#define BUFFER_SIZE 1024

void copiarArquivo(char *origem, char *destino) {
    FILE *src = fopen(origem, "rb");
    FILE *dst = fopen(destino, "wb");
    char buffer[BUFFER_SIZE];
    size_t bytes;

    if (src == NULL || dst == NULL) {
        perror("Erro ao abrir arquivo");
        return;
    }

    while ((bytes = fread(buffer, 1, BUFFER_SIZE, src)) > 0) {
        fwrite(buffer, 1, bytes, dst);
    }

    fclose(src);
    fclose(dst);
}

void atualizarArquivo(char *arquivo, char *conteudo) {
    FILE *file = fopen(arquivo, "a");
    if (file == NULL) {
        perror("Erro ao abrir arquivo");
        return;
    }
    fprintf(file, "%s", conteudo);
    fclose(file);
}

void excluirArquivo(char *arquivo) {
    if (remove(arquivo) == 0) {
        printf("Arquivo excluído com sucesso\n");
    } else {
        perror("Erro ao excluir arquivo");
    }
}

int main() {
    int server_fd, new_socket;
    struct sockaddr_in address;
    int addrlen = sizeof(address);
    char buffer[BUFFER_SIZE] = {0};

    if ((server_fd = socket(AF_INET, SOCK_STREAM, 0)) == 0) {
        perror("Falha ao criar socket");
        exit(EXIT_FAILURE);
    }

    address.sin_family = AF_INET;
    address.sin_addr.s_addr = INADDR_ANY;
    address.sin_port = htons(PORT);

    if (bind(server_fd, (struct sockaddr *)&address, sizeof(address)) < 0) {
        perror("Falha ao fazer bind");
        close(server_fd);
        exit(EXIT_FAILURE);
    }

    if (listen(server_fd, 3) < 0) {
        perror("Falha ao ouvir");
        close(server_fd);
        exit(EXIT_FAILURE);
    }

    printf("Servidor aguardando conexões...\n");

    if ((new_socket = accept(server_fd, (struct sockaddr *)&address, (socklen_t*)&addrlen)) < 0) {
        perror("Falha ao aceitar conexão");
        close(server_fd);
        exit(EXIT_FAILURE);
    }

    read(new_socket, buffer, BUFFER_SIZE);
    printf("Comando recebido: %s\n", buffer);

    // Aqui você pode adicionar lógica para interpretar o comando e chamar as funções apropriadas

    close(new_socket);
    close(server_fd);
    return 0;
}

Client.c

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <arpa/inet.h>

#define PORT 8080
#define BUFFER_SIZE 1024

int main() {
    int sock = 0;
    struct sockaddr_in serv_addr;
    char buffer[BUFFER_SIZE] = {0};

    if ((sock = socket(AF_INET, SOCK_STREAM, 0)) < 0) {
        perror("Falha ao criar socket");
        exit(EXIT_FAILURE);
    }

    serv_addr.sin_family = AF_INET;
    serv_addr.sin_port = htons(PORT);

    if (inet_pton(AF_INET, "127.0.0.1", &serv_addr.sin_addr) <= 0) {
        perror("Endereço inválido");
        close(sock);
        exit(EXIT_FAILURE);
    }

    if (connect(sock, (struct sockaddr *)&serv_addr, sizeof(serv_addr)) < 0) {
        perror("Falha ao conectar");
        close(sock);
        exit(EXIT_FAILURE);
    }

    // Exemplo de comando para copiar um arquivo
    char *comando = "copiar arquivo_origem.txt arquivo_destino.txt";
    send(sock, comando, strlen(comando), 0);
    printf("Comando enviado: %s\n", comando);

    close(sock);
    return 0;
}

---------------------------------------------------------

# Powershell 1

Claro! Aqui está um exemplo de uma rotina em PowerShell para baixar arquivos de uma URL:

## Define a URL de origem e o caminho de destino
$url = "http://exemplo.com/arquivo.zip"
$destino = "C:\caminho\para\destino\arquivo.zip"

## Baixa o arquivo usando Invoke-WebRequest
Invoke-WebRequest -Uri $url -OutFile $destino

## Exibe uma mensagem de confirmação
Write-Host "Download concluído: $destino"

---------------------------------------------------------

# Powershell 2

Aqui está um exemplo de um script em PowerShell que baixa arquivos de uma URL e os salva em uma pasta específica na inicialização do Windows:

### Script PowerShell

```powershell
# Define a URL de origem e o caminho de destino
$url = "http://exemplo.com/arquivo.zip"
$destino = "C:\caminho\para\destino\arquivo.zip"

# Função para baixar o arquivo
function Baixar-Arquivo {
    param (
        [string]$url,
        [string]$destino
    )
    Invoke-WebRequest -Uri $url -OutFile $destino
    Write-Host "Download concluído: $destino"
}

# Chama a função para baixar o arquivo
Baixar-Arquivo -url $url -destino $destino
```

### Agendando o Script para Inicialização

Para garantir que o script seja executado na inicialização do Windows, você pode usar o Agendador de Tarefas:

1. **Abra o Agendador de Tarefas**:
   - Pressione `Win + R`, digite `taskschd.msc` e pressione `Enter`.

2. **Crie uma nova tarefa**:
   - No painel direito, clique em "Criar Tarefa".

3. **Configurações Gerais**:
   - Dê um nome à tarefa, como "Baixar Arquivos na Inicialização".
   - Marque a opção "Executar com privilégios mais altos".

4. **Configurações de Disparo**:
   - Vá para a aba "Disparadores" e clique em "Novo".
   - Selecione "Ao iniciar" como o disparador.

5. **Configurações de Ação**:
   - Vá para a aba "Ações" e clique em "Novo".
   - Selecione "Iniciar um programa".
   - No campo "Programa/script", digite `powershell.exe`.
   - No campo "Adicionar argumentos (opcional)", digite `-File "C:\caminho\para\seu_script.ps1"` (substitua pelo caminho real do seu script).

6. **Salve a tarefa**:
   - Clique em "OK" para salvar a tarefa.

Agora, toda vez que o Windows iniciar, o script será executado e o arquivo será baixado para a pasta especificada.

Se precisar de mais alguma coisa ou tiver dúvidas, estou aqui para ajudar!

Fonte: conversa com o Copilot, 08/08/2024
(1) How to Download a File with PowerShell — LazyAdmin. https://lazyadmin.nl/powershell/download-file-powershell/.
(2) Use PowerShell to download a file with HTTP, HTTPS, and FTP. https://4sysops.com/archives/use-powershell-to-download-a-file-with-http-https-and-ftp/.
(3) Windows: PowerShell - Download File From URL - ShellHacks. https://www.shellhacks.com/windows-powershell-download-file-from-url/.
(4) How to Download File from URL in PowerShell?. https://powershellfaqs.com/download-file-from-url-in-powershell/.
(5) PowerShell Wget: Download Files with Ease - ATA Learning. https://adamtheautomator.com/powershell-download-file/.
(6) undefined. http://speed.transip.nl/10mb.bin.
(7) undefined. https://www.contoso.com/file.
(8) undefined. http://www.contoso.com.

---------------------------------------------------------
