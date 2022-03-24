# TAB INDEX

## Organizando o tab

```html
<div tabindex="0"> I need keyboard focus! </div>
```

**tabindex**

* `-1` indica que um elemento está focado, mas não será acessado pelo teclado. Usado para focar um conteúdo programaticamente, como uma janela pop-up, de forma que o conteúdo ao fundo não possa ser acessado.

* `0` força o tab a passar por um objeto que normalmente não teria prioridade (como por exemplo `<p>`, `<div>`, `<span>`, antes de `input` (que recebem prioridade).

* `1` o foco é levado para esse elemento ao usar tab pela primeira vez. Em seguida, o foco passará ao próximo elemento que tem um tabindex maior que o anterior (2, 3, 4...). Quando não existirem mais itens para receberem foco, ele volta ao valor inicial (0).