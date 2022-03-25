# ANIMAÇÕES

## Keyframes

Especifica exatamente o que acontece na animação ao longo de sua duração, sendo 0% o início e 100% o fim.

* O valor de *animation-name* deve ser o mesmo nome da regra *@keyframes*:

```css
#elemento {
  animation-name: XXX;
  animation-duration: 3s;
}

@keyframes XXX {
  0% {
    background-color: blue;
  }
  100% {
    background-color: yellow;
  }
}
```

```css
#elemento:hover {
  animation-fill-mode: forwards;
}
```
Por padrão, a animação retorna ao primeiro frame. Com forwards, ela pausa no último frame.

```css
/* Single animation */
animation-fill-mode: none;
animation-fill-mode: forwards;
animation-fill-mode: backwards;
animation-fill-mode: both;

/* Multiple animations */
animation-fill-mode: none, backwards;
animation-fill-mode: both, forwards, none;
```

## Movimento

```css
#elemento {
  animation-name: XXX;
  animation-duration: 3s;
  position: relative;
}

@keyframes XXX {
  0% {
    background-color: red;
    top: 0px;
  }
  0% {
    background-color: yellow;
    top: 50px;
  }
  100% {
    background-color: red;
    top: 0px;
  }
}
```

## Repetições

```css
  animation-iteration-count: X | infinite;
```

A animação repete X vezes ou infinitamente;
­
## Variação de Velocidade

```css
animation-timing-function: ease | ease-in | ease-out | linear;
```

* **ease:** devagar - acelera - desacelera;

* **ease-in:** acelera - desacelera;

* **ease-out:** devagar - acelera;

* **linear:** constante;

Definindo sua própria velocidade:

```css
animation-timing-function: cubic-bezier(0.25, 0.25, 0.75, 0.75);
```

* Os valores acima são o equivalente a "linear".

* A função *cubic-bezier* é um polinômio.

* Todas as funções cubic-bezier começam com p0 em (0, 0) e terminam com p3 em (1, 1).