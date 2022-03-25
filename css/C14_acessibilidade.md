# ACESSIBILIDADE

## Leitores de tela

Ocultando visualmente conteúdos destinados apenas a leitores de tela:

```html
<table class="sr-only">
  [...]
</table>
```

```css
.sr-only {
  position: absolute;
  left: -10000px;
  width: 1px;
  height: 1px;
  top: auto;
  overflow: hidden;
}
```

* Observação: as seguintes abordagens não devem ser utilizadas:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ `display: none;` ou `visibility: hidden;` oculta o conteúdo para todos, incluindo usuários de leitores de tela, portanto não use.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Valores zero para o tamanho como `width: 0px;` e `height: 0px;` removem esse elemento do fluxo do seu documento, o que significa que os leitores de tela vão ignorá-lo, e portanto você não deve utilizá-los.

## Contraste

As Diretrizes de Acessibilidade de Conteúdo da Web (WCAG) recomendam uma relação de contraste de, pelo menos, 4,5 para 1 para texto normal. A proporção é calculada comparando os valores de luminância (brilho) entre duas cores. Isso varia de 1: 1, para a mesma cor (ausência de contraste), até 21: 1 para branco em contraste com preto, o mais forte. Este contraste também deve existir mesmo em sites coloridos, visto que pessoas com daltonismo podem ver alguns tons em escalas de cinza.

Cores vizinhas no círculo cromática também não são indicadas como contraste, pois pessoas com daltonismo podem não distinguir.

Verifique através do [inspect](https://docs.microsoft.com/pt-br/microsoft-edge/devtools-guide-chromium/accessibility/color-picker).