# ESTRUTURA

## Rules

![Rules](/imagens/rules.png "rules")

## Seletores

* \* *(seletor universal)*

* type *(tags: p, h1, div, ...)*

* .class *(agrupável)*

* \#ID *(não agrupável)*

* :pseudo-class *(efeitos sob ações: hover)*

* ::pseudo-element *(primeiro child, segundo child)*

* [atributo] *(seletor de atributo)*

* [atributo="value"] *(seletor de atributo com valor)*

* @keyframes *(regra de animações)*

* @media *(media querie)*

## Cascade (Cascata)

Ordem de prioridades:

**1. Importância**

1.1 transition

1.2 !important (colocado no fim de uma declaração, antes do ";")

1.3 animation

1.4 normal

**2. Origem**

2.1 website (style definido no css)

2.2 user Preference (configuração feita pelo usuário no navegador)

2.3 browser (padrão do navegador)

**3. Specificidade**

3.1 inline (style direto do html)

3.2 layer (a camada que está por cima se sobrepõe)

3.3 ID

3.4 class | attribute | pseudo-class | type | pseudo-element

 ⤷ 3.4.5 Quando mais específico, maior a prioridade

**4. Position** (códigos inseridos por último vencem)

## Combinadores

```html
<button> Botão 1 </button>
<input>
<button> Botão 2 </button>
<button> Botão 3 </button>
```

* (**+**): Seleciona o primeiro irmão seguinte do mesmo nível:

`input + button { apenas Botão 2; }`

* (**~**): Seleciona os demais irmãos seguintes do mesmo nível:

`input ~ button { Botões 2 e 3; }`

```html
<div class="pai"> Pai
  <div class="filho"> Filho
    <div class="filho"> Neto
    </div>
  </div>
</div>
```

* (**>**): Seleciona apenas filhos diretos:

`.pai > .filho { apenas Filho; }`

* (**&nbsp;**): Seleciona todos os descendentes:

`.pai .filho { Filho e Neto; }`

## Estrutura

* Quando escrito tudo junto, trata-se do mesmo elemento:

```html
<h1 class="content"> h1.content
<h1 class="content1 content2"> .content1.content2
<!-- é possível ocultar o type como no segundo exemplo -->
```

* Quando escrito separado, trata-se do combinador de descendentes:

```html
<div class="parent"> <!-- A -->
  <div class="child"> <!-- B -->
    <div class="child"> <!-- C -->
      div.parent .child { não importa o quão profunda seja a camada, engloba todos os child B e C dentro do parent A; }
    </div>
  </div>
</div>
```

## Seletor de atributo

[attr="value"]

**attr:** atributo

**value:** valor do atributo

Exemplo:

```html
<input type="radio">
```

```css
[type="radio"] { }
```

## :Root

É um seletor do tipo pseudo-class que corresponde ao elemento raiz do documento. Ao criar variáveis usando a :root, elas estarão disponíveis globalmente e podem ser acessadas a partir de qualquer outro seletor no CSS.

Exemplo:

```css
:root {
  --var: value;
}

* {
  element: (--var, fallback);
}
```

## Pseudo-elementos

São usados para modificar determinado conteúdo de um elemento sem adicionar uma classe ou ID. 

**::before** primeiro filho do elemento selecionado;

**::after** último filho do elemento selecionado;

* PS.: Não confundir :after/:before (pseudo-class) com ::after/::before (pseudo-elements)

Por exemplo, para adicionar uma símbolo antes de um parágrafo:

```html
<a> Conteúdo </a>
```

```css
a::after {
  content: "🔗";
}
```

Conteúdo exibido será:

🔗 <Conteúdo>

Caso não sejam adicionados novos _content_, deixar esta propriedade em branco. Dessa forma é possível apenas mudar formatações adicionando outras propriedades.

Desenhando um Coração ♥

```html
<style>
  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: rotate(-45deg);
  }
  .heart::after {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart::before {
    content: "";
    background-color: pink;
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }
</style>
<div class="heart"></div>
```

## Keyframes

[Keyfranes]()