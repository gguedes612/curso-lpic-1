# LPIC-1 Exam 101

## Topico 101: Arquitetura do sistema

### Topico 101.1 - Determinar e definir as configurações de hardware (2)

Descrição: Os candidatos devem ser capazes de determinar e configurar o hardware fundamental do sistema

Principais áreas de conhecimento:
- Habilite e desabilite periféricos integrados.
- Diferencie os vários tipos de dispositivos de armazenamento em massa.
- Determinar recursos de hardware para dispositivos.
- Ferramentas e utilitários para listar várias informações de hardware (por exemplo, lsusb, lspci, etc.).
- Ferramentas e utilitários para manipular dispositivos USB.
- Compreensão conceitual de sysfs, udev e dbus.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- /sys/
- /proc/
- /dev/
- modprobe
- lsmod
- lspci
- lsusb

### Subtopico 101.2 - Inicialize o sistema (3)

Descrição: Os candidatos devem ser capazes de orientar o sistema durante o processo de inicialização.

Principais áreas de conhecimento:
- Forneça comandos comuns para o carregador de inicialização e opções para o kernel no momento da inicialização.
- Demonstrar conhecimento da sequência de inicialização do BIOS/UEFI até a conclusão da inicialização.
- Compreensão de SysVinit e systemd.
- Conscientização do Upstart.
- Verifique os eventos de inicialização nos arquivos de log.


A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- dmesg
- journalctl
- BIOS
- UEFI
- bootloader
- kernel
- initramfs
- init
- SysVinit
- systemd

### Subtopico: 101.3 - Altere os níveis de execução / alvos de inicialização e desligue ou reinicie o sistema (3)

Descrição: Os candidatos devem ser capazes de gerenciar o nível de execução do SysVinit ou o destino de inicialização do sistema do sistema. Este objetivo inclui a mudança para o modo de usuário único, desligamento ou reinicialização do sistema. Os candidatos devem ser capazes de alertar os usuários antes de alternar entre níveis de execução/destinos de inicialização e encerrar os processos adequadamente. Esse objetivo também inclui definir o nível de execução padrão do SysVinit ou o destino de inicialização do systemd. Também inclui o reconhecimento do Upstart como uma alternativa ao SysVinit ou ao systemd.

Principais áreas de conhecimento:

- Defina o nível de execução padrão ou destino de inicialização.
- Altere entre níveis de execução/destinos de inicialização, incluindo o modo de usuário único.
- Desligue e reinicie a partir da linha de comando.
- Alerte os usuários antes de alternar entre níveis de execução/destinos de inicialização ou outros eventos importantes do sistema.
- Encerre os processos corretamente.
- Conscientização do ácido.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- /etc/inittab
- shutdown
- init
- /etc/init.d/
- telinit
- systemd
- systemctl
- /etc/systemd/
- /usr/lib/systemd/
- wall

## Tópico 102: Instalação do Linux e Gerenciamento de Pacotes

### Subtopico 102.1 - Projetar o layout do disco rígido (2)

Descrição: Os candidatos devem ser capazes de projetar um esquema de particionamento de disco para um sistema Linux.

Principais áreas de conhecimento:

- Aloque sistemas de arquivos e espaço de troca para separar partições ou discos.
- Adapte o design ao uso pretendido do sistema.
- Certifique-se de que a partição /boot esteja em conformidade com os requisitos de arquitetura de hardware para inicialização.
- Conhecimento dos recursos básicos do LVM.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- / (root) filesystem
- /var filesystem
- /home filesystem
- /boot filesystem
- EFI System Partition (ESP)
- swap space
- mount points
- partitions



### Subtopico 102.2 - Instale um gerenciador de inicialização(2)

Descrição: Os candidatos devem ser capazes de selecionar, instalar e configurar um gerenciador de inicialização.

Principais áreas de conhecimento:

- Fornecendo locais de inicialização alternativos e opções de inicialização de backup.
- Instale e configure um carregador de inicialização como o GRUB Legacy.
- Execute alterações de configuração básica para GRUB 2.
- Interaja com o carregador de inicialização.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- menu.lst, grub.cfg and grub.conf
- grub-install
- grub-mkconfig
- MBR
 

