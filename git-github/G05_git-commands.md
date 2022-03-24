# COMMANDOS DO GIT

## Sobre os comandos

* Possuem flags, que são complementos que modificam, acrescentam ou formatam o comando.

* *silence on success*: Se não houve resposta, significa sucesso.

* Setas para cima e para baixo acessam comandos usados anteriormente.

## Comandos

### Arquivos

Sintaxe | O que faz
------------- | --------------
`git init` | Inicia o git na pasta atual
`git clone` | Download de um repositório remoto (ex.: GitHub) - [\[tutorial\]]()
`git remote -v` | mostra os repositórios vinculados ao git local
`git remote add origin SSH` | conecta o git a um repositório remoto - [\[tutorial\]](#novo-repositório)
`git remote remove origin` | para desvincular a SSH ou HTML do diretório local
`git status` | Mostra se sua branch está atualizada em relação ao repositório
`git add .` | Inclui as alterações que serão enviadas no próximo commit
`git reset` | desfaz o último git add
`git commit -m "msg"` | Envia nova versão ao Git
`git commit --amend -m "nova mensagem"` | Renomeia o último commit
`git revert 000000` | desfaz o último commit (substitua 000000 pelo ID do commit)
`git push` | salva as alterações no repositório remoto
`git push --set-upstream origin nome-da-branch` | envia a branch para o github
`git pull` | puxa atualizações do repositório remoto
`git log` | visualiza histórico de commits
`git log -p meus-arquivos` | indica nomes de arquivo ou de um diretório para ver o histórico específico

### Branches

Sintaxe | O que faz
------------- | --------------
`git branch` | mostra a branch atual
`git branch -a` | também lista as branches no repositório remoto
`git checkout -b nome-da-branch` | cria e entra na nova branch
`git checkout nome-da-branch` | entra na branch especificada
`git branch -m novo-nome-da-branch` | renomeia a branch atual
`git branch -d nome-da-branch` | deleta uma branch
`git merge nome-da-branch` | une a branch informada à branch parent
`git merge --abort` | interrompe o merge caso apresente algum erro

## Novo repositório

Comando:

`git remote add origin git@github.com:USER-NAME/REPOSITORY-NAME.git`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ `origin` é apenas um apelido, mas utiliza-se este termo por convenção.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ No lugar de `git@github.com:USER-NAME/REPOSITORY-NAME.git` insira o link SSH do seu repositório.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![SSH](/imagens/novo-repo.png "Link SSH")

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Certifique-se de que a opção SSH esteja selecionada, e não HTML.

## Cópia de repositório

Comando:

`git clone git@github.com:USER-NAME/REPOSITORY-NAME.git`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ No lugar de `git@github.com:USER-NAME/REPOSITORY-NAME.git` insira o link SSH do repositório a ser clonado.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![SSH](/imagens/clone-repo.png "Link SSH")

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Certifique-se de que a opção SSH esteja selecionada, e não HTML.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Digite `yes` caso alguma confirmação seja pedida e sua senha caso seu repositório seja privado.

## Unindo branches locais com merge

Entre na branch parent, neste caso a principal:

`git checkout main`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Em alguns repositórios antigos, a branch principal ainda se chama `master`, portanto utilize o nome correto da branch.

Atualize os arquivos utilizando o comando:

`git pull`

Entre na branch que será unida à principal:

`git checkout outra-branch`

Se necessário, suba os arquivos com:

`git add arquivo.md` e `git commit -m "Adicionando arquivo"`

Volte para a branch principal:

`git checkout main`

Para conferir, utilize o comando `ls` para listar os arquivos e veja se estão todos na branch.

Finalmente una as duas branches com o comando:

`git merge outra-branch`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ (se abrir algo, dê `esc` e digite `:q`, ou feche o arquivo que abrir na sua IDE).