# LINKS

[CSS: links]()

## Navegando

```html
<a href="link" target="_blank" rel="external"> Texto linkado </a>
```

**href=**

* Por convenção, `"#"` é usado como valor no `href` quando ainda não sabemos o link para o qual o conteúdo irá direcionar.
 
**target=**

* `"_self"` (default) abre na aba ativa

* `"_blank"` abre em uma nova aba em branco

**rel=**

* `"next"` indica que o link é para a próxima parte do site

* `"prev"` indica que é pra parte anterior do site

* `"author"` indica que o link é para o site do autor

* `"external"` indica que é um link externo

* `"nofollow"` indica que é para um link não endossado

# Downloads

```html
<a href="#" download="arquivo.pdf" type="application/pdf"> Texto linkado </a>
```

**type=**

* `"application/zip"`

* `"text/html"`

* `"video/mp4"`

* `"audio/aac"`

* `"audio/mpeg"`

* `"font/ttf"`

* `"image/png"`

* Outros: <https://www.iana.org/assignments/media-types/media-types.xhtml>

## Links para partes da página

```html
<a href="#ID-do-item"> Texto linkado </a>
<footer id="ID-do-item"> Rodapé </footer>
```

A página vai rolar até o footer.

Basta referenciar o ID da tag para que o link direcione a ela.