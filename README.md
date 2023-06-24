## mobaSH

Realiza consultas rápidas a hashes no seu terminal usando a API do HashMob.

Recursos:
Leia um ou mais hashes como argumento.
mobaSH [hash], mobaSH [hash],[hash]
Leia hashes de um arquivo.
mobaSH /caminho/para/o/arquivo
Leia hashes do STDIN.
cat hashes.txt | mobaSH
Imprima de forma organizada a resposta da API em formato JSON.
Exiba os resultados no formato hash:plain.
Leia a chave da API de uma variável de ambiente.
export HASHMOB_KEY=[chave]


Uso:

ubuntu@void# mobaSH -h

Lê uma lista de hashes e procura por suas contrapartes em texto claro no banco de dados do HashMob.
Se nenhum argumento posicional for fornecido e o programa detectar um pipe, os hashes serão lidos do STDIN.
Uma chave de API válida deve ser fornecida através da variável de ambiente HASHMOB_KEY.

Uso: 

./hashmob [-q] [-n] <entrada de hash> 

(hash único / hashes separados por vírgula / caminho do arquivo)

  -n	Desabilita a formatação em JSON da resposta
  -no-color

  Desabilita a saída colorida no log

  -q	Exibe os resultados como hash:plain em vez da resposta completa da API

Exemplos:

   ./hashmob -q 098f6bcd4621d373cade4e832627b4f6

   cat hashes.txt | ./hashmob -q

   ./hashmob 098f6bcd4621d373cade4e832627b4f6,5f4dcc3b5aa765d61d8327deb882cf99

   ./hashmob -q caminho/para/hashes.txt# MobaSH
