# LISTAS

[CSS: listas]()

## Tipos de lista

```html
<ul> unordered list
  <li> item 1 </li>
  <li> item 2 </li>
</ul>

<ol> ordered list
  <li> item 1 </li>
  <li> item 2 </li>
</ol>

<dl> definition list
  <dt> item 1 </dt>
  <dd> description of item 1 </dd>
  <dt> item 2 </dt>
  <dd> description of item 2 </dd>
</dl>
```

* Não é mais obrigatório o uso da tag `</li>`, mas para fins de organização é recomendado seu uso;

## Lista ordenada

```html
<ol type="1" start="4"> ordered list
  <li> item 1 </li>
  <li> item 2 </li>
</ol>
```

* **type:** 1 *(default)* | a *(letras minúsculas)* | A *(letras maiúsculas)* | i *(romanos em minúsculas)* | I *(romanos em maiúsculas)*
* **start:** Número no qual começa a lista;

## Lista não-ordenada

```html
<ul type="disc"> unordered list
 <li> item 1 </li>
 <li> item 2 </li>
</ul>
```

* **type:** disc (•) | circle (૰) | square (🢝)

## Lista de definição

```html
<dl> definition list
  <dt> termo 1 </dt>
  <dd> description 1 </dd>
  <dt> termo 2 </dt>
  <dd> description 2 </dd>
</dl>
```

## Junção de listas

```html
<ol> Lista Ordenada
  <li> Item
    <ul> Lista Não-Ordenada
      <li> Subitem </li>
    </ul>
  </li>
</ol>
```