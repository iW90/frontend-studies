# TABELAS

[HTML Tabelas]()

## Borda

```css
table {
  border-collapse: separate | collapse;
}
```

## *Alinhamento do conteúdo na célula
```CSS
td {
  text-align: left | center | right; /* horizontal */
  vertical-align: top | middle | bottom; /* vertical */
}
```

## Efeito zebrado

```css
tbody > tr:nth-child(2n) {
  background-color: lightgray;
}
```

* `(2n)` = de dois em dois (linha sim, linha não);

* `(odd)` = linhas ímpares;

* `(even)` = linhas pares;

## Cabeçalho fixo

Pode ser que ainda não funcione em todos os navegadores, como o Safari.

```css
table {
  position: relative;
}

thead > tr > th {
  position: sticky;
  top: -1px;
  background-color: #000;
}
```

## Tabelas responsivas

```html
<div id="container">
  <table>
    ...
  </table>
</div>
```

* **Responsivo:** Rola somente a tabela, não o restante do conteúdo da página, mantendo o tamanho ajustado ao *div#container* e criando uma barra de rolagem somente na tabela.

```css
div#container {
  overflow-x: auto;
}
```

* Adapta a tabela para XX% do tamanho do *div#container* e cria uma barra de rolagem somente na tabela, não na página.

```css
div#container {
  width: XXvw;
}
```