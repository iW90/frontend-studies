# FLEXBOX

## Eixos

O eixo principal (main axis) pode ser tanto horizontal quanto vertical e será definido por flex-direction. O outro eixo perpendicular é chamado de eixo transversal (cross axis).

![Eixos](/imagens/flex-axis.png)

```html
<div class="flex-container">
  <div class="flex-item">1</div>
  <div class="flex-item">2</div>
  <div class="flex-item">3</div>
</div>
```

```css
.flex-container {
  display: flex | inline-flex;
}
```

## Direção

Estabelece o eixo principal:

![Direction](/imagens/flex-direction.png)

```css
.flex-container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

## "Quebra de linha"

Permite que haja uma quebra de linha para que o conteúdo se encaixe dentro do elemento pai:

![Wrap](/imagens/flex-wrap.png)

```css
.flex-container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

* **nowrap** (default): todos os flex items ficarão em uma só linha;

* **wrap**: os flex items vão quebrar em múltiplas linhas, de cima para baixo;

* **wrap-reverse**: os flex items vão quebrar em múltiplas linhas de baixo para cima;

## Shorthand: direction + wrap

```css
.flex-container {
  flex-flow: row nowrap | row wrap | column nowrap | column wrap;
}
```

## Alinhamento do eixo principal

Forma como os flex-items são distribuídos no flex-container:

![Jusfity content](/imagens/flex-justify.png)

```css
.flex-container {
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
}
```

* **flex-start** _(default)_**:** os itens são alinhados junto à borda de início (start) do flex-direction.

* **flex-end:** os itens são alinhados junto à borda final (end)  do flex-direction.

* **start:** os itens são alinhados junto à borda de início da direção do writing-mode (modo de escrita).

* **end:** os itens são alinhados junto à borda final da direção do writing-mode (modo de escrita).

* **left:** os itens são alinhados junto à borda esquerda do container, a não ser que isso não faça sentido com o flex-direction que estiver sendo utilizado. Nesse caso, se comporta como art.

* **right:** os itens são alinhados junto à borda direita do container, a não ser que isso não faça sentido com o flex-direction que estiver sendo utilizado. Nesse caso, se comporta como art.

* **center:** os itens são centralizados na linha.

* **space-between:** os itens são distribuídos de forma igual ao longo da linha; o primeiro item junto à borda inicial da linha, o último junto à borda final da linha.

* **space-around:** os itens são distribuídos na linha como se o mesmo espaçamento entre eles. Todos os itens tem a mesma quantidade de espaço dos dois lados: o primeiro item vai ter somente uma unidade de espaço junto à borda do container, mas duas unidades de espaço entre ele e o próximo item, pois o próximo item também tem seu próprio espaçamento que está sendo aplicado.

* **space-evenly:** os itens são distribuídos de forma que o espaçamento entre quaisquer dois itens da linha (incluindo entre os itens e as bordas) seja igual.

## Alinhamento do eixo contrário

![Align item](/imagens/flex-align-item.png)

```css
.flex-container {
  align-items: stretch | flex-start | flex-end | center | baseline;
}
```

* **stretch** _(default)_**:** estica os itens para preencher o container, respeitando o min-width/max-width).

* **flex-start/ start / self-start:** itens são posicionados no início do eixo transversal. A diferença entre eles é sutil e diz respeito às regras de flex-direction ou writing-mode.

* **center:** itens são centralizados no eixo transversal.

* **baseline:** itens são alinhados de acordo com suas baselines.

## Alinhamento das linhas

Não funciona caso haja apenas uma linha de itens.

![Align content](/imagens/flex-align-content.png)

```css
.flex-container {
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}
```

* **flex-start / start:** itens alinhados com o início do container. O valor (com maior suporte dos navegadores) flex-start se guia pela flex-direction, enquanto start se guia pela direção do writing-mode.

* **flex-end / end:** itens alinhados com o final do container. O valor (com maior suporte dos navegadores) flex-end se guia pela flex-direction, enquanto end se guia pela direção do writing-mode.

* **center:** itens centralizados no container.

* **space-between:** itens distribuídos igualmente; a primeira linha junto ao início do container e a última linha junto ao final do container.

* **space-around:** itens distribuídos igualmente com o mesmo espaçamento entre cada linha.

* **space-evenly:** itens distribuídos igualmente com o mesmo espaçamento entre eles.

* **stretch _(default)_**:** itens em cada linha esticam para ocupar o espaço remanescente entre elas.

### *safe* e *unsafe*

Funcionam nos três aligns:

Os modificadores podem ser usados em conjunto com todas essas palavras-chave e servem para prevenir qualquer alinhamento de elementos que faça com que o conteúdo fique inacessível (por exemplo, para fora da tela).

Safe garante que, independente da forma que você faça esse tipo de posicionamento, não seja possível "empurrar" um elemento e fazer com que ele seja renderizado para fora da tela (por exemplo, acima do topo), de uma forma que faça com que o conteúdo seja impossível de movimentar com a rolagem da tela (o CSS chama isso de "perda de dados").

## Sequência

Identifique qual o item a ser modificado através de uma ID ou outra class:

![Ordem](/imagens/flex-ordem.png)

```css
.flex-item #id2 {
  order: -2; /* o valor padrão é 0 */
}
```

## Proporções 

![Flex](/imagens/flex.png)

```css
.flex-item {
  flex-grow: 0; /* o valor default(padrão) é 0 */
  flex-shrink: 1; /* o valor padrão é 0 */
  flex-basis: auto | 100%; /* o valor padrão é auto */
  /* basis também aceita: content | max-content | min-content | fit-content; Mas poucos navegadores oferecem suporte. */
}

/* shorthand */
.flex-item {
  flex: grow > shrink > basis;
  flex: 0 1 auto; /* default */
}
```

Caso o valor de "flex" seja mudado para outro número diferente de 0, basis automaticamente se tornará 0%. Por exemplo:

```css
  flex: 1;
    ==
  flex: 1 1 0%;
```

Os três usam o tamanho do parent como base:

* **grow:** Proporção que aumenta em relação aos demais itens;

* **shrink:** Proporção que diminui em relação aos demais itens;

* **basis:** Proporção que ocupa em relação aos demais itens;

Obs.: Para que o valor de width e height de um objeto seja considerado e não fique espremido, é necessário colocar shrink: 0;

## Alinhamento individual

![Flex align self](/imagens/flex-align-self.png)

Permite sobrescrever alinhamento padrão ou do grupo:

```css
.flex-item #id2 {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

Os valores são os mesmos de align-items.

## Gap

![Gap](/imagens/flex-gap.png)

Define o espaço entre os itens:

```css
.container {
  gap: 10px; /* all gaps */
  gap: 10px 20px; /* row-gap column gap */
  row-gap: 10px;
  column-gap: 20px;
}
```

### Exemplo

Centralizar:

```css
.parent {
  display: flex;
  height: 300px; /* Or whatever */
}

.child {
  width: 100px;  /* Or whatever */
  height: 100px; /* Or whatever */
  margin: auto;  /* Magic! */
}
```

**!IMPORTANT**

* O Flex-Box só enxerga a hierarquia pai-filho; não vai aplicar as propriedades Flex para elementos que não estejam diretamente relacionados. Portanto é possível criar um flexbox dentro de um item do flexbox usando display: flex novamente;

* Para que as propriedades funcionem nos elementos-filhos, as pais devem ter propriedade display: flex; e serem configurados como um novo flex-box.

* As propriedades float, clear e vertical-align não têm efeito em flex-items.

-----------------------------------------------------------
<https://css-tricks.com/snippets/css/a-guide-to-flexbox/>