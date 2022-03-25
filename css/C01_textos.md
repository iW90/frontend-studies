# ESTILIZAÇÃO DE TEXTO

## font

```css
font-variant: small-caps;
font-size: 1em;
font-style: italic;
font-family: 'Work Sans', 'sans-serif';
font-weight: lighter // normal // bold // bolder // 100, 200, ..., 900;
/* 'Work Sans': melhor fonte para ver weight */
```

### font-shorthand

```css
font: italic small-caps bold 12px/30px 'Georgia', serif;
```

Pode pular um item, contanto que sempre respeitando a ordem correta:

* font-style

* font-variant

* font-weight

* font-size/line-height

* font-family

## font-size

### Medidas Absolutas

* `px`: pixel (recomendável, padrão é 16px)

* `cm`: centímetros

* `mm`: milímetro

* `in`: inches/polegadas

* `pt`: ponto

* `pc`: paica

### Medidas Relativas

* `em`: ao tamanho da altura-M (recomendável, padrão 1em)

* `ex`: ao tamanho da altura-x

* `rem`: ao tamanho da root, fonte configurada no body

* `vw`: viewport, % da tela

* `vh`: altura da viewport

* `vw`: largura da viewport

* `%`: porcentagem

**PS.: Normalmente 1em = 16px**

## font-family

* **serif:** 'Times New Roman'

* **sans-serif:** 'Arial'

* **monospace:** 'TrueType'

* **cursive:** *handwriting* ou 'Comic Sans MS'

* **fantasy:** *display* ou fontes decorativas

Um valor reserva se chama *"fallback"*, que é a segunda opção de fonte caso a primeira não funcione.

## color

RGB (red, green, blue):

* `color: rgb(255,255,255);`

HSL (hue, saturation, lightness):

* `color: hsl(0, 100%, 100%);`

HEX (Hexadecimal):

* `color: #fff;`

Nome de Cores:

* `color: skyblue;`

## Importando fontes

### Fontes Externas

Vindas de sites como [Google Fonts]()

* *html*

```html
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400" rel="stylesheet">
```

* *css*

```css
@import url('https://fonts.googleapis.com/css?family=Open+Sans:400');
```

### Fontes Externas Baixadas

```css
@font-face {
  font-family 'nome da fonte';
  src: url('../fonts/caminho-da-fonte.otf') format('opentype'), url('../fonts/caminho-da-fonte.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
}
```

**Tipos de format()**

* opentype otf

* truetype ttf

* embedded-opentype

* truetype-aat (Apple Advanced Typography)

* svg

## Parágrafos

### Indentação

```css
text-indent: 20px;
```

Espaço no início da primeira linha do parágrafo;

### Alinhamento

```css
text-align: center | right | left | justify;
```

## Outras ações para texto

### Maiúsculas, minúsculas, capital

```css
text-transform: lowercase | uppercase | capitalize;
```

### Sublinhado, sobrelinhado e rasurado

```css
text-decoration: underline | overline | line-through | none;
```

### Sombreado

```css
/* offset-x > offset-y > spread-radius > color */
text-shadow: 2px 3px 1px black;

/* none/inset > offset-x > offset-y > blur-radius > spread-radius > color */
text-shadow: inset 1px 2px 3px 4px red;

/* Any number of shadows, separated by commas */
text-shadow: 3px 3px red, -1em 0 0.4em olive;
```

**Sequências:**

* offset-x | offset-y | color

* offset-x | offset-y | blur-radius | color

* offset-x | offset-y | blur-radius | spread-radius | color

* inset | offset-x | offset-y | blur-radius | spread-radius | color

## Colunas

```css
  columns: X;
/* Divide em X colunas. Atenção aos ecrãs pequenos. */
```