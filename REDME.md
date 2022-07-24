# Aula Bootstrap
Comando para fazer download os links de uma página de referência pelo terminal
digitado na mesma pasta em que está o arquivo.
```bash

$ grep -o ‘https.*’ index,html
https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
```
```bash
$ grep -o  'https.*' index.html | sed 's/\".*//g'
```

	Dessa forma filtrou tudo que estava após as aspas duplas serão trocados por ‘nada’
https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css
https://code.jquery.com/jquery-3.2.1.slim.min.js
https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js
https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js

```bash
mkdir -p assets /{css,js,img}
```
para copiar o link direto 
```bash
$ wget -q  https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js
```

```html
<div class="container-fluid"> -fluid para ficar na página inteira

<div class="row"> separa a div em colunas

<div class="col-6">  O total é sempre 12 portanto de uma tiver 6 sobra 6

```

Conteúdo de largura variável

Use col-{breakpoint}-autoclasses para dimensionar colunas com base na largura natural de seu conteúdo.


1 de 3
Conteúdo de largura variável
3 de 3
1 de 3
Conteúdo de largura variável
3 de 3
cópia de
```html
<div class="container">
  <div class="row justify-content-md-center">
    <div class="col col-lg-2">
      1 of 3
    </div>
    <div class="col-md-auto">
      Variable width content
    </div>
    <div class="col col-lg-2">
      3 of 3
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col-md-auto">
      Variable width content
    </div>
    <div class="col col-lg-2">
      3 of 3
    </div>
  </div>
</div>

```

## sm = preferência para dispositivos moveis
## md = computadores
xl - tv

não informar nada… por default ele considerará sm
Como se a pǵina fosse feita ṕrimeiro para um celular e depois ela iria se ajustar

Quando a propriedade é uma das seguintes:
* m - para classes que definem margin
* p - para classes que definem padding
Onde lados é um dos seguintes:
* t- para classes que definem margin-topoupadding-top
* b- para classes que definem margin-bottomoupadding-bottom
* l- para classes que definem margin-leftoupadding-left
* r- para classes que definem margin-rightoupadding-right
* x- para classes que definem tanto *-lefte*-right
 * y- para classes que definem tanto *-tope*-bottom
* blank - para classes que definem um marginou paddingem todos os 4 lados do elemento
nde o tamanho é um dos seguintes:
* 0- para classes que eliminam o marginou paddingconfigurando-o para0
* 1- (por padrão) para classes que definem o marginou paddingpara$spacer * .25
* 2- (por padrão) para classes que definem o marginou paddingpara$spacer * .5
* 3- (por padrão) para classes que definem o marginou paddingpara$spacer
* 4- (por padrão) para classes que definem o marginou paddingpara$spacer * 1.5
* 5- (por padrão) para classes que definem o marginou paddingpara$spacer * 3
* auto- para classes que definem margincomo auto
(Você pode adicionar mais tamanhos adicionando entradas à $spacersvariável do mapa Sass.)

ícones da nav bar
https://fontawesome.com/v5.15/icons?d=gallery&p=2
## Colocar stylesheet como CDN
```html
<link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.13.0/css/all.css">
```
## pesquisar o ícone. Cliar em abrir em nova aba e copiar o código html
```html
<i class="fas fa-users"
```

