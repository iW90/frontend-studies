# MULTIMÍDIAS

## Áudio

```html
<audio src="musica.mp3" controls autoplay></audio>
```

### Áudio responsivo

```html
<audio preload="" autoplay controls loop>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
  <source src="audio.wav" type="audio/wav">
  <p>Infelizmente este navegador não possui suporte para áudios.</p>
</audio>
```

**preload=**

* `"auto"` o site só carrega depois que o áudio carrega.

* `"metadata"` o site só pega informações dos áudios.

* `"none"` só carrega se a pessoa der play.

**type=**

* [Lista de Tipos](https://www.iana.org/assignments/media-types/media-types.xhtml "lista de tipos")

#### Observações

1. Não toca todos, apenas o primeiro que o navegador suporta;

2. Carrega na sequência colocada, de cima para baixo;

3. Utilize do mais leve ao mais pesado, evite wav que é pesado;

## Vídeos

```html
<video src="video.mp4" width="XXpx" height="YYpx" controls></video>
```

### VÍDEO RESPONSIVO

```html
<video poster="imagem.jpg" width="" height="" controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.m4v" type="video/mp4">
  <source src="video.webm" type="video/webm">
  <source src="video.ogv" type="video/ogg">
  <p>Infelizmente este navegador não possui suporte para áudios.</p>
</video>
```

**preload=**

* `auto` o site só carrega depois que o vídeo carrega.

* `metadata` o site só pega informações dos vídeos.

* `none` só carrega se a pessoa der play.

**type=**

* [Lista de Tipos](https://www.iana.org/assignments/media-types/media-types.xhtml "lista de tipos")

#### Observações

1. Vídeos locais consomem muito tráfego de dados, melhor usar Youtube, Vimeo, etc.

2. Não toca todos, apenas o primeiro que o navegador suporta;

3. Carrega na sequência colocada, de cima para baixo;

4. Utilize do mais leve ao mais pesado;