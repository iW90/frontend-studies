FORMATAÇÃO MARKDOWN PARA GITHUB
===


## Índice

- [Títulos](#títulos)
- [Parágrafos](#parágrafos)
    - [Indentação](#indentação)
- [Formatação de Texto](#formatação-de-texto)
    - [Negrito](#negrito)
    - [Itálico](#itálico)
    - [Negrito e Itálico](#negrito-e-itálico)
    - [Rasurado](#rasurado)
- [Citações](#citações)
    - [Citações aninhadas](#citações-aninhadas)
- [Listas](#listas)
    - [Listas ordenadas](#listas-ordenadas)
    - [Listas não-ordenadas](#listas-não-ordenadas)
    - [Subitens](#subitens)
    - [Lista de Tarefas](#lista-de-tarefas)
- [Blocos de Código](#blocos-de-código)
    - [Code](#code)
- [Preformatação](#preformatação)
- [Linhas horizontais](#linhas-horizontais)
- [Imagens](#imagens)
    - [Imagens com legenda](#imagens-com-legenda)
- [Links](#links)
    - [Link com legenda](#link-com-legenda)
    - [Índices](#índices)
    - [Email e URL](#email-e-url)
    - [Imagem com link](#imagem-com-link)
    - [Lista de Referências](#lista-de-referências)
- [Escape Characters](#escape-characters)
- [Tabelas](#tabelas)
    - [Alinhando itens da tabela](#alinhando-itens-da-tabela)
- [Emojis](#emojis)
- [Notas de Rodapé](#notas-de-rodapé)




| Formato        | Sintaxe      | Exemplo |
| :------:|:-----:|:-----:|
| Títulos 	| \# h1<br>\## h2<br>\### h3<br>\#### h4<br>\##### h5<br>\###### h6 	|  <h3>Título h3</h3>	|
| Parágrafos  	| Deixar linha em branco entre as frases	| Linha1<br><br>Linha2  	|
| Negrito  	| \*\*Conteúdo\*\* 	| **Conteúdo** 	|
| Itálico  	| \*Conteúdo\* 	| *Conteúdo* 	|
| Negrito e itálico  	| \*\*\*Conteúdo\*\*\* 	| ***Conteúdo*** 	|
| Rasurado 	| &#126;&#126;Conteúdo&#126;&#126; 	| ~~Conteúdo~~ 	|
| Citações 	| \> Conteúdo 	|  <blockquote>Conteúdo</blockquote> 	|
| Citações aninhadas 	| \>\> Conteúdo 	|  <blockquote><blockquote>Conteúdo</blockquote></blockquote> 	|
| Listas ordenadas  	| 1. item 1<br>2. item 2 	| <ol><li>item 1</li><li>item 2</li></ol>  	|
| Listas não-ordenadas 	| \-item<br>\-item  	| <ul><li>item</li><li>item</li></ul> 	|
| Subitens 	| 1. Item 1<br>1. subitem 1<br>2. subitem 2<br>2. Item 2<br>\-subitem<br>\-subitem  	| <ol><li>item 1<ol><li>subitem i</li><li>subitem ii</li></ol></li><li>item 2 <ul><li>item</li><li>item</li></ul></li></ol> 	|
| Lista de Tarefas 	| \- [ ] A <br> \- [x] B  	| [Veja aqui](#lista-de-tarefas)	|
| Bloco de código 	| \`\`\`Conteúdo\`\`\` 	|  [Veja aqui](#blocos-de-código) 	|
| Código 	| \`Conteúdo\` 	| `Conteúdo` 	|
| Preformatação 	| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Comece cada linha com dois espaços ou mais&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 	| [Veja aqui](#preformatação)  	|
| Linha horizontal 	| \-\-\- ou \_\_\_ ou \=\=\= 	| <hr> 	|
| Imagens 	| \![Alt\](/link.png) 	| ![github-icon](/imagens/github-icon.png) 	|
| Imagens com legenda 	| \![Alt\](/link.png "legenda") 	| ![github-icon](/imagens/github-icon.png "Github Icon") 	|
| Links 	| \[Conteúdo\](/link) 	| [Conteúdo](#links) 	|
| Links com legenda 	| \[Conteúdo\](/link "legenda") 	| [Conteúdo](#link-com-legenda "Conteúdo") 	|
| Índice 	| \[Conteúdo\](\#título) 	| [Conteúdo](#índice) 	|
| Email e URL 	| \<exemplo@email.com\> 	| <exemplo@email.com> 	|
| Imagem com link 	| \[\![Alt\](/link.png)\](/link) 	|  [![github-icon](/imagens/github-icon.png)](#imagem-com-link) 	|
| Lista de referência  	| \[Conteúdo]\[1] <br> \[1]: link 	| [Veja aqui](#lista-de-referências)  	|
| Escape characters  	| Barra invertida antes do símbolo	| [Veja aqui](#escape-characters)  	|
| Tabelas 	| \| Título 1   \|      Título 2      \|  Título 3 \|<br>\|\----------\|\:\----------\:\|----------\:\|<br>\| col 1 lin 1 \| col 2 lin 1 \| col 3 lin 1 \| | [Veja aqui](#tabelas) |
| Emojis  	| \:código-do-emoji\: 	| :smile:  	|
| Notas de rodapé  	| Conteúdo\[^1\]   \[^1\]: Nota 	| [Veja aqui](#notas-de-rodapé)  	|


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


## Parágrafos

Basta separar o texto por uma linha em branco.

* Não deixe espaços em branco antes do texto.

Para pular mais de uma linha é necessário deixar dois espaços em cada linha em branco.


### Indentação

Utilizar espaços antes do texto pode causar conflitos. Utilizamos `&nbsp;` (equivale a 1 espaço) antes do texto. Para um espaçamento maior, repetimos o comando.

&nbsp;&nbsp;&nbsp;&nbsp;Isso é um parágrafo indentado.


## Formatação de Texto


### Negrito 

Coloque o conteúdo entre `**`:

Texto em \*\***negrito**\*\*


### Itálico

Coloque o conteúdo entre `*`:

Texto em \**itálico*\*


### Negrito e Itálico

Coloque o conteúdo entre `***`:

Texto em \*\*\****negrito e itálico***\*\*\*


### Rasurado

Coloque entre `~~`:

Texto &#126;&#126;~~rasurado~~&#126;&#126;


## Citações

Utilize `>` seguido de espaço no início do texto:

> `> Citação`


### Citações aninhadas

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


#### Subitens

Utilize 4 espaços ou 1 tabulação e insira o markdown da lista ordenada ou não-ordenada:

1. `1. Item 1`
    1. `1. SubItem i`
    2. `2. SubItem ii`
2. `2. Item 2`
    - `- Item`
    - `- Item`


### Lista de Tarefas
Utilize `-[ ]` antes do item, e `-[x]` para um item checked:

- [ ] `-[ ] A`
- [ ] `-[ ] B`
- [ ] `-[ ] C`
- [x] `-[x] D`


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


### Code

Coloque o conteúdo entre ` :

```
`conteúdo`
```


## Preformatação

Comece o conteúdo com dois espaços ou mais:

    texto   pre-formatado
     É similar ao bloco de código.
        Interpreta todos os       espaços


## Linhas horizontais

Utilize um desses `***`, `---` ou `___`:

___

* Por convenção, deixe linhas em branco em cima e embaixo.


## Imagens

Utilize o modelo abaixo:

`![Alt](/link.png)`

![github-icon](/imagens/github-icon.png)


### Imagens com legenda

Utilize o modelo abaixo:

`![Alt](/link.png "legenda")`

![github-icon](/imagens/github-icon.png "Ícone do Github")


## Links

Utilize o modelo abaixo:

`[Texto Linkado](/link)`


### Link com legenda

Utilize o modelo abaixo:

`[Texto linkado](/link "legenda")`


### Índices

`[Título linkado](#título)`

* Utilize o nome dos títulos como pontos de referência na página.


### Email e URL

Para transformar um email ou URL clicável:

`<link>` ou `<exemplo@email.com>`

<exemplo@email.com>

* No caso do email, torna-se equivalente a `<mailto:exemplo@email.com>`. Será encaminhado a alguma plataforma de envio de emails (Outlook, Gmail, etc).


### Imagem com link

Utilize o código abaixo

`[![Alt](/link.png)](/link)`

[![github-icon](/imagens/github-icon.png)](#img-link)


### Lista de Referências

São duas partes, a primeira é:

`[texto][n]`

Onde `n` é o número que se referencia ao item da lista na segunda parte:

`[n]: link`

[Exemplo][2]

[2]: #reference "Exemplo"


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


## Emojis

Insira o atalho do emoji entre `:`. Os atalhos podem ser encontrados [aqui](https://www.webfx.com/tools/emoji-cheat-sheet/) :smile:

`:smile:`


## Notas de Rodapé

Similar à lista de links, mas o link aparecerá sobrescrito[^bignote]:

```
palavra[^1]
[^1]: Texto da footnote.
```


[^bignote]: A anotação de rodapé aparece somente no final do documento, mesmo que `[^1]: Nota` seja declarada no meio.