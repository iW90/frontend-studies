# BOXES

## Tamanhos

### Width

```css
max-width: Largura máxima;
min-width: Largura mínima;
width: XXpx; /* medida fixa */
width: XX% ou XXem; /* relativo ao tamanho do parent */
```

### Height

```css
max-height: Altura máxima;
min-height: Altura mínima;
height: 100vh;
```

### Unidades de medida

* **vh (view height):** 100% da altura do viewport;

* **vw (view width):** 100% da largura do viewport;

* **vmin (mínimo da viewport):** 70vmin seria 70% da menor dimensão da viewport (altura ou largura).

* **vmax (máximo da viewport):** 100vmax seria 100% da maior dimensão da viewport (altura ou largura).

## Tipos de caixa

![Inline-block](/imagens/inline-block.png "Comparação entre inline e block)

```css
display: block;
/* box-level (ex.: div): sempre se inicia numa linha nova, sempre ocupa a largura total, sempre pula pra próxima linha. */

display: inline;
/* inline-level (ex.: span): não pula pra próxima linha, continua na frente do elemento anterior, e depois que termina tb não quebra a linha. "margin: auto;" não funciona no inline, como por exemplo <img>.*/

display: inline-block;
/* inline-level (ex.: span): não pula pra próxima linha, continua na frente do elemento anterior, e depois que termina tb não quebra a linha. Mas tem as configurações padrões de margin, padding e border do block. */

display: none;
/* torna o elemento oculto e não ocupa espaço. É como se deletasse o item, sem efetivamente apagá-lo. */
```

## Espaçamentos

* **Padding:** margem interna;

* **Border:** borda externa;

* **Margin:** margem externa;

* **Outline:** borda por dentro da *margin*, encostada na *border*, mas pode extrapolar a *margin*.

### Shorthand margin e padding

![margin-padding](/imagens/margin-padding.png "Sequência do shorthand de margin e padding")

```css
margin: 1px 2px 3px 4px;
/* Top > Right > Bottom > Left */

padding: 1px 2px;
/* Top e Bottom > Right e Left */

margin: 5px;
/* Todas as medidas iguais */

margin: auto;
/* Centraliza elementos block horizontalmente */
```

## Box-sizing

Faz border e margin serem inclusos na soma de *widht* e *height*.

```css
box-sizing: border-box;
```

## Shorthand border ou outline

[Bordas]()

```css
outline: 1px solid black;
border: 2px dotted red;
/* width > style (obrigatório) > color */
```