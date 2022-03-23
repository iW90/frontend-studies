# CONFIGURAÇÕES INICIAIS DO GIT

Vale lembrar que quando não aparece nenhuma mensagem ao realizar o comando, ele foi executado corretamente.

## Conta no Github

Primeiramente é necessário ter uma conta no Github. Caso ainda não tenha, veja como criar uma [aqui](https://github.com/Dindinha/frontend-studies/blob/main/git-github/G03_github-account.md "Github Account").

## Download

Baixe e instale o Git conforme o sistema operacional que você usa:

[Download Git](https://git-scm.com/downloads "Git Download")

O próprio site fornece instruções sobre como fazer a instalação quando clicar no seu sistema operacional (Windows, Linux ou Mac).

## Cadastrando username e e-mail

1. No Windows, abra o **Git Bash** (foi instalado junto com o Git), ou abra o **terminal** no Linux.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ **Importante:** Os comandos `Ctrl+C` e `Ctrl+V` não funcionam no prompt (terminal). É necessário clicar com o lado direito do mouse e depois em `Copy` (para copiar) ou `Paste` (para colar) quando necessário.

2. No prompt de comando digite:

`git config --global user.name "Username"`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Substitua `Username` pelo username utilizado no seu Github.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Não remova as aspas.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Para verificar se foi inserido corretamente, digite: `git config --global user.name`

3. No prompt de comando digite:

`git config --global user.email "exemplo@exemplo.com"`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Substitua `exemplo@exemplo.com` pelo mesmo email que é utilizado no seu Github.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Não remova as aspas.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Para verificar se foi inserido corretamente, digite: `git config --global user.email`

## Verificação de SSH

1. Verifiquemos se já há chaves SSH criadas. No prompt de comando digite:

`ls -al ~/.ssh`

A senha possui um desses formatos:

```
id_rsa.pub
id_ecdsa.pub
id_ed25519.pub
```

Caso você apareça um erro dizendo que o `~/. sh` não existe, significa que você ainda não tem um par de chaves SSH.

1.1 Se não houver chaves SSH, vamos gerar uma. No prompt de comando digite:

`ssh-keygen -t ed25519 -C "exemplo@exemplo.com"`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Substitua `exemplo@exemplo.com` pelo mesmo email que é utilizado no Github.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Não remova as aspas.

As seguintes linhas serão exibidas: 

```
> Generating public/private algorithm key pair.
> Enter a file in which to save the key (/c/Users/you/.ssh/id_algorithm):
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Pressione `Enter`.

Em seguida será pedido para criar uma senha-frase. Como não criaremos uma (por praticidade), apenas pressione `Enter` e depois `Enter` novamente:

```
> Enter passphrase (empty for no passphrase):
> Enter same passphrase again:
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Copie, cole em um bloco de notas e salve em um lugar seguro o conteúdo que foi gerado.

## Adicionando chave SSH ao ssh-agent

1. Vamos vincular a chave SSH ao ssh-agent. No prompt de comando digite:

`eval "$(ssh-agent -s)"`

Aparecerá a seguinte linha:

```
> Agent pid 1234
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ O número do agent pid varia.

2. Adicione sua chave SSH privada ao ssh-agent. No prompt de comando digite:

`ssh-add ~/.ssh/id_ed25519`

## Adicionando a chave SSH ao Github

1. Copiaremos a chave pública SSH para a sua área de transferência. No prompt de comando digite:

`clip < ~/.ssh/id_ed25519.pub`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Este comando copia o código para a área de transferência, estando agora disponível no seu `Ctrl+V`.

2. Abra o GitHub no seu navegador.

3. No canto superior direito, clique sobre a miniatura da sua foto e depois em *settings*.

4. Na tela que foi aberta, no menu ao lado esquerdo, clique em **SSH and GPG keys**.

5. Clique em **New SSH key** (Nova chave SSH).

6. No campo **"Title"** (Título), adicione uma etiqueta descritiva para a nova chave ("Notebook Pessoal", "PC do Trabalho", ou algo que identifique a máquina que está usando).

7. Cole sua chave no campo **"Key"** (Chave). Se o passo 1 foi feito corretamente, basta utilizar o `Ctrl+V`.

8. Clique em **Add SSH key** (Adicionar chave SSH).

9. Se solicitado, confirme sua senha do GitHub.

____

Prontinho, seu Git e Github estão devidamente configurados e prontos para serem usados.