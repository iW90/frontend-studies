# TAGs HTML

## **METADADOS**

[HEAD TUTORIAL]()

```html
<head> Cabeça, dentro deste elemento são inseridos os metadados do documento
  <title> Título do documento, mostrado na aba do navegador </title>
  <link> Linka a recursos externos, como style.css, favicon.ico, etc.
  <style> Espaço para inserir formatação CSS </style>
  <script> Espaço para inserir JavaScript, também usado fora de "head" </script>
  <base> Especifica o URL por todos os endereços relativos do documento
  <meta> Metadados que não são definidos por outros elementos (base, link, script, style ou tittle)
</head>
```

## GROUPING TAGS

Funcionam como "blocos":

![grouping-tags](/imagens/grouping.png "Grouping tags")

```html
<header> Cabeçalho </header>
<nav> Barra de Navegação </nav>
<main> Conteúdo </main>
<footer> Rodapé </footer>

<section> Seção </section>
<article> Artigo </article>
<aside> Extra </aside>

<div> Bloco sem semântica </div>
<hr> Linha horizontal que representa uma quebra de temas
```

## CONTEÚDO TEXTUAL

[LINKS TUTORIAL]()

```html
<a> link </a>
```

```html
<p> Parágrafo </p>
<br> Quebra de linha

<em> Ênfase (itálico) </em>
<strong> Destaque (bold) </strong>
<mark> Efeito marca-texto </mark>
<small> Letras pequenas </small>
<del> Texto deletado </del>
<ins> Texto inserido </ins>
<s> Texto errado ou rasurado </s>
<dfn> Definição (marca o termo que será definido) </dfn>
<abbr> Abreviação (pontilha embaixo e exibe o significado ao parar o mouse sobre a palavra </abbr>

<sub> Texto subescrito (H₂O) </sub>
<sup> Texto sobrescrito (x²) </sup>

<q> Citação simples (sem quebras de linha, insere aspas) </q>
<cite> Citação (fragmento de outro texto) </cite>
<blockquote> Citação em bloco </blockquote>

<address> Informa que é um endereço (telefone, url, etc.) </address>
<time datetime="aaaa-mm-dd"> Informa que é uma data </time>
<data value="código do dado"> Usada para adicionar uma tradução legível por uma máquina </data>

<code> Códigos de computador </code>
<pre> Pré-formatação: os espaços, quebras de linha e tabulações são considerados </pre>
<samp> Output de uma execução, deixa o texto monoespaçado </samp>
<kbd> Keyboard (tecla), deixa o  texto monoespaçado </kbd>
<var> Variável matemática </var>

<meter> Barrinha de escala </meter>
<progress> Barrinha de progresso </progress>

<details> ⯈ Um container de texto
  <summary> ⯈ Título do container </summary>
  <p> Texto que aparece ao abrir (clicando) o container </p>
</details>

<dialog open> Janela de diálogo (flutua) </dialog>

<ruby> Legenda para caracteres asiáticos
  <rp> Parênteses em torno da pronúncia </rp>
  <rt> Pronúncia </rt>
  <rp> Parênteses em torno da pronúncia </rp>
</ruby>

<bdo dir="rtl | ltr"> Bidirectional Override: Altera a direção do texto. </bdo>
```

## IMAGEM E MULTIMÍDIA

```html
<img> Insere uma imagem

<figure> Imagens, diagramas, fotos, imagens 
  <figcaption> Legenda </figcaption>
</figure>
```

[IMAGENS TUTORIAL]()

```html
<picture> Um container para múltiplas imagens (usado para design responsivo) 
  <source> Alternativa </source>
</picture>
``` 

[MAPEAMENTO TUTORIAL]()

```html
<map> Define um mapa em uma imagem
  <area> Torna clicável uma área </area>
</map>
```

[MULTIMÍDIAS TUTORIAL]()

```html
<audio> Um container para múltiplos áudios (usado para design responsivo)
  <source> Alternativas </source>
</audio>

<video> Conteúdo de vídeo
  <track> Usado para legendas </track>
</video>
```

# TABELAS

[TABELAS TUTORIAL]()

```html
<table>

  <caption> Legenda no Topo </caption>

  <colgroup> Agrupamento de colunas
    <col> Coluna
  </colgroup>

  <thead> Cabeçalho
    <tr> Linha
      <th> Título</th>
    </tr>
  </thead>

  <tbody> Corpo
    <tr> Linha
      <td> Informação (coluna) </td>
    </tr>
  </tbody>

  <tfoot> Rodapé
    <tr> Linha
      <td> Informação </td>
    </tr>
  </tfoot>

</table>
```

## CONTEÚDO INTEGRADO

```html
<embed>  </embed>
<iframe>  </iframe>
<object>  </object>
<param>  </param>
<portal>  </portal>
```

## FORMULÁRIOS

[FORMULÁRIOS TUTORIAL]() 

```html
<form> Envia dados do input a um servidor
  <fieldset> Seus elementos filhos são um conjunto
    <legend> Legenda do conjunto </legend>
    <label> Respostas de múltipla escolha
      <input> Campo de inserção de dados
      <textarea> Box de Texto </textarea>
    </label>
    </fieldset>
    <button> Botão que executa ação </button>
  </form>
```

## OUTRAS

```html
<!DOCTYPE html> Informa que a página utiliza a versão HTML5 (para navegadores antigos, recomendável deixar "doctype" em maiúsculas.
<!-- Comentário -->
<script> Inserere JS </script>
<noscript> You need to enable JavaScript to view the full site. </noscript>
```