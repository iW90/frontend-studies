# COMANDOS PARA O TERMINAL

Terminologias usadas no prompt de comando (ou terminal) para Git Bash / Linux.
Se você está procurando os comandos específicos do git, veja aqui.

## Sobre os comandos

* Possuem flags, que são complementos que modificam, acrescentam ou formatam o comando.
* *Silence is success*: Se não houver resposta, significa sucesso.
* Prompt e Terminal são sinônimos.


## Lista de atalhos

Atalhos | Funcionalidade
:---------: | ----------------------
`Ctrl + C` | Interrompe um processo no prompt
`Ctrl + L` | Limpa o prompt
`TAB` | Autocompleta palavras
`↑` e `↓` (setas direcionais) | Acessam comandos anteriores

## Lista de comandos

Sintaxe | Funcionalidade
:---------: | ----------------------
`cd` | Volta para a pasta mãe
`cd dir/dir` | Vai para a pasta especificada através do caminho
`pwd` | Mostra o caminho da pasta atual
`mkdir dir` | Cria uma pasta no caminho especificado
`rm file` | Deleta o arquivo ou pasta
`rm -rf dir` | Força a exclusão sem pedir confirmação
`cp file1 file2` | Copia o arquivo1 para o arquivo2
`mv file1 file2` | Renomeia file1 para fil2, ou move o file1 para o file2
`mv file1 dir2` | Move o arquivo1 para a pasta2
`ls` | Lista os arquivos dentro da pasta atual; Se houver * no arquivo, significa que é executável
`ls -a` | Também exibe arquivos ocultos
`echo msg` | Exibe a mensagem na tela
`echo msg > file1.txt` | Insere a mensagem no arquivo. Caso o arquivo ainda não exista, ele será criado
`clear` | Limpa o prompt
`sudo` | Concede permissão de administrador


### Legenda:
* `file` : arquivo
* `dir` : diretório / pasta
    - `dir/dir` : caminho do diretório
    - `..` : pasta anterior
    - `.` : pasta atual