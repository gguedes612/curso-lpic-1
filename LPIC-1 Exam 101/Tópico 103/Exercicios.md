# 103.1 Trabalhando na Linha de Comando

1. Encontre as seguintes informações sobre a sua instalação Linux:

    O caminho completo do arquivo .bash_history para o seu usuário;
    R: set | grep HIST

    O release do kernel instalado:
    R: lsb_release -a

    Os diretórios incluídos em seu PATH:
    r: echo $PATH

    O hostname da máquina:
    echo $HOSTNAME

    O PID da sua sessão shell atual
    ps aux | grep bash


2. Crie e exporte uma variável chamada "NOME" que contenha o seu nome completo.

    export NOME="Guilherme de Lima Guedes"
    echo NOME

3. Crie um comando que escreva na tela a seguinte frase: "O Nome do Próximo Certificado LPI 1 é: <utilize a variável NOME>"

    echo O Nome do Próximo Certificado LPI 1 é: $NOME

# 103.2 Aplicando Filtros a Textos e Arquivos

4. O arquivo /etc/passwd contém a lista de usuários do Linux, os campos são separados pelo caractere :, o primeiro campo indica o nome do usuário e o terceiro o ID do usuário.

    Escreva um comando que mostre os últimos 15 registros do arquivo, exibindo apenas o nome do usuário e seu ID, e que esteja ordenado pelo ID numérico. Por exemplo:

    usuario1:10

    usuario2:12

    usuario:3:1000

    ```tail -n5 /etc/passwd```


5. Gere um comando, ou sequência deles, que mostre o número de linhas do arquivo /etc/passwd excluindo-se as linhas que contenham a palavra "daemon". O resultado do comando deve ser o número de linhas.

    cat /etc/passwd | sed '/daemon/d' | wc -l

# 103.3 Gerenciamento Básico de Arquivos

6. No home de seu usuário, crie um diretório chamado LPI1, dentro dele crie Aulas, Exercicios e Exemplos.

    mkdir -p LPI1/Aulas LPI1/Exercicios LPI1/Exemplos

7. Copie (não mova) todos os arquivos e diretórios existentes em /etc/network/ para <HOME>/LPI1/Exercicios/Network/. Mantenha as mesmas permissões.

    mkdir -p ~/LPI1/Exercicios/Network/
    cp -r /etc/network/* ~/LPI1/Exercicios/Network/

8. Copie (não mova) todos os arquivos do diretório /etc, cujo norme termine com ".conf" para <HOME>/LPI1/Exercicios/Config/ 

    mkdir -p ~/LPI1/Exercicios/Config/ 
    cp -r /etc/*.conf ~/LPI1/Exercicios/Config/ 

9. Em <HOME>/LPI1/Exercicios, crie um arquivo chamado arquivos-cron.tgz, compactado com o gzip, contendo todos os arquivos e diretórios do /etc que contenham a palavra "cron" no nome.

    
10. Descompacte conteúdo do arquivo arquivos-cron.tgz dentro do diretório <HOME>/LPI1/Exercicios/Descompactar/

11. Encontre todos os arquivos do diretório /var, cujo nome termine com ".gz" e que foram modificados nas últimas 48 horas.

## 103.4 Fluxos, Pipes e Redirecionamentos

12. Gere um comando que crie um arquivo chamado diretorios-config.out, contendo a saída do "ls -l" para todos os diretórios do /var cujo nome contenha a palavra "config". A saída deve ser algo como o visto abaixo:

drwxr-xr-x 2 root    root    4096 Mar 28 11:49 /var/cache/fontconfig 

drwx------ 2 root    root    4096 Abr  7 11:37 /var/cache/ldconfig 

drwxr-xr-x 2 lightdm lightdm 4096 Mar 27 16:41 /var/lib/lightdm/.cache/fontconfig 

drwx------ 4 lightdm lightdm 4096 Mar 27 16:41 /var/lib/lightdm/.config

    ls -l /etc | grep config >> diretorios-config.out

13. Explique as diferenças entre os seguintes redirecionadores de entradas e saídas

> arquivo   : sobrescreve saida
< arquivo   : redireciona entrada
>> arquivo : escreve saida
2> arquivo : apenas pra erro
>arquivo 2>&1   : para erro e para saida normal no mesmo arquivo

14. Escreva um único comando comando que gere a lista de arquivos e diretórios contidos em ~/LPI1/Exercicios/Network, exibindo-os na tela e em um novo arquivo chamado lista-network.out

????

## 103.5 Criar, Monitorar e Encerrar Processos

15. Preencha as informações abaixo com os dados de sua instância Linux:

    Total de Memória RAM utilizada (em MB): 66,1
    Load Average (Média dos Últimos 5 minutos): 0,00
    Quantidade de Processos em Execução: 82
    PID dos 3 processos que estão utilizando mais Memória:825 1 2
    PPID (Parent Process ID) dos 3 processos com maior tempo de Uso de CPU: 

16. Crie um comando, que gere um arquivo chamado ~/LPI1/Exercicios/resultado-top.out, que contenha a saída do comando top, atualizado a cada 10 segundos, sendo executado indefinidamente até que o processo seja morto. O comando deve rodar em background.
    
    top -b -d10 >> ~/LPI1/Exercicios/resultado-top.out &

17. Envie um sinal de SIGKILL para o processo iniciado no exercício 16.

    kill <PID do processo>

## 103.6 Modificar a Prioridade de Execução de Processos

18. Inicie o mesmo comando aplicado no exercício 16, porém com a menor prioridade possível.
    
    nice -0 top -b -d10 >> ~/LPI1/Exercicios/resultado-top.out &

19. Altere o NICE do processo cujo dono é o usuário "syslog" para o valor -10.

    renice -n -10 -u syslog 

# 103.7 Pesquisar arquivos de texto com Expressões Regulares

20. Gere um comando que exiba na tela todas as linhas do arquivo /etc/passwd que terminem com "nologin" 

    cat /etc/passwd | egrep "nologin$"

21. Crie um comando que liste todos os arquivos do diretório /etc/ que contenham a palavra "eth0" em seu conteúdo,  não no nome do arquivo. A pesquisa deve incluir também os subdiretórios. Apenas o nome e caminho do arquivo deve ser exibido.

    grep -r "eth0" /etc/

22. No arquivo /etc/passwd, o primeiro campo indica o nome do usuário, enquanto que o terceiro indica o ID do usuário. Crie um comando que exiba apenas os nomes de usuários que tenham o ID com 3 dígitos.

    egrep "[a-zA-Z]:[0-9][0-9][0-9]:" /etc/passwd