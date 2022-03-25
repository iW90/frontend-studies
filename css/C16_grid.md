# GRID

```html
<div class="container">
  <div class="d1">1</div>
  <div class="d2">2</div>
  <div class="d3">3</div>
  <div class="d4">4</div>
  <div class="d5">5</div>
</div>
```

```css
  .container {
    display: grid | inline-grid;
  }
```

* grid: block level;

* inline-grid: inline level;

## Colunas e linhas

```css
grid-template-columns: XXpx YYpx;
grid-template-rows: ZZpx WWpx;
```

### Colunas

* Coluna 1 com XXpx de largura.

* Coluna 2 com YYpx de largura.

* A cada novo valor adicionado, uma nova coluna com o tamanho definido. Se a quantidade de linhas não for definida, os itens dentro serão distribuídos nas colunas.

### Linhas

* Linha 1 com ZZpx de largura.

* Linha 2 com WWpx de largura.

* A cada novo valor adicionado, uma nova linha com o tamanho definido.

![Grid](/imagens/grid.png)
­
### Outras unidades de medida além de px e em

* fr: define a coluna ou linha para uma fração do espaço disponível.

* auto: define a coluna ou linha para a largura ou altura de seu conteúdo automaticamente.

* %: ajusta a coluna ou linha para a largura percentual de seu contêiner.

### Nomes

É possível dar nomes para as linhas e colunas:

```css
grid-template-columns: [col1] XXpx [col2] YYpx;
grid-template-rows: [line1] ZZpx [line2] WWpx;
```

## Repeat

```css
.container {
  grid-template-columns: repeat(Y, 20px [nome-da-coluna]);
  grid-template-row: repeat(X, 80px [nome-da-linha]);
}
```

É utilizado o repeat(), sendo Y a quantidade de vezes que a coluna será criada, e X a quantidade de vezes em que a linha será criada.

**Modelo**

* 100 linhas com *height* 50px (colunas definem *width*):

```css
grid-template-rows: repeat(100, 50px);
```

**Modelo 2**

* 5 colunas `1fr, 50px, 1fr, 50px, 20px`:

```css
grid-template-columns: repeat(2, 1fr 50px) 20px;
```

## Nomeando áreas

![Grid names](/imagens/grid-names.png)

```css
.container {
  grid-template-areas: 
    "grid-area-name | . | none | ..."
    "...";
}
```

* **grid-area-name**: nome de uma célula (especificada com grid-area).

* **.** : um ponto significa célula vazia.

* **none**: célula indefinida.

* Repetir um `name` significa que toda aquela área será abrangida.

Modelo:

```css
.item-a {
  grid-area: header;
}
.item-b {
  grid-area: main;
}
.item-c {
  grid-area: sidebar;
}
.item-d {
  grid-area: footer;
}

.container {
  display: grid;
  grid-template-columns: 50px 50px 50px 50px;
  grid-template-rows: auto;
  grid-template-areas: 
    "header header header header"
    "main main . sidebar"
    "footer footer footer footer";
}
```

## Espaçamento

![Grid gap](/imagens/grid-gap.png)

```css
row-gap: XX¹px auto² XX³px; /* espaço horizontal, entre linhas, medidas diferentes */
column-gap: YYpx; /* espaço vertical, entre colunas */
gap: XXpx YYpx; /* shorthand: row | column */
```

Modelo:

```css
column-gap: 10px;
row-gap: 15px;
```

## Alinhamento horizontal

![Grid horizontal](/imagens/grid-h.png)

```css
.container {
  justify-items: start | end | center | stretch;
}
```

## Alinhamento vertical

![Grid vertical](/imagens/grid-v.png)

```css
.container {
  align-items: start | end | center | stretch;
}
```

## Alinhamento individual

```css
.grid-item {
  align-self: start | end | center | stretch;
}
```

* Feito na célula específica, não no container.
­
### Alinhamento horizontal e vertical

```css
.container {
  place-items: start | end | center | stretch;
}
```

## Linhas

![Grid linhas](/imagens/grid-lines.png)

As linhas verticais são chamadas de "column lines" e as linhas horizontais são "row lines", e elas são numeradas para que possam ser identificadas.
Um grid de `5 x 3` possui `6 row lines` e `4 column lines`.

## Mesclando células

![Grid merge](/imagens/grid-merge.png)

```css
.grid-item {
  grid-column-start: Y | nome-da-linha;
  grid-column-end: Y | nome-da-linha;
  grid-row-start: X | nome-da-linha;
  grid-row-end: X | nome-da-linha;
}
```

* X começa na column line designada por nome ou número;

* X termina na column line designada por nome ou número;

* Y começa na row line designada por nome ou número;

