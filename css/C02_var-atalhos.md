# ATALHOS EM VARIÁVEIS

## Criando o próprio padrão

```css
@import url('fonteimportada');

@font-face {
  font-family: 'Android';
  src: url('/caminho/otafonte.otf') format('opentype');
  font-weight: normal;
}

:root {
  --nomedacor1: #fffff1;
  --nomedacor2: #fffff2;
  --nomedacor3: #fffff3;

  --fonte-padrao: 'Arial', 'Verdana', 'Helvetica', 'sans-serif';
  --fonte-destaque: 'fonteimportada', 'cursive';
  --fonte-android: 'otafonte', 'cursive';
} 

* {
  color: var(--nomedacor1);
  font-family: var(--fonte-padrao);
}
```