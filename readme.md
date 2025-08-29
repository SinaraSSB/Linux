# Linux  -  Principais comandos 

As letras que aparecem antes do cursor fornecem informações valiosas sobre isso.

lcs@Avell4060-2:~$

Estamos na pasta home, que é o ponto inicial do sistema para o usuário lcs. O nome da pessoa usuária é indicado por lcs antes do arroba. Após o arroba, observamos o Avell4060, que indica o nome do dispositivo que estamos utilizando. O til (~) indica que estamos na home, e o cifrão ($) mostra que estamos prontos para digitar comandos no nível de pessoa usuária, sem privilégios administrativos.

> Em suma:
> 
> Nome da pessoa usuária: Indicado por lcs antes do arroba.
> 
> Nome do dispositivo: Observado como Avell4060 após o arroba.
> 
> Pasta atual: O til (~) indica que estamos na home.
> 
> Nível de acesso: O cifrão ($) mostra que estamos prontos para digitar comandos no nível de pessoa usuária.


* sinara@VM022330[novo-portal-dev]:~$   --- o ~ indica que está na home 
* sinara@VM022330[novo-portal-dev]:/$   --- a /  indica o diretório raiz

---

## 📁 Manipulação de arquivos e diretórios

### Comando	Função
* ls	Lista arquivos e pastas
* ls -a lista não apenas os arquivos visíveis, mas também os arquivos ocultos do sistema,
* cd	Muda de diretório  -- sem especificar diretorio nos leva para home usuario
* cd /  seremos direcionados para a raiz do sistema 
* pwd	Mostra o caminho atual
* clear limpar a tela
* mkdir	Cria uma nova pasta
* rm	Remove arquivos
* rm -r	Remove pastas e conteúdo
* cp	Copia arquivos ou pastas
* mv	Move ou renomeia arquivos
* touch	Cria um arquivo vazio
* cat	Exibe o conteúdo de um arquivo direto no terminal
* vim	Editores de texto no terminal

--- 

## 🔍 Busca e visualização

Comando	Função

* find	Busca arquivos por nome ou tipo
* grep	Busca por texto dentro de arquivos
* less	Visualiza arquivos página por página
* head / tail	Mostra início ou fim de arquivos


# Linux 

