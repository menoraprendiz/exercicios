
- https://leetcode.com/problems/tenth-line/



bash script = sequencia de comandos


comandos do terminal

head = imprime o começo de um arquivo

tail = imprime o fim de um arquivo

| = encadeia comandos (saida de um na entrada de outro)

wc = conta linhas e palavras de um arquino

cut = divide as linhas de um arquivo em colunas (segundo um delimitador -d) e imprime os campos (-f)


Programa para achar a decima linha

```sh
# ARQUIVO=$1
ARQUIVO="file.txt"

# se o arquivo tiver menos que 10 linhas, retorne vazio
NUMERO_DE_LINHAS=$(wc -l $ARQUIVO | cut -d' ' -f1)

if [ "$NUMERO_DE_LINHAS" -lt "10" ];then
  exit
else
  DECIMA_LINHA=`head $ARQUIVO -n10 | tail -n1`;
  echo $DECIMA_LINHA
fi
```
