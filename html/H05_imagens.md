# IMAGENS

* Imagens são inline-level, portanto `margin: auto;` não centraliza. É necessário colocar `display: block;` pra centralizar. Veja mais em [boxes]().

## Inserindo imagens

```html
<img src="link-da-imagem.jpg" alt="texto descritivo para acessibilidade">
```

* Imagens meramente ilustrativas costumam ter o `alt=""` (vazio).

## Imagens que se adaptam ao ecrã

```html
<picture>
  <source media="(max-width: PPpx)" srcset="link.PP.png" type="image/png">
  <source media="(max-width: MMpx)" srcset="link.MM.png" type="image/png">
  <img src="link.GG.png" alt="imagem flexível">
</picture>
```

* Usar [responsividade]() para adaptar os divs a diferentes tamanhos de ecrãs.