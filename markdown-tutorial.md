FORMATAÇÃO MARKDOWN PARA GITHUB
===


## Índice

- [Títulos](#titulos)
- [Parágrafos](#paragrafos)
    - [Indentação](#indent)
- [Formatação de Texto](#format)
    - [Negrito](#b)
    - [Itálico](#i)
    - [Negrito e Itálico](#bi)
    - [Rasurado](#s)
- [Citações](#blockquote)
    - [Citações aninhadas](#quotenested)
- [Listas](#listas)
    - [Listas ordenadas](#ol)
    - [Listas não-ordenadas](#ul)
    - [Subitens](#subitens)
    - [Lista de Tarefas](#tasks)
- [Blocos de Código](#codeblock)
    - [Code](#code)
- [Linhas horizontais](#hline)
- [Imagens](#img)
    - [Imagens com legenda](#img-legenda)
- [Links](#links)
    - [Link com legenda](#links-legenda)
    - [Link por ID](#id-link)
    - [Email e URL](#clickable)
    - [Lista de Referências](#reference)
- [Escape Characters](#escape)
- [Tabelas](#table)
    - [Alinhando itens da tabela](#align-cell)
- [Emojis](#emoji)
- [Notas de Rodapé](#footnotes)


<span id='titulos'/>

## Títulos

Utiliza-se o símbolo `# `:

```
# h1
## h2
### h3
#### h4
##### h5
###### h6
```


<span id='paragrafos'/>

## Parágrafos

Basta separar o texto por uma linha em branco.

* Não deixe espaços em branco antes do texto.

Para pular mais de uma linha é necessário deixar dois espaços em cada linha em branco.


<span id='indent'/>

### Indentação

Utilizar espaços antes do texto pode causar conflitos. Utilizamos `&nbsp;` (equivale a 1 espaço) antes do texto. Para um espaçamento maior, repetimos o comando.

&nbsp;&nbsp;&nbsp;&nbsp;Isso é um parágrafo indentado.


<span id='format'/>

## Formatação de Texto


<span id='b'/>

### Negrito 

Coloque o conteúdo entre `**`:

Texto em \*\***negrito**\*\*


<span id='i'/>

### Itálico

Coloque o conteúdo entre `*`:

Texto em \**itálico*\*


<span id='bi'/>

### Negrito e Itálico

Coloque o conteúdo entre `***`:

Texto em \*\*\****negrito e itálico***\*\*\*


<span id='s'/>

### Rasurado

Coloque entre `~~`:

Texto ~~rasurado~~


<span id='blockquote'/>

## Citações

Utilize `>` seguido de espaço no início do texto:

> `> Citação`


<span id='quotenested'/>

### Citações aninhadas

Utilize mais de um `>` (com apenas um espaço após o último) no início do texto:

>> `>> Citação aninhada`


<span id='listas'/>

## Listas

<span id='ol'/>

### Listas ordenadas

Utilize números seguidos de ponto:

1. `1. Item 1`
2. `2. Item 2`
3. `3. Item 3`


<span id='ul'/>

### Listas não-ordenadas

É possível utilizar `-`, `*` ou `+` no início do texto:

- `- Item`
- `- Item`
- `- Item`


<span id='subitens'/>

#### Subitens

Utilize 4 espaços ou 1 tabulação e insira o markdown da lista ordenada ou não-ordenada:

1. `1. Item 1`
    1. `1. SubItem i`
    2. `2. SubItem ii`
2. `2. Item 2`
    - `- Item`
    - `- Item`


<span id='tasks'/>

### Lista de Tarefas
Utilize `-[ ]` antes do item, e `-[x]` para um item checked:

- [ ] `-[ ] A`
- [ ] `-[ ] B`
- [ ] `-[ ] C`
- [x] `-[x] D`


<span id='codeblock'/>

## Blocos de código

Coloque o conteúdo entre \`\`\`:

```
    ```
     <tag>
        <tag2>
        </tag2>
    </tag>
    ```
```


<span id='code'/>

### Code

Coloque o conteúdo entre ` :

```
`conteúdo`
```


<span id='hline'/>

## Linhas horizontais

Utilize um desses `***`, `---` ou `___`:

___

* Por convenção, deixe linhas em branco em cima e embaixo.


<span id='img'/>

## Imagens

Utilize o modelo abaixo:

`![Alt](/link.png)`

![github-icon](/imagens/github-icon.png)


<span id='img-legenda'/>

### Imagens com legenda

Utilize o modelo abaixo:

`![Alt](/link.png "legenda")`

![github-icon](/imagens/github-icon.png "Ícone do Github")


<span id='links'/>

## Links

Utilize o modelo abaixo:

`[Texto Linkado](/link)`


<span id='links-legenda'/>

### Link com legenda

Utilize o modelo abaixo:

`[Texto Linkado](/link "legenda")`


<span id='id-link'/>

### Link por ID

`[Texto linkado](#custom-id)`

* A ID é inserida com um recurso do HTML: `<span id='custom-id'/>` (sem tag de encerramento).


<span id='clickable'/>

### Email e URL

Para transformar um email ou URL clicável:

`<link>` ou `<exemplo@email.com>`

<exemplo@email.com>

* No caso do email, torna-se equivalente a `<mailto:exemplo@email.com>`. Será encaminhado a alguma plataforma de envio de emails (Outlook, Gmail, etc).


<span id='reference'/>

### Lista de Referências

São duas partes, a primeira é:

`[texto][n]`

Onde `n` é o número que se referencia ao item da lista na segunda parte:

`[n]: link`

[Exemplo][2]

[2]: #reference "Exemplo"


<span id='escape'/>

## Escape Characters

Alguns caracteres são utilizados para comandos. Caso precise utilizá-los literalmente, adicione uma barra invertida antes `(\)`.

Exemplos de alguns caracteres para dar escape:

- \{\}
- \(\)
- \[\]
- \<\>
- \#
- \.
- \+
- \-
- \*
- \_
- \`
- \!
- \|
- \\


<span id='table'/>

## Tabelas

```
Título1 | Título2
--------- | ------
A     | 1
B     | 2
C     | 3
D     | 4
```

Modelo:

Título1 | Título2
--------- | ------
A | 1
B | 2
C | 3
D | 4


<span id='align-cell'/>

### Alinhando itens da tabela

No tracejado horizontal, insira `:` na direção do alinhamento. Para centralizar, basta colocar dos dois lados:

```
Título1 | Título2
:---------: | ------:
A     | 1
B    | 2
C   | 3
D  | 4
```

Título1 | Título2
:---------: | ------:
A   | 1
B    | 2
C   | 3
D    | 4


<span id='emoji'/>

## Emojis

Insira o atalho do emoji entre `:`. Os atalhos podem ser encontrados [aqui](https://www.webfx.com/tools/emoji-cheat-sheet/) :smile:

`:smile:`


<span id='footnotes'/>

## Notas de Rodapé

Similar à lista de links, mas o link aparecerá sobrescrito[^bignote]:

```
palavra[^1]
[^1]: Texto da footnote.
```


[^bignote]: A anotação de rodapé aparece somente no final do documento, mesmo que `[^1]: Nota` seja declarada no meio.