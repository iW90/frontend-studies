# EFEITOS

## Transição

```css
a {
  color: white;
  transition-duration: 0.5s;
}

a:hover {
  color: black;
}
/* tempo de transição entre um efeito e outro. Colocar no estático, não no :hover. */
```

## Símbolo de visualizado no link (🗸)

```css
a.externo::after {
  content: '\nºdoSímbolo'
}
/* ºdoSímbolo Exemplo: U+2713, use apenas 2713 */
```