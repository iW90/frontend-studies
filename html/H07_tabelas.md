# TABELAS

[CSS: tabelas]()

## TABELA SIMPLES

```html
<table> table (tabela)
  <tr> table row (linha da tabela) linha 1
    <td> table data (dados da tabela) coluna 1 </td>
    <td> table data (dados da tabela) coluna 2 </td>
  </tr>
  <tr> table row (linha da tabela) linha 2
    <td> table data (dados da tabela) coluna 1 </td>
    <td> table data (dados da tabela) coluna 2 </td>
  </tr>
</table>
```

* As tags de encerramento </tr> e </td> não são mais obrigatórias, mas utiliza-se para fins de organização.

## Tabela completa

```html
<table>
  <caption> Legenda no Topo </caption>

  <thead> Cabeçalho
    <tr> Linha 1
      <th> Título da coluna 1 </th>
      <th> Título da coluna 2 </th>
    </tr>
  </thead>

  <tbody> Corpo
    <tr> Linha 2
      <td> Dado da Coluna 1 </td>
      <td> Dado da Coluna 2 </td>
    </tr>
    <tr> Linha 3
      <td> Dado da Coluna 1 </td>
      <td> Dado da Coluna 2 </td>
    </tr>
  </tbody>

  <tfoot> Rodapé
    <tr> Linha 4
      <th> Título na Coluna 1 </th>
      <td> Dado da Coluna 2 </td>
    </tr>
  </tfoot>

</table>
```

## Mesclagem de células

Ocupar mais de uma coluna:

```html
<tr>
  <td> L1, C1 </td>
  <td colspan="3"> L1, C2-C3-C4 </td>
  <!-- Apagar os td seguintes da mesma linha -->
  <!-- Apagar os td seguintes da mesma linha -->
</tr>
```

Ocupar mais de uma linha:
```html
<tr>
  <td rowspan="2"> C1, L1-L2 </td>
  <td> C2, L1 </td>
  <td> C3, L1 </td>
</tr>
<tr>
  <!-- Apagar o td seguinte da mesma coluna -->
  <td> C1 </td>
  <td> C1 </td>
</tr>
```

* O número do `rowspan` e do `colspan` é a quantidade de células que serão ocupadas. É necessário apagar os <td> que ocupariam a posição mesclada.

## Escopo

Não tem diferença visual, é apenas por semântica (acessibilidade):

```html
<th scope="col"> título de uma coluna de dados
<th scope="row"> título de uma linha de dados

<th scope="colgroup"> título (mesclado) de mais de uma coluna de dados 
<th scope="rowgroup"> título (mesclado) de mais de uma linha de dados
```

## Formatação de linhas e colunas

Insira <colgroup> no início do código para agrupar colunas.

```html
<colgroup>
  <col id="coluna1"> Coluna 1. Use a ID do <col> para formatar uma coluna
  <col id="coluna2e3" span="2"> Colunas 2 e 3. O span="2" é a quantidade de colunas mescladas.
  <col id="coluna4"> Coluna 4
</colgroup>

<tr id="NomeDaLinha"> Use a ID do <tr> para formatar uma linha
```

* Insira `<colgroup>` no início do código da tabela para isolar colunas, cada `<col>` representa uma coluna.

* Use `<col span="x">` sendo **x** o número de colunas a serem agrupadas.