### Subtopico 102.3 - Gerenciar bibliotecas compartilhadas(1)

Descrição: Os candidatos devem ser capazes de determinar as bibliotecas compartilhadas das quais os programas executáveis ​​dependem e instalá-las quando necessário.

Principais áreas de conhecimento:

- Identificar bibliotecas compartilhadas.
- Identifique os locais típicos das bibliotecas do sistema.
- Carregar bibliotecas compartilhadas.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- ldd
- ldconfig
- /etc/ld.so.conf
- LD_LIBRARY_PATH

### Subtopico 102.3 - Gerenciar bibliotecas compartilhadas(1)

Descrição: Os candidatos devem ser capazes de determinar as bibliotecas compartilhadas das quais os programas executáveis ​​dependem e instalá-las quando necessário.

Principais áreas de conhecimento:

- Identificar bibliotecas compartilhadas.
- Identifique os locais típicos das bibliotecas do sistema.
- Carregar bibliotecas compartilhadas.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- ldd
- ldconfig
- /etc/ld.so.conf
- LD_LIBRARY_PATH
 

### Subtopico 102.4 - Use o gerenciamento de pacotes Debian(3)

Descrição: Os candidatos devem ser capazes de realizar o gerenciamento de pacotes usando as ferramentas de pacotes Debian.

Principais áreas de conhecimento:

- Instale, atualize e desinstale pacotes binários Debian.
- Encontre pacotes contendo arquivos ou bibliotecas específicos que podem ou não estar instalados.
- Obtenha informações do pacote como versão, conteúdo, dependências, integridade do pacote e status da instalação (se o pacote está instalado ou não).
- Conscientização do apto.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- /etc/apt/sources.list
- dpkg
- dpkg-reconfigure
- apt-get
- apt-cache
 

### Subtopico 102.5 - Use o gerenciamento de pacotes RPM e YUM(3)

Descrição: Os candidatos devem ser capazes de realizar o gerenciamento de pacotes usando RPM, YUM e Zypper.

Principais áreas de conhecimento:

- Instale, reinstale, atualize e remova pacotes usando RPM, YUM e Zypper.
- Obtenha informações sobre pacotes RPM como versão, status, dependências, integridade e assinaturas.
- Determine quais arquivos um pacote fornece, bem como encontre de qual pacote um arquivo específico vem.
- Conscientização do dnf.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- rpm
- rpm2cpio
- /etc/yum.conf
- /etc/yum.repos.d/
- yum
- zypper

## Topic 103: Comandos GNU e Unix 

### Subtopico 103.1 - Trabalhar na linha de comando(4)

Descrição: Os candidatos devem ser capazes de interagir com shells e comandos usando a linha de comando. O objetivo assume o shell Bash.

Principais áreas de conhecimento:

- Use comandos de shell únicos e sequências de comandos de uma linha para executar tarefas básicas na linha de comando.
- Use e modifique o ambiente shell, incluindo definição, referência e exportação de variáveis ​​de ambiente.
- Use e edite o histórico de comandos.
- Invoque comandos dentro e fora do caminho definido.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- bash
- echo
- env
- export
- pwd
- set
- unset
- type
- which
- man
- uname
- history
- .bash_history
- Quoting
 

### Subtopico 103.2 - Processar fluxos de texto usando filtros(2)

Descrição: Os candidatos devem ser capazes de aplicar filtros a fluxos de texto.

Principais áreas de conhecimento:

- Envie arquivos de texto e fluxos de saída por meio de filtros de utilitário de texto para modificar a saída usando comandos UNIX padrão encontrados no pacote GNU textutils.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- bzcat
- cat
- cut
- head
- less
- md5sum
- nl
- od
- paste
- sed
- sha256sum
- sha512sum
- sort
- split
- tail
- tr
- uniq
- wc
- xzcat
- zcat

### Subtopico 103.3 - Execute o gerenciamento básico de arquivos(4)