* Y termina na row line designada por nome ou número;
­
**Shorthand**

```css
.grid-item {
  grid-column: X / Y;
  grid-row: X / Y;
}
```

* X começa na line designada por nome ou número;

* Y termina na line designada por nome ou número;

Modelo:

```css
.item-a {
  grid-column: 2 / 5;
  grid-row-start: row1-start;
  grid-row-end: 3;
}
```

## Posicionando um item

![Grid position](/imagens/grid-position.png)

Após ter dado um nome para uma área (no container), você pode posicionar um item dentro dela usando o nome. Ou então simplesmente usar as coordenadas (linhas) para posicioná-lo.

```css
.item-d {
  grid-area: name | Xs / Ys / Xe / Ye;
}
```

* name: nome dado para uma área

* Xs: Row Start;

* Ys: Column Start;

* Xe: Row End;

* Ye: Column End;
­
## Alinhamento horizontal individual

![Grid ih](/imagens/grid-ih.png)

```css
.item-a {
  justify-self: start | end | center | stretch;
}
```

## Alinhamento vertical individual

![Grid iv](/imagens/grid-iv.png)

```css
.item-a {
  align-self: start | end | center | stretch;
}
```

### Alinhamento individual shorthand

![Grid align short](/imagens/grid-alignshort.png)

* O valor se aplica tanto horizontal quanto verticalmente.

```css
.item-a {
  place-self: center | stretch;
}
```

## Outros valores

* **min-content**: o tamanho mínimo do conteúdo. Imagine uma linha de texto como “E pluribus unum”, o conteúdo mínimo é provavelmente a largura do mundo “pluribus”.

* **max-content**: o tamanho máximo do conteúdo. Imagine a frase acima, o conteúdo máximo é o comprimento de toda a frase.

* **auto**: esta palavra-chave é muito parecida com unidades fr, exceto que elas “perdem” a luta no dimensionamento contra unidades fr ao alocar o espaço restante.

* **fit-content**: use o espaço disponível, mas nunca menos que min-content e nunca mais que max-content.

* **unidades fracionárias**: Xfr. Basicamente "parte do espaço restante". Ex.:

```css
colunas de modelo de grade: 1fr 3fr;
```

Significa, vagamente, 25% 75%. Também se associam bem a outros valores:

```css
grid-template-columns: 50px min-content 1fr;
```

## Mínimo e máximo

Limita o tamanho dos grid items quando o grid container muda de tamanho.

```css
.container {
  grid-template-columns: minmax(MINpx, MAXpx);
}
```

* MIN é o mínimo que encolhe;

* MAX é o máximo que aumenta;

**Modelo 1**

* Três colunas com largura entre 90px e 1fr.

```css
grid-template-columns: repeat(3, minmax(90px, 1fr));
```

**Modelo 2**

* Duas colunas, uma com largura de 100px, e outra entre 90px e 1fr.

```css
grid-template-columns: 100px minmax(50px, 200px);
```

## Preenchimento automático

É usada dentro de `repeat()`:

* **auto-fill**: Ajusta o maior número possível de colunas em uma linha, mesmo que estejam vazias.

* **auto-fit**: Encaixa quaisquer colunas que existam no espaço (prefira expandir as colunas para preencher o espaço em vez de colunas vazias).

**Modelo 1:**

Auto-fill: Quando o tamanho do contêiner muda, esta configuração continua inserindo colunas de 60px e esticando-as até que seja possível inserir outra. Observação: se não for possível ajustar todos os grid items no grid container, os grid items que ficarem de fora do grid container serão movidos para uma nova linha (similar a wrap):

```css
.container {
  grid-template-columns: repeat(auto-fill, minmax(60px, 1fr));
} 
```

**Modelo 2:**

Auto-fit: funciona quase de forma idêntica ao auto-fill. A única diferença é que, quando o tamanho do grid container for maior que a soma da largura de todos os grid items, o auto-fill continua inserindo linhas ou colunas vazias e empurra os grid items para o lado, enquanto o auto-fit estica os grid items para caber no tamanho do grid container.

* Observação: se não for possível ajustar todos os itens em uma linha, eles serão movidos para uma nova linha:

```css
.container {
  grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
}
```

**!IMPORTANT**

* O Grid pode tornar ainda mais fácil a tarefa de criar um site responsivo ao usar [media-queries]() para reorganizar as áreas do grid, alterar as dimensões do grid e reorganizar a posição dos itens;

* O Grid só enxerga a hierarquia pai-filho; não vai aplicar as propriedades grid para elementos que não estejam diretamente relacionados. Portanto é possível criar um grid dentro de um item do grid usando display: grid novamente;

-----------------------------------------------------------

<https://css-tricks.com/snippets/css/complete-guide-grid/>