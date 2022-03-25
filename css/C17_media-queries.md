# MEDIA QUERY

Media Queries consistem em um media type. Se esse media type corresponde ao tipo de dispositivo no qual o documento é exibido, os estilos são aplicados. Você pode ter quantos seletores e estilos quiser dentro de sua media query.

* O CSS dentro da *media query* é aplicado apenas se o tipo de mídia corresponder ao do dispositivo que está sendo usado.

```css
@media ( /* condição */ ) { /* CSS Rules */ }
```

Exemplo:

```css
@media (min-height: 350px) { 
  .class {
      /* CSS Declarations */
  }
}
```

## Media query no grid

[CSS Grid]()

```css
@media (min-width: 400px){
    .container{
      grid-template-areas:
      /* Altere apenas o código abaixo desta linha */
        "header header"
        "advert content"
        "footer footer";
      /* Altere apenas o código acima desta linha */
    }
  }
```