Descrição: Os candidatos devem ser capazes de usar os comandos básicos do Linux para gerenciar arquivos e diretórios.

Principais áreas de conhecimento:

- Copie, mova e remova arquivos e diretórios individualmente.
- Copie vários arquivos e diretórios recursivamente.
- Remova arquivos e diretórios recursivamente.
- Use especificações curinga simples e avançadas nos comandos.
- Usando find para localizar e agir em arquivos com base no tipo, tamanho ou tempo.
- Uso de tar, cpio e dd.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- cp
- find
- mkdir
- mv
- ls
- rm
- rmdir
- touch
- tar
- cpio
- dd
- file
- gzip
- gunzip
- bzip2
- bunzip2
- xz
- unxz
- file globbing
 

### Subtopico 103.4 - Use streams, pipes e redirecionamentos(4)

Descrição: Os candidatos devem ser capazes de redirecionar fluxos e conectá-los para processar dados textuais com eficiência. As tarefas incluem redirecionar a entrada padrão, a saída padrão e o erro padrão, canalizar a saída de um comando para a entrada de outro comando, usar a saída de um comando como argumentos para outro comando e enviar a saída para stdout e um arquivo.

Principais áreas de conhecimento:

- Redirecionando entrada padrão, saída padrão e erro padrão.
- Encaminhe a saída de um comando para a entrada de outro comando.
- Use a saída de um comando como argumentos para outro comando.
- Envie a saída para stdout e um arquivo.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- tee
- xargs

### Subtopico 103.5 - Criar, monitorar e eliminar processos(4)

Descrição: Os candidatos devem ser capazes de realizar o gerenciamento básico de processos.

Principais áreas de conhecimento:

- Execute trabalhos em primeiro e segundo plano.
- Sinalize um programa para continuar em execução após o logout.
- Monitore os processos ativos.
- Selecione e classifique os processos para exibição.
- Enviar sinais para processos.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- &
- bg
- fg
- jobs
- kill
- nohup
- ps
- top
- free
- uptime
- pgrep
- pkill
- killall
- watch
- screen
- tmux
 

### Subtopico 103.6 - Modificar as prioridades de execução do processo(2)

Descrição: Os candidatos devem ser capazes de gerenciar as prioridades de execução do processo.

Principais áreas de conhecimento:

- Conheça a prioridade padrão de um trabalho que é criado.
- Execute um programa com prioridade mais alta ou mais baixa que o padrão.
- Altere a prioridade de um processo em execução.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- nice
- ps
- renice
- top

### Subtopico 103.7 - Pesquisar arquivos de texto usando expressões regulares(3)

Descrição: Os candidatos devem ser capazes de manipular arquivos e dados de texto usando expressões regulares. Este objetivo inclui a criação de expressões regulares simples contendo vários elementos de notação, bem como a compreensão das diferenças entre expressões regulares básicas e estendidas. Também inclui o uso de ferramentas de expressão regular para realizar pesquisas em um sistema de arquivos ou conteúdo de arquivo.

Principais áreas de conhecimento:

- Crie expressões regulares simples contendo vários elementos de notação.
- Entenda as diferenças entre expressões regulares básicas e estendidas.
- Compreender os conceitos de caracteres especiais, classes de caracteres, quantificadores e âncoras.
- Use ferramentas de expressão regular para realizar pesquisas em um sistema de arquivos ou conteúdo de arquivo.
- Use expressões regulares para excluir, alterar e substituir texto.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- grep
- egrep
- fgrep
- sed
- regex(7)
 

### Subtopico 103.8 - Edição básica de arquivos(3)

Descrição: Os candidatos devem ser capazes de editar arquivos de texto usando vi. Este objetivo inclui navegação vi, modos vi, inserção, edição, exclusão, cópia e localização de texto. Também inclui reconhecimento de outros editores comuns e configuração do editor padrão.

Principais áreas de conhecimento:

- Navegue em um documento usando vi.
- Compreender e usar os modos vi.
- Inserir, editar, excluir, copiar e localizar texto no vi.
- Conhecimento de Emacs, nano e vim.
- Configure o editor padrão.

