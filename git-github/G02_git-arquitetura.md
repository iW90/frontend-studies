# ARQUITETURA DO GIT

## Objetos: Commits, Trees e Blobs

![Objetos-do-Git](/imagens/objetos.png "Objetos do Git")

### Blobs (Bolhas)

Armazenam os metadados de cada versão de um arquivo, como  o como comprimento da string, tamanho, tipo, conteúdo. Não armazena os nomes dos arquivos, eles são identificados apenas pelo SHA1, que resumidamente é um conjunto único de 40 caracteres encriptados que serve como identificador.

### Trees (Árvores)

Armazena as blobs e alguns metadados. As trees exibem nomes do arquivo e outras trees. É basicamente a estrutura de diretórios, mostrando arquivos e pastas. Se um arquivo for mudado, toda a encriptação da estrutura será alterada na blob, e a tree também será alterada.

![Trees](/imagens/trees.png "Trees")

### Commits

São informações sobre cada versão do arquivo que apontam para a tree, o parente (último commit antes dele), o autor, a mensagem, a data e a hora. Os vários commits formam como se fosse uma timeline do arquivo a cada vez que ele for modificado.

### Estrutura

![Estrutura](/imagens/estrutura.png "Estrutura")