# FUNÇÕES

## Blur

```css
filter: blur(XXpx);
```

* Desfoca **XX** pixels (quanto maior o valor, maior o desfoque).

## Escala de Cinza

```css
filter: grayscale(XX%);
```

*(max até 100%)*

* Acinzenta **XX** por cento (0% é colorido e 100% é preto e branco).

## Opacidade

```css
filter: opacity(XX%);
```

*(max até 100%)*

* Deixa **XX** por cento translúcido (0% é visível e 100% é invisível).

* OU: O valor 1 é opaco, 0.5 é meio transparente e 0 é totalmente transparente.


## Brilho

```css
filter: brightness();
```

*(aceita valores acima de 100%)*

* Deixa **XX** por cento mais ou menos branco (0% é tudo preto, 100% é o default, +100% deixa esbranquiçado).

## Saturação

```css
filter: saturate();
```

*(aceita valores acima de 100%)*

* Deixa **XX** por cento mais ou menos vívido (0% não tem cor, 100% é o default, +100% extrapola as cores).

## Contraste

```css
filter: contrast();
```
*(aceita valores acima de 100%)*

* Deixa **XX** por cento mais ou menos "profundo", aumentando ou diminuindo a diferença entre tons mais claros e tons mais escuros  (>100% deixa em tonalidades mais parecidas, 0% é o default, <100% é preto e branco).

## Shorthand

```css
filter: saturate() brightness() contrast();
```

* Basta colocar uma função uma na frente da outra, sem vírgulas;

## Gradient

```css
* {
  height: 100%
}

body {
  background-image: radial-gradient(1cor xx%, 2cor yy%, ncores);
  background-image: linear-gradient(90deg, 1cor xx%, 2cor yy%, ncores);
  background-image: repeat-linear-gradient(90deg, 1cor, 2cor, ncores);
}
```

* **linear** ou **radial**: em linha ou circular;

* **repeat**: repete o ciclo de cores;

* **90deg**: ângulo;

* **xx% / yy%**: em relação à proporção;

## Listras

Ao invés de porcentagem, podemos usar **px** para definir a distância entre a cor e a borda do elemento:

```css
background: repeating-linear-gradient(90deg,
yellow 0px, blue 40px, green 40px, red 80px);
```

As cores *blue* e *green* não vão se misturar, pois começam na mesma distância. Será perceptível somente a transição entre *yellow* e *azul* | *green* e *red*.

A partir dessa ideia é possível criar listras:

```css
background: repeating-linear-gradient(45deg,
  yellow 0px,
  yellow 40px,
  black 40px,
  black 80px
);
```

## Transform

Quando usado com *:hover* pode dar movimento a um objeto.

### ESCALAS (scaleX / scaleY)

Redimensiona uma imagem proporcionalmente em uma escala de X.

```css
transform: scale(x);
```

### ROTAÇÃO

Rotaciona a **XX** graus (aceita valores positivos (sentido horário) e negativos (anti-horário).

```css
transform: rotation(XXdeg);
```

### SKEW (skewX / skewY)

Inclina um objeto ( / ) sobre o eixo definido.

```css
transform: skewX(XXdeg);
```