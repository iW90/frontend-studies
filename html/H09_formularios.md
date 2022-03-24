# FORMULÁRIOS

## Estrutura básica do formulário

```html
<form action="#" method="post"> Onde são inseridos dados do formulário
  <fieldset> "Conjunto de Campos", agrupa partes do formulário
    <legend> Título do Agrupamento </legend>

    <label for="associador"> Etiqueta do campo a ser preenchido </label>
    <input type="tipo" id="associador" name="coluna"> Entrada de dados

    <label for="associador2"> Etiqueta do campo a ser preenchido </label>
    <input type="tipo" id="associador2" name="coluna"> Entrada de dados
  </fieldset>
  <button> Botão de envio </button>
</form>

```

* **action=** é o link para onde os dados serão enviados e armazenados.

* **associador=** o valor inserido em `for` no label deve ser o mesmo valor inserido no `name` do input.

* **name=** o valor de `name` é o título do grupo para qual a informação dada pelo usuário será enviado.

* **method=** é o método de submissão do formulário (`get` ou `post`);

Existem duas formas de utilizar o `<label>`:

* **Explícita=** (recomendado) como é no modelo acima, com o `input` fora do `label`.

* **Implícita=** como é no modelo abaixo, com o `input` dentro do `label`.

```html
<!-- IMPLICIT LABEL (not recommended for use) -->
<!-- O associador torna-se opcional -->
<label> Título do campo a ser preenchido 
    <input type="tipo" name="coluna"> Entrada de dados
</label>
```

## Inputs

```html
<input type="" placeholder="legenda" name="">
<input type="" placeholder="legenda" name="" required>
```

**placeholder=**

* É o texto exibido dentro do elemento input antes da inserção de texto por parte do usuário.

**required=**

* Torna o campo como preenchimento obrigatório.

**type=**

* `button` Botão

* `checkbox` Caixa de seleção (múltipla escolha)

* `color` Seletor de cores

* `date` Seletor de data

* `datetime` 

* `datetime-local` 

* `email` É necessário ter formato de email (com @)

* `file` Seletor de arquivo (necessário definir as extensões aceitas)

* `hidden` Input não é visível no site

* `image` Seletor de imagens (necessário definir as extensões aceitas)

* `month` Seletor de meses

* `number` Aceita somente números

* `password` Os dígitos não ficam visíveis (aparecem • ou \*)

* `radio` Caixa de seleção (escolha única)

* `range` Tamanho

* `reset` Reseta as informações digitadas no formulário

* `search` Campo de busca

* `tel` Formato para número de telefone

* `text` Aceita uma linha de texto

* `time` Seletor de hora

* `url` Seletor de links

* `week` Seletor de semanas

* [Inputs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/input "inputs")

## Botões

```html
<button type="submit"> Texto do Botão </button>
```

**type=**

* `"submit"` envia os dados das entradas

* `"reset"` apaga os dados preenchidos

* `"button"` botão para outras funcionalidades

## Resposta de múltipla-escolha (checkbox e radio)

```html
<label> Uma resposta dentre várias
  <input type="radio" name="nome" value="valor1" checked> Resposta 1
</label>
```

**name=**

Todos os `<input>` correspondentes a uma mesma pergunta devem ter o mesmo `name`;

**type=**

* `"radio"` uma única resposta

* `"checkbox"` múltiplas respostas

**value=**

* Os inputs do tipo radio e checkbox têm seus valores identificados a partir do atributo value. No banco de dados,  `name` receberá os dados do `value` definido no input escolhido pelo er. Se você omitir *value*, *name* receberá o valor *on*, portanto value precisa de um valor que identifique a resposta.

**checked**

* Deixa a opção selecionada por padrão (opcional)

**for=**

* Defina o atributo *for* em `<label>` com o valor do *id* do elemento `<input>` permite que tecnologias assistivas criem uma relação entre os dois:

```html
<label for="associador"> 
  <input id="associador" type="checkbox" name="nome" value="valor1"> Resposta 1
</label>
<label for="associador">
  <input id="associador" type="checkbox" name="nome" value="valor2"> Resposta 2
</label>
```

## Caixas de seleção (dropdown)

```html
<label>Dropdown</label>
<select id="senioridade">
  <option value="" selected disabled>Selecione</option>
  <option> Opção1 </option>
  <option> Opção2 </option>
  <option> Opção3 </option>
</select>
```

**selected** é a primeira opção que aparece selecionada;

**disabled** é uma opção não selecionável;

**value=** colocamos em branco na unidade não selecionável.

## Campo de texto

```html
<textarea row="X" placeholder="legenda"> Caso queira algo já digitado dentro da área, insira aqui. O usuário poderá substituir pelo próprio conteúdo. </textarea>
```

* **row=** Insira X linhas de espaço.

* **placeholder=** É o texto exibido dentro do elemento input antes da inserção de texto por parte do usuário.


## Atributos
* `min="X"`, `max="Y"` e`step="Z"`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Os atributos min e max especificam o intervalo mínimo e máximo.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ O atributo step é usado para definir os incrementos que serão aceitos em uma entrada.

* `maxlength="valor"` número máximo de caracteres aceitos no campo.

* `multiple` permite ao usuário inserir vários valores nesse campo separando por vírgulas.

* `checked` define qual botão de opção ou caixa de seleção já está marcado quando o formulário é exibido.

* `placeholder` é usado para fornecer textos dentro de um campo de formulário indicando o que o usuário deve fazer.

* `pattern="[A-Za-z]{4}"` o atributo `pattern` é usado para definir o requisito para os caracteres exatos que podem ser inseridos em um campo.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;⤷ Acima definimos que o campo só vai ser enviado se conter 4 letras alfabéticas, aceita maiúsculas e minúsculas.

* `required` o campo deve ser preenchido antes que o formulário possa ser enviado.

* `aria-required="true"` é usado para dizer aos leitores de tela que um campo é necessário, se eles não suportam o atributo requerido.

* `disabled` significa que nenhum dado pode ser inserido e também os dados não serão enviados

* `readonly` significa que nenhum dado pode ser inserido, mas o valor previamente definido será enviado.

* `accept="image/*"` usado para o `type="file"`, especifica quais tipos de arquivos são permitidos. Você especifica um JPG, GIF, PNG e etc.

___

**Modelo:**

```html
<form>
  <fieldset>
    <legend>Login</legend>
    <label for="email">E-mail: </label>
    <input type="text" id="email" name="email">
     <br>
    <label for="senha">Senha:  </label>
    <input type="password" id="senha" name="senha">
  </fieldset>
  <fieldset>
    <legend>Desenvolvimento</legend>
      <label for="email">Qual aplicação você desenvolve:</label>
      <label for="dev">
        <input type="radio" id="dev" name="dev" valor="back"> Back-end
      </label>
      <label for="dev">
        <input type="radio" id="dev" name="dev" valor="front"> Front-end
      </label>
      <label for="dev">
        <input type="radio" id="dev" name="dev" valor="full"> Full-stack
      </label>
      <label>Senioridade</label>
      <select id="senioridade">
        <option selected disabled value="">Selecione</option>
        <option> Trainee </option>
        <option> Júnior </option>
        <option> Pleno </option>
        <option> Sênior </option>
      </select>
  </fieldset>
  <button>Submit</button>
</form>
```