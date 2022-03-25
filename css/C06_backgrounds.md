# BACKGROUNDS

## Cor de fundo

RGB (red, green, blue):

* `background-color: rgb(255,255,255);`

HSL (hue, saturation, lightness):

* `background-color: hsl(0, 100%, 100%);`

HEX (Hexadecimal):

* `background-color: #fff;`

Nome de Cores:

* `background-color: skyblue;`

## Gradiente

[Funções]()

```css
background: linear-gradient(XXdeg, 1cor, 2cor, 3cor, ncores);
background-image: radial-gradient(XXdeg, 1cor, 2cor, 3cor, ncores);
```

## Imagens de fundo

```css
background-image: url('caminho-ou-url-da imagem.jpg');
```

**Defaults:**

* Mantém tamanho original;

* Repetir horizontal e verticalmente;

### Ajustes da imagem de fundo

```css
background-repeat: repeat | no-repeat | x-repeat | y-repeat | space | round;
```

* **repeat:** repete horizontal e verticalmente;

* **no-repeat:** nunca repete;

* **repeat-x:** repete horizontalmente;

* **repeat-y:** repete verticalmente;

* **space:** repete com espaçamento entre as imagens;

* **round:** repete ajustando o tamanho de forma a não cortar as imagens nos extremos;

### Posicionamento da imagem de fundo

```css
background-position: x y;
```

* **x (horizontal):** left center right;

* **y (vertical):** top center bottom;

### Tamanho da imagem de fundo

```css
background-size: XXpx YYpx;
background-size: ZZ%;
background-size: contain | cover;
```

* **XX** para largura e **YY** para altura;

* **ZZ** largura, altura aumenta proporcionalmente;

* **contain:** se adapta à tela para mostrar a imagem 100%, sem deformar;

* **cover:** cobre a tela toda, mesmo que acabe cortando as extremidades;

## Vínculo

```css
background-attachment: scroll | fixed ;
```

* **scroll:** a imagem rola com a tela; 

* **fixed:** a imagem fica fixada no lugar, sem rolar;

## Shorthando para background

```css
background: black url('') center center no-repeat [cover*] fixed;
/* color > image > position-x position-y > repeat > [size*] > attachment; */
```

* **size** ainda não funciona no shorthand apesar de incluído no manual, necessário incluir separadamente até que navegadores atualizem;

## Centralização vertical

```css
#container {
  position: relative;
}

#content {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
```

* left e top consideram o canto superior esquerdo como ancoragem, para centralizar colocamos a ancoragem no centro usando transform (serve para mover o content).

## Extensão do background

```css
.container {
  background-clip: border-box | padding-box | content-box;
}
```

* **border-box**: Preenche todo o *container*, inclusive atrás da borda.

* **padding-box**: Preenche todo o *container*, mas não por trás da borda.

* **content-box**: Preenche somente atrás do *content*, não inclui borda nem padding.
­
___

## Efeito paralax

```css
.box01 {
  background-color: #fff;
}

.box02 {
  background-image: ('');
  background-attachment: fixed;
} 
```