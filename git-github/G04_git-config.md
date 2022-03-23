# CONFIGURAÇÕES INICIAIS DO GIT

## Conta no Github

Primeiramente é necessário criar uma conta no Github.

## Download

Baixe e instale o Git conforme o sistema operacional que você usa:

[Git](https://git-scm.com/downloads "Git Download")

O próprio site fornece instruções sobre como fazer a instalação.

## Cadastrando username e e-mail

1. No Windows, abra o **Git Bash** (foi instalado junto com o Git), ou abra o **terminal** no Linux.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ **Importante:** Os comandos `Ctrl+C` e `Ctrl+V` não funcionam no terminal. É necessário clicar com o lado direito do mouse e depois em `Copy` (para copiar) ou `Paste` (para colar) quando necessário.

2. No prompt de comando digite:

　`git config --global user.name "Username"`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Não remova as aspas.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ O username (não o nome) deve ser o mesmo utilizado no Github.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Para verificar se foi inserido corretamente, digite: `git config --global user.name`

3. No prompt de comando digite:

　`git config --global user.email "exemplo@exemplo.com"`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Não remova as aspas.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ O email deve ser o mesmo utilizado no Github.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Para verificar se foi inserido corretamente, digite: `git config --global user.email`

## Verificação de SSH

1. Verifiquemos se já há chaves SSH criadas. No prompt de comando digite:

　`ls -al ~/.ssh`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Se você receber um erro que ~/. sh não existe, significa que você não tem um par de chaves SSH.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ A senha possui um desses formatos:
```
id_rsa.pub
id_ecdsa.pub
id_ed25519.pub
```

1.1 Caso não exista, vamos gerar uma. No prompt de comando digite:

　`ssh-keygen -t ed25519 -C "exemplo@exemplo.com"`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Não remova as aspas.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ O email deve ser o mesmo utilizado no Github.


As seguintes linhas serão exibidas: 

```
> Generating public/private algorithm key pair.
> Enter a file in which to save the key (/c/Users/you/.ssh/id_algorithm):
> Enter passphrase (empty for no passphrase):
> Enter same passphrase again:
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Não criaremos uma senha-frase, portanto apenas pressione [enter] três vezes.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Copie, cole em um bloco de notas e salve em um lugar seguro a senha que foi gerada.

## Adicionando chave SSH ao ssh-agent

1. Vamos adicionar a chave ao -agent. No prompt de comando digite:

　`eval "$(ssh-agent -s)"`

```
> Agent pid 1234
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ O número do agent pid varia.

1.1 Adicione sua chave SSH privada ao ssh-agent. No prompt de comando digite:

　`ssh-add ~/.ssh/id_ed25519`