FORMATAÇÃO MARKDOWN
===

## Índice

1. [Títulos]{#titulo}
2. [Parágrafos]{#2}
    1. [Indentação]{#2-1}

## Títulos {#titulo}

Utiliza-se o símbolo #:

```
# h1
## h2
### h3
#### h4
##### h5
###### h6
```

* Por convenção e para evitar conflitos, é necessário ter um espaço entre o símbolo # e o texto.


## Parágrafos {#2}

Basta separar o texto por uma linha em branco.

* Não deixe espaços em branco antes do texto.


### Indentação {#2-1}

Utilizar espaços antes do texto pode causar conflitos. Caso seu visualizador aceite HTML, utilizamos `&nbsp;` algumas vezes antes do texto. Caso contrário, não será possível.
&nbsp;&nbsp;&nbsp;&nbsp;Isso é um parágrafo indentado.


## Negrito e Itálico

### Negrito 

Coloque o conteúdo entre \*\*:

Texto em \*\***negrito**\*\*


### Itálico

Coloque o conteúdo entre \*:

Texto em \**itálico*\*


### Ambos

Coloque o conteúdo entre \*\*\*:

Texto em \*\*\****negrito e itálico***\*\*\*


## Blockquotes

Utilize `>` seguido de espaço no início do texto:

> `> Citação`


### Blockquotes aninhados

Utilize mais de um `>` (com apenas um espaço após o último) no início do texto:

>> `>> Citação aninhada`


## Listas

### Listas ordenadas

Utilize números seguidos de ponto:

1. `1. Item 1`
2. `2. Item 2`
3. `3. Item 3`


### Listas não-ordenadas

É possível utilizar `-`, `*` ou `+` no início do texto:

- `- Item`
- `- Item`
- `- Item`


### Subitens

Utilize 4 espaços ou 1 tabulação e insira o markdown da lista ordenada ou não-ordenada:

1. `1. Item 1`
    1. `1. SubItem i`
    2. `2. SubItem ii`
2. `2. Item 2`
    - `- Item`
    - `- Item`


### Listas de Definição
Utilize `:` antes da definição do termo:

Primeiro Termo

: `: Definição do termo`


## Code blocks

Coloque o conteúdo entre \`\`\`:

```
    ```
     <tag>
        <tag2>
        </tag2>
    </tag>
    ```
```


### Code

Coloque o conteúdo entre `:

` ``conteúdo`` `


## Linhas horizontais

Utilize um desses `***`, `---` ou `___`:

* Por convenção, deixe linhas em branco em cima e embaixo.


## Imagens

Utilize o modelo abaixo:

`![Alt](/link.png)`


### Imagens com legenda

Utilize o modelo abaixo:

`![Alt](/link.png "legenda")`


## Links

Utilize o modelo abaixo:

`[Texto Linkado](/link)`


### Link com legenda

Utilize o modelo abaixo:

`[Texto Linkado](/link "legenda")`


### Email e URL

Para transformar um email ou URL clicável:

`<link>` ou `<email@email.com>`


### Lista de links

São duas partes, a primeira é:

`[texto][n]`

`[texto][2]`

Onde `n` é o número que se referencia ao item da lista na segunda parte:

`[n]: link`

`[2]: link2 "título"`


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


## Footnotes

Similar à lista de links, mas o link aparecerá sobrescrito¹:

```
palavra[^1]
[^1]: Texto da footnote.
```

palavra[^bignote]
[^bignote]: Texto da bignote.


## IDs nos Títulos

`### Título {#custom-id}`


### Link por ID

`[Texto linkado](#custom-id)`