## copia do servidor para outro

        scp corrigir_cargo.csv detranpaeapl07.detran.reders:/home/sinara
        
        pwd:  mostra onde está (diretório pasta)
        cp:  cp arquivo /home/sinara
        mv:  move ou renomeia
        
        
        vim (editor linux)  :q  sai sem salvar `
        
--- 

## ⚙️ Sistema e permissões

Comando	Função
chmod	Altera permissões de arquivos
chown	Altera dono de arquivos
df -h	Mostra uso de disco
du -sh	Mostra tamanho de pastas
top ou htop	Monitora processos
ps aux	Lista processos ativos
kill	Encerra processos
sudo	Executa comandos como administrador

sudo su-    para logar-se como admin 
sudo -i     iniciar uma sessão como superusuário.
exit -  sai do modo superuser

## SCP 📦 Sintaxe básica do scp:

Para copiar arquivos de um servidor Linux para outro, o comando mais comum e seguro é o scp (Secure Copy). Ele usa SSH para transferir arquivos entre máquinas.

`scp arquivo.txt usuario@ip_do_destino:/caminho/destino/`

`scp relatorio.md sinara@192.168.1.100:/home/sinara/documentos/`

`scp relatorio.md sinara@detranpaeapl07.detran.reders:/home/sinara/documentos/`

relatorio.md: arquivo local que será copiado
sinara: usuário no servidor de destino
192.168.1.100: IP do servidor de destino
/home/sinara/documentos/: pasta onde o arquivo será salvo

### 🔁 Copiar uma pasta inteira:

Use a opção -r para copiar diretórios:

`scp -r pasta/ sinara@192.168.1.100:/home/sinara/`

___ 

## -  Comandos basicos linux


* pwd (Print Working Directory): Exibe o caminho completo do diretório atual em que você está no terminal.

* ls (List): Lista os arquivos e diretórios no diretório atual. Com a opção -a, exibe também arquivos ocultos.

* cd (Change Directory): Altera o diretório atual para o especificado. Exemplo (cd /projeto muda para o diretório projeto.

* sudo (SuperUser Do): Permite a execução de comandos com privilégios de superusuário (root). Exemplo (sudo ls /root exibe o conteúdo do diretório root com permissões elevadas.

* sudo -i: Inicia uma sessão de shell interativa como usuário root, permitindo executar comandos com permissões administrativas sem precisar prefixar cada comando com sudo.

* sudo su: Abre uma sessão de shell como usuário root, mantendo o ambiente do usuário atual. Semelhante a sudo -i, mas mantém o ambiente do usuário.

* cat (Concatenate): Exibe o conteúdo de arquivos. Pode também ser usado para concatenar e criar arquivos.

* exit: Encerra a sessão atual de shell, seja ela como usuário normal ou root.

* git clone: Cria uma cópia local de um repositório Git remoto. Exemplo: git clone https://github.com/alura-cursos/adopet-frontend-cypress clona o repositório especificado.


* mkdir (Make Directory): Cria novos diretórios.

* touch: Cria um arquivo vazio ou atualiza a data de modificação de um arquivo existente.

* nano ou vim: Editor de texto no terminal, usado para criar e editar arquivos.

* mv (Move): Move ou renomeia arquivos e diretórios.

* cp (Copy): Copia arquivos e diretórios.

* clear: Limpa a tela do terminal, removendo o histórico visível.

* ls -l (List Long): Lista arquivos e diretórios com detalhes, incluindo permissões e proprietários.

* ls -al (List All Long): Combina as opções -a e -l, listando todos os arquivos com detalhes.

* rm               - remove files or directories
* rmdir            - remove empty directories
* rm --help 

# restante omitido…

### 🌐 Rede

Comando	Função

* ping	Testa conexão com um host
* curl	Faz requisições HTTP
* wget	Baixa arquivos da internet
* ip a	Mostra IPs da máquina
* netstat	Mostra conexões de rede

---


## Para saber mais: compreendendo o sistema de arquivos do Linux (FHS)


A estrutura de diretórios da raiz (/) no Ubuntu, distribuição que adotamos em nossa jornada de aprendizado, observa o padrão conhecido como Filesystem Hierarchy Standard (Padrão para Sistema de Arquivos Hierárquico - FHS), que define os principais diretórios e o seu conteúdo em sistemas baseados no Linux.

Vamos descrever sinteticamente os principais diretórios que comumente encontramos na raiz do Ubuntu com suas respectivas finalidades de uso. A raiz do sistema de arquivos é o “ponto de partida”, assim todos os demais diretórios e arquivos ficam localizados abaixo desse diretório.

/bin → armazenamento de arquivos binários essenciais do sistema.

/boot → armazenamento de arquivos necessários para a inicialização do sistema, incluindo o carregador de inicialização (boot loader) e o kernel do Linux.

/dev → armazenamento de arquivos de dispositivo (device files) que representam dispositivos de hardware, como discos rígidos, terminais e outros periféricos.

/etc → armazenamento de arquivos de configuração do sistema.

/home → armazenamento de diretórios pessoais dos usuários.

/lib → armazenamento de bibliotecas compartilhadas essenciais para binários localizados nos diretórios /bin e \sbin.

/media → ponto de montagem para mídias removíveis (drivers USB, por exemplo).

/mnt → ponto de montagem temporária para sistemas de arquivos. Usado para montar temporariamente outros sistemas de arquivos durante a administração do sistema.

/opt → armazenamento de aplicativos opcionais e pacotes de software adicionais que não fazem parte da instalação padrão do sistema.

/proc → sistema de arquivos virtual que armazena informações sobre os processos em execução e o estado do kernel.

/root → diretório pessoal do usuário root (superusuário).

/run → armazenamento de informações voláteis sobre o sistema desde a última inicialização, como PID files e sockets.

/sbin → armazenamento de binários essenciais para a administração do sistema, necessários para o boot e recuperação do sistema.

/srv → armazenamento de dados específicos de serviços fornecidos pelo sistema.

/sys → sistema de arquivos virtual que fornece informações e interfaces para o kernel do Linux.

/tmp → armazenamento de arquivos temporários criados por aplicativos e pelo sistema. Esses arquivos geralmente são excluídos ao reiniciar o sistema.

/usr → armazenamento de dados de usuário mais instalados pelo sistema, incluindo binários adicionais, bibliotecas e arquivos de cabeçalho.

/var → armazenamento de arquivos variáveis, como logs, filas de email e arquivos de spool.

Cada diretório presente na raiz do sistema possui um propósito bem definido, atuando para manter o sistema operacional de modo eficiente. A compreensão detalhada de seu funcionamento e configuração está fora do escopo do nosso curso, mas, caso queira entender mais sobre o tema, recomendamos algumas referências ao final do curso.


## Sabeer qual versão linux


1. Para distribuições baseadas em Debian/Ubuntu: Esse comando mostra informações como o nome da distribuição, versão e codinome.
lsb_release -a

2. Para qualquer distribuição:
cat /etc/os-release
Esse comando exibe detalhes sobre o sistema operacional, como nome, versão e ID.

3. Para saber a versão do kernel:
uname -r

--- 
## Kernel

O kernel é o núcleo do sistema operacional Linux — ele é responsável por fazer a ponte entre o hardware (como processador, memória, disco rígido) e o software (os programas que você usa).

### Em resumo, o kernel:
* Gerencia recursos do sistema, como memória, processos e dispositivos.
* Controla a comunicação entre o hardware e o software.
* Garante segurança e estabilidade do sistema.

> Quando você roda o comando uname -r, 
> 
> ele mostra a versão do kernel que está em uso. Por exemplo:
> 
> `5.15.0-151-generic`