# BORDAS

## Border style

```css
border-style: top right left bottom; /* estilo */
border-color: top right left bottom; /* cor */
border-width: top right left bottom; /* espessura */
```

É possível definir diferentes tipos de bordas para cada aresta.

![Border Style](/imagens/border-style.png "Estilos de bordas")

**style:**

* **dotted**: Pontilhado

* **dashed**: Tracejado

* **solid**: Sólida

* **double**: Sólida dupla

* **groove**: Borda 3D (cores definidas em border-color)

* **ridge**: Borda 3D (cores definidas em border-color)

* **inset**: Borda 3D  (cores definidas em border-color)

* **outset**: Borda 3D (cores definidas em border-color)

* **hidden**: Borda invisível

* **none**: Sem borda

## Border ou outline shorthand

```css
outline: 1px solid black;
border: 2px dotted red;
/* width > style (obrigatório) > color */
```

## Frame border

* *(não compatível com todos os navegadores)*

Crie uma imagem em PNG e testa tamanho do slice (sem unidade de medida) até acertar o tamanho:

![Border](/imagens/border-1.png)

```css
border: 10px solid transparent; /* obrigatório ter border */
border-image-source: url('borda.png');
border-image-slice: 20;
border-image-repeat: repeat (repete arestas) | stretch (estica arestas);

/* shorthand */
border-image: url('borda.png') 20 repeat;
```

![Frame border](/imagens/borda-teste.png)

## Bordas arredondadas

```css
border-radius: 20px;
/* Todas as bordas iguais */
```

```css
border-radius: 50%;
/* A imagem se torna circular */
```

```css
border-radius: 10px 20px
```

* border-top-left-radius | border-bottom-right-radius

* border-top-right-radius | border-bottom-left-radius

![Border Direction](/imagens/border-direction.png)

```css
border-radius: 10px 20px 30px 40px;
```

* border-top-left-radius

* border-top-right-radius

* border-bottom-right-radius

* border-bottom-left-radius

### Formas com border-radius

É possível dar diversas formas a um objeto com border-radius:

![Formas](/imagens/formas-bordas.png)

O site [9Elements](https://9elements.github.io/fancy-border-radius/full-control.html "cria formatos personalizados com bordas") ajuda a criar outras formas!



### Outras configurações com bordas

border-corner-shape: bevel;

border-corner-shape: curve;

border-corner-shape: notch;

border-corner-shape: scoop;

Exemplos:

* Create a trapezoid:

```css
border-corner-shape: bevel;
border-radius: 25% / 100% 100% 0 0;
```

* Create a diamond (rhombus) shape:
```css
border-corner-shape: bevel;
border-radius: 50%;
```

Extra: <https://lea.verou.me/tag/css4/>

## Exemplos de shadow

```css
/* offset-x > offset-y > spread-radius > color */
box-shadow: 2px 3px 1px black;

OU

/* none/inset > offset-x > offset-y > blur-radius > spread-radius > color */
box-shadow: inset 1px 2px 3px 4px red;

OU

/* Any number of shadows, separated by commas */
box-shadow: 3px 3px red, -1em 0 0.4em olive;
```

**Sequência caso algum item não seja preenchido:**

* offset-x | offset-y | color

* offset-x | offset-y | blur-radius | color

* offset-x | offset-y | blur-radius | spread-radius | color

* inset | offset-x | offset-y | blur-radius | spread-radius | color

É possível configurar cada aresta separadamente:

```css
box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
```