Termos e Utilitários:

- vi
- /, ?
- h,j,k,l
- i, o, a
- d, p, y, dd, yy
- ZZ, :w!, :q!
- EDITOR

## Tópico 104: Dispositivos, Sistemas de Arquivos Linux, Padrão de Hierarquia do Sistema de Arquivos

### Subtopico 104.1 - Criar partições e sistemas de arquivos(2)

Descrição: Os candidatos devem ser capazes de configurar partições de disco e criar sistemas de arquivos em mídias como discos rígidos. Isso inclui o manuseio de partições de swap.

Principais áreas de conhecimento:

- Gerenciar tabelas de partição MBR e GPT
- Use vários comandos mkfs para criar vários sistemas de arquivos, como:
- ext2/ext3/ext4
- XFS
- VFAT
- exFAT
- Conhecimento básico de recursos do Btrfs, incluindo sistemas de arquivos de vários dispositivos, compactação e subvolumes.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- fdisk
- gdisk
- parted
- mkfs
- mkswap
 

### Subtopico 104.2 - Manter a integridade dos sistemas de arquivos(2)

Descrição: Os candidatos devem ser capazes de manter um sistema de arquivos padrão, bem como os dados extras associados a um sistema de arquivos de journaling.

Principais áreas de conhecimento:

- Verifique a integridade dos sistemas de arquivos.
- Monitore o espaço livre e os inodes.
- Repare problemas simples do sistema de arquivos.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- du
- df
- fsck
- e2fsck
- mke2fs
- tune2fs
- xfs_repair
- xfs_fsr
- xfs_db


### Subtopico 104.3 - Controle de montagem e desmontagem de sistemas de arquivos(3)

Descrição: Os candidatos devem ser capazes de configurar a montagem de um sistema de arquivos.

Principais áreas de conhecimento:

- Monte e desmonte manualmente os sistemas de arquivos.
- Configure a montagem do sistema de arquivos na inicialização.
- Configure sistemas de arquivos removíveis montáveis ​​pelo usuário.
- Uso de rótulos e UUIDs para identificação e montagem de sistemas de arquivos.
- Conhecimento das unidades de montagem do systemd.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- /etc/fstab
- /media/
- mount
- umount
- blkid
- lsblk
 

### Subtopico 104.4 - Removido
 

### Subtopico 104.5 - Gerenciar permissões e propriedade de arquivos(3)

Descrição: Os candidatos devem ser capazes de controlar o acesso a arquivos por meio do uso adequado de permissões e propriedades.

Principais áreas de conhecimento:

- Gerencie permissões de acesso em arquivos regulares e especiais, bem como em diretórios.
- Use modos de acesso como suid, sgid e sticky bit para manter a segurança.
- Saiba como alterar a máscara de criação de arquivos.
- Use o campo de grupo para conceder acesso ao arquivo aos membros do grupo.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- chmod
- umask
- chown
- chgrp

### Subtopico 104.6 - Criar e alterar links físicos e simbólicos(2)

Descrição: Os candidatos devem ser capazes de criar e gerenciar links físicos e simbólicos para um arquivo.

Principais áreas de conhecimento:

- Crie ligações.
- Identifique links físicos e/ou flexíveis.
- Copiar versus vincular arquivos.
- Use links para dar suporte a tarefas de administração do sistema.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- ln
- ls
 

### Subtopico 104.7 - Encontre arquivos do sistema e coloque os arquivos no local correto(2)

Descrição: Os candidatos devem estar completamente familiarizados com o Filesystem Hierarchy Standard (FHS), incluindo locais típicos de arquivos e classificações de diretório.

Principais áreas de conhecimento:

- Entenda os locais corretos dos arquivos sob o FHS.
- Encontre arquivos e comandos em um sistema Linux.
- Conheça a localização e a finalidade de arquivos e diretórios importantes, conforme definido no FHS.

A seguir está uma lista parcial dos arquivos, termos e utilitários usados:

- find
- locate
- updatedb
- whereis
- which
- type
- /etc/updatedb.conf