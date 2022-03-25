# LISTAS

[HTML Listas]()

## Listas ordenadas e não ordenadas

```css
ul, ol {
  list-style-position: inside;
/* Por padrão, as bolinhas ou números ficam pra fora da caixa; */

  list-style-type: '\nºdoSímbolo\00A0\00A0';
/* Não é compatível com todo navegador. */
/* 00A0 é um código para espaço */
/* ºdoSímbolo Exemplo: U+2713, use apenas 2713 */

  list-style: none;
/* Remove o bullet no início da lista, mas não o padding */
}
```