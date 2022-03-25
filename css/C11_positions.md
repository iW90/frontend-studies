# POSITION

```css
div {
  position: static | relative | fixed | sticky | absolute;
  top: 0; /* propriedade complementar */
  bottom: 1%; /* propriedade complementar */
  right: 2px; /* propriedade complementar */
  left: 3em; /* propriedade complementar */
} 
```

## Static *(default)*

Ele basicamente segue o fluxo comum da página. Não aceita as propriedades complementares (top, bottom, right, left).

![Static](/imagens/static.gif)

## Relative

Essa position habilita as propriedades complementares (top, bottom, left e right). É usado quando queremos alterar a posição de um elemento tendo como referência a posição inicial dele (ao invés de usar margin).

![Relative](/imagens/relative.gif)

## Fixed

Deixa de fazer parte do fluxo comum da página, se referenciando ao viewport (independente da barra de rolagem). Independente da barra de rolagem, torna-se fixo em uma posição específica da tela, definido através das propriedades complementares (top, bottom, right, left).

![Fixed](/imagens/fixed.gif)

## Sticky

*(new: ainda não funciona em todos os navegadores)*

Semelhante ao fixed, mas ao invés de ficar fixo em relação à tela, ele fica fixo em relação ao rolamento da página. Volta a ocupar a sua posição inicial quando voltamos com a barra de rolagem como antes. É necessário definir os limites através das propriedades complementares (top, bottom, left e right).

![Sticky](/imagens/sticky.gif)

## Absolute
Posiciona-se em qualquer lugar da tela através das propriedades complementares (top, bottom, left e right). Ele deixa de fazer parte do fluxo comum e o espaço destinado a ele deixa de existir no documento ("flutua"), sobrepondo outros elementos.

Possui dois comportamentos:

* *Parent static position / no parent*

O canto superior esquerdo do viewport é referência:

![Absolute sem parent](/imagens/absoluteNoParent.gif)

* *Parent demais positions*

O elemento pai é referência para seu posicionamento:

![Absolute com parent](/imagens/absoluteParent.gif)

## Float

Os elementos são removidos do fluxo normal de um documento e posicionados em relação ao elemento pai. O restante do conteúdo contorna o elemento com float. Essa propriedade é comumente usada com a propriedade *width* para especificar o espaço horizontal. Comportam-se como inline um com o outro.

```css
div {
  float: none | left | right;
  width: XX%;
} 
```

## Empilhamento

Modifica a ordem de sobreposição dos elementos. **X** é representado por um número inteiro, e os valores maiores movem o elemento para cima na pilha.

```css
z-index: X;
```