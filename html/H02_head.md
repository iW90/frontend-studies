# TAGS DE HEAD

Metadados, não aparecem no corpo do site. Não confundir com a tag `header`.

## Title

```html
<title> Título exibido na aba do site </title>
```

## Import Style

```html
<link rel="stylesheet" href="style.css"> Importa arquivo CSS.
```

## Import favicon

```html
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon"> Icon exibido na aba do site.
```

## Import fonts

```html
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400" rel="stylesheet"> Importa fontes.
```

* Recomendado que seja feito por CSS: [\(@import\)]()
## Names

São associados ao conteúdo do atributo content. Valores de `name`:

* **author:** Autor do documento;

* **keywords:** Palavras-chave, tags, palavras em buscas;

* **description:** Contém uma descrição do conteúdo da página. Alguns browsers usam este meta como descrição padrão da página quando é marcada.

* **creator:** Criador do documento, podendo ser uma instituição. Se há mais de uma, muitos elementos `<meta>` podem ser usados;

* **publisher:** Nome do editor do documento, podendo ser uma instituição;

* **viewport:** Dá dicas sobre o tamanho inicial do viewport. Este pragma é usado por dispositivos móveis (*width, height, initial-scale, maximum-scale, minimum-scale, user scalable*).­

### Description

* Descrição do site exibida na busca do Google abaixo do título.

* Frases de 140-160 caracteres. Se for muito longa, fica cortado.

* Inclua palavras-chave.

* Crie tags significativas e descritivas, apresentando seu conteúdo

```html
<meta name="description" content="Descrição que será exibida">
```

## Charset

```html
<meta charset="UTF-8"> Tipo de caracteres exibidos no site. Padrão pt-br é UTF-8.
```

ou no CSS:

```css
@charset "UTF-8";
```

**!Important**

* Esse elemento <meta> deve estar dentro dos primeiros 1024 bytes da página, pois alguns navegadores só olham para esses primeiros bytes antes de escolher um caractere definido para a página.

## Refresh

```html
<meta http-equiv="refresh" content="3;url=https://www.mozilla.org">
```

Este pragma especifica:

* O número de segundos até a página ser recarregada, se o atributo content contém apenas um numero inteiro positivo;

* O número de segundos ate a página ser redirecionada para outro lugar, se o atributo content contém um inteiro positivo seguido de uma string `;url=` e uma URL válida.

