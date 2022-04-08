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

cat - lê um arquivo de texto

cat -n - numera as linhas

cat -b - numera as linhas (apenas com conteudo)

cat -s - deixa apenas uma linha em branco

cat -a - mostra caracteres especiais (quebra de linha e etc)


tac - imprime o arquivo de forma inversa


head - mostra o cabeçalho do arquivo (primeiras 10ou 5 linhas)

head -n2 - mostra apenas as duas primeiras linhas

head -c50 - mostra apenas os primeiros bytes

tail - mostra ultimas linhas

tail -n5 mostra 5 ultimas linhas

tail -f mostra ultimas linhas em tempo de execução

less - mostra arquivo de forma paginada

/<string> - acha ocorrencia da string

cat <arquivo_texto> | less - joga saida do cat para o comando less

wc - le numero de linhas, palavras e caracteres do arquivo

wc -l - mostra apenas linhas

wc -w - mostra apenas palavras

wc -c - mostra apenas caracteres

cat <arquivo_texto> | wc -l - mostra apenas a quantidade de linhas, sem o nome do arquivo

nl - numera as linhas de um arquivo sem considerar as linhas em branco

sort - ordenas as linhas(contando linhas em branco)

sort -r - ordena de maneira reversa

sort -k2 - ordena pelo segundo campo

uniq - mostra ocorrencias unicas apenas sequencialmente

sort <arquivo_texto> | uniq - uniq com melhor desempenho

uniq -d - mostra as linhas duplicadas

uniq -c - mostra as linhasrepetidas com o numero de ocorrencias

expand - converte tab pra espaço

unexpand - converste espaço em tab (apenas começo)

unexpand -a - converte qualquer espaço em tab

unexpand -a -t 5 - considera 5 espaços como um tab

od - exibe um formato de texto em formato octal

od -tx - exibe em hexadecimal

join - combina dois arquivos atravez de um indice

paste - combina linha a linha sem ser por indice

split -l20 - divide o arquivo em varios arquivos de 20 linhas

split -l20 <arquivo_entrada> nome_arquivo_saida 

split -b100 - divide o arquivo em varios arquivos de 100 bytes

tr - pegar um conteudo e substituir um caracter (apenas via pipe ou redirecionamento de entrada)

cat <arquivo_texto> | tr a-z A-Z - troca todas as letras minusculas por maiusculas

cat <arquivo_texto> | tr A E - troca todas as letras A maiusculas por E maiusculas

cat <arquivo_texto> | tr ei Ei - troca todos os e e i minusculos por E e I maiusculos

cat <arquivo_texto> | tr [:upper:] [:lower:] - troca todas as petras maiusculas por minusculas


cat <arquivo_texto> | tr  ' ' '_' - troca todos os espaçoes em underline

cat <arquivo_texto> | tr -d A - deletou todas as A maiusculas

cat <arquivo_texto> | tr -d [:upper:] - deletou todas as A maiusculas

fmt - formata uma saida de texto

fm -w 100 - cada linha não ultrapassa de 100 caracteres

pr - preparar arquivo pra impressão

pr -l 50 - a cada 50 linhas uma pagina para impressão

pr -l 50 -h 'Cabeçalho foda' - cabeçalho da pagina

cut - recortar parte de um texto

cut -c1-5 - recorta do caracter 1 ao 5

cut -c1,2,3 - recorta o caracter 1 2 e 5

cut -c-5 - do começo ao caracter 5

cut -c5- - do caracter 5 pra frente

cut -d " " -f1 - extraindo o primeiro campo do arquivo

sed - procurar um conteudo e substituir ou deletar algumas partes do texto

sed 's/Silva/Sousa' <nome_arquivo> - subsititui o arquivo silva por sousa

sed 's/Silva/Sousa/g' <nome_arquivo> - subsititui o arquivo silva por sousa em todas as ocorrencias na linha

sed '3,5 d' <nome_arquivo> - apaga da linah 3 a linha 5

sed '/Claudia/d' - apaga a linha com a string Claudia

- 103.3 Gerenciamento Básico de Arquivos (4)
- 103.4 Fluxo, pipes e Redirecionamentos (4)
- 103.5 Criar, monitorar e encerrar processos (4)
- 103.6 Modificar a prioridade de execução de processos (2)
- 103.7 Pesquisar arquivos de texto com expressões regulares (2)
- 103.8 Edição Basica de Arquivos usando VI (3)
