- 103.1 Trabalhando na linha de Comando (4)
echo - saida no shell
$SHELL - variavel de ambiente que mostra caminho do shell

O que é um comando??

comando interno - faz parte do bash, esta imbutido dentro do shell
programa externo - programa externo instalado no linux
script - executando um escript

type <comando> - verifica o tipo de comando

$PATH - variavel de ambiente que verifica os diretorios para rodar comandos no dentro do shell

pwd - mostra diretorio atual

cd - mudar diretorio

ls - lista diretorio

./<arquivo> - executa script no diretorio apontado

NOME_VARIAVEL=valor - declaração de variavel shell

echo $NOME_VARIAVEL - mostra variavel criada

export NOME_VARIAVEL - exporta variavel como variavel global

set - lista variaveis no ambiente

env - mostra apenas as variaveis globais e altera valor de variavel apenas durante tempo de execução
env TESTE=Windows 



clear ; date ; ls -> Executa sequencialmente os comandos
clear && date && ls -> Executa o proximo comando se a saída do anterior foi um sucesso
clear || date || ls - > Executa o proximo comando caso a saida do anterior tenha sido uma falha

history -> Historico de comando do usuario

!! -> ultimo comando digitado 

!<numero_comando> -> executa o numero do comando no story

!<string> -> executa o comando que tenha a string digitada

history -c -> apaga o historico de comandos

man <comando> -> Manual do comando 

man -k '<descrição>' -> procura comando que bata a descrição

info <comando> - > Informação do comando

uname - retorna informações do sistema

alias <comando_atalho> = <comando> - cria comando de atalho







- 103.2 Aplicando Filtros a Textos e Arquivos (3)
- 103.3 Gerenciamento Básico de Arquivos (4)
- 103.4 Fluxo, pipes e Redirecionamentos (4)
- 103.5 Criar, monitorar e encerrar processos (4)
- 103.6 Modificar a prioridade de execução de processos (2)
- 103.7 Pesquisar arquivos de texto com expressões regulares (2)
- 103.8 Edição Basica de Arquivos usando VI (3)
