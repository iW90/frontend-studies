# RESPONSIVIDADE

## Largura de imagem

```css
div {
  max-width: 800px;
  min-width: 320px;
}
/* Ao invés de width, use máximo e mínimo para ter maior responsividade. */

img {
  width: 100%
}
/* width 100% para imagens dentro do div. */
```

* Usar [imagens]() para ter responsividade de imagens.

* Referência mínima: 320px é a largura máxima de celulares antigos em pé.

    * subtrair desse valor o tamanho da padding usada.

## Largura de vídeo

 Colocar o `<iframe>` dentro de um `<div class="video">` pode ajudar.

```css
div.video {
  position: relative;
  padding-bottom: 59%;
}

div.video > iframe {
  position: absolute;
  top: 5%;
  left: 5%;
  width: 90%;
  height: 90%;
}
```

## Imagens pixeladas

Devido à diferença na densidade de pixels (PPI/DPI) entre uma "Retina Display" e "Non-Retina", algumas imagens feitas na primeira tela podem parecer pixeladas na segunda tela.

Para contornar este problema, basta reduzir os valores da largura e altura para a metade do tamanho original.

```css
img {
  height: 250px;
  width: 250px;
}
```

* Largura original: 500px;

* Altura original: 500px;