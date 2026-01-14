# BOX MODEL

Em uma página HTML, todos os elementos são renderizados como **caixas retangulares**, com largura e altura definidas. Esse entendimento é a base do **Box Model**, um modelo que descreve como o espaço ocupado por um elemento é calculado no layout da página.

Existem 4 propriedades presents no box model:
* Conteúdo;
* Margem (margin);
* Padding;
* Borda (border).

Essas quatro áreas definem a quantidade total de espaço que um elemento ocupa no documento.

## Margem = Margin

A propriedade ```**margin**``` define o espaço externo do elemento, ou seja, a distância entre ele e os outros elementos ao seu redor. Ela pode ser definida individualmente para cada lado ()```margin-top```, ```margin-right```, ```margin-bottom``` e ```margin-left```) ou de forma abreviada.

```css
.square {
    /* declaração explícita */
    margin-top: 10px;
    margin-right: 12px;
    margin-bottom: 10px;
    margin-left: 12px;

    /* declaração abreviada: top, right, bottom, left */
    margin: 10px, 12px, 10px, 12px;

    /* mesmo valor para todos os lados */
    margin: 12px;
}
```

Se a propriedade receber:

* 1 valor: aplica a todos os lados;
* 2 valores: primeiro para ```top/bottom```, segundo para ```left/right```;
* 3 valores: primeiro para ```top```, segundo para ```left/right``` e terceiro para ```bottom```;
* 4 valores: sentido horário a partir de ```top```, isto é, ```top```, ```right```, ```bottom``` e ```left```.

## Padding

O ```**padding**``` define o espaço interno do elemento, ou seja, a distância entre o conteúdo e a borda. Ele funciona da mesma forma que a propriedade margin.

```css
.square {
  /* declaração explícita */
  padding-top: 10px;
  padding-right: 12px;
  padding-bottom: 10px;
  padding-left: 12px;

  /* declaração abreviada */
  padding: 10px 12px 10px 12px;

  /* mesmo valor para todos os lados */
  padding: 12px;
}
```

## Borda = Border

A propriedade ```**border**``` cria uma borda ao redor do elemento. Ela pode ser definida por três valores principais:

* ```border-width```: espessura da borda (definida pelas medidas CSS);
* ```border-style```: estilo da borda (```solid```, ```dashed```, ```double```, ```dotted```, etc.);
* ```border-color```: cor da borda.

```css
.square {
    /* declarção explícita */
    border-width: 2px;
    border-style: solid;
    border-color: blue;

    /* declaração abrevida */
    border: 2px solid blue;
}
```

É possível aplicar espessura, estilo e cor diferentes para cada lado da borda utilizando propriedades específicas como ```border-top```, ```border-right```, ```order-bottom``` e ```border-left```.

```css
.box {
    border-top: 2px solid red;
    border-right: 4px dashed blue;
    border-bottom: 3px dotted green;
    border-left: 5px double orange;
}
```

As propriedades abreviadas ```border-width```, ```border-style``` e ```border-color``` seguem o mesmo padrão de abreviação das demais propriedades do CSS. No entanto, a propriedade abreviada ```border``` não permite variações por lado; ela aplica os mesmos valores a todas as bordas.

```css
.box {
    border-width: 2px 4px 3px 5px;
    border-style: solid dashed dotted double;
    border-color: red blue green orange;

    /* aplicando o mesmo estilo para todos os lados */
    border: 2px solid red;
}

```

Além disso, existe a propriedade ```border-radius```, que permite arredondar os cantos do elemento utilizando valores nas unidades do CSS. É possível definir valores diferentes para cada canto, de forma individual ou abreviada.

```css
.box {
    /* mesmo raio para todos os lados */
    border-radius: 12px;

    /* declaração abreviada */
    border-radius: 10px 20px 30px 40px;

    /* declaração explícita */
    border-top-left-radius: 10px;
    border-top-right-radius: 20px;
    border-bottom-right-radius: 30px;
    border-bottom-left-radius: 40px;
}
```

> O ```border-radius``` aceita valores em %, facilitando a criação de círculos e elipses.


## Outline

A propriedade outline adiciona um contorno externo ao elemento.
A principal diferença em relação à borda é que o outline não ocupa espaço no layout e não entra no cálculo do tamanho do elemento. É muito utilizada para foco e acessibilidade.

O outline aceita as 3 principais propriedades abaixo:

* ```outline-width```: espessura da borda (definida pelas medidas CSS);
* ```outline-style```: estilo da borda (```solid```, ```dashed```, ```double```, ```dotted```, etc.);
* ```outline-color```: cor da borda.

Ele também permite escrever de forma abreviada, mas não é possível definir diferentes espessuras para os lados ou ter raio.

```css
.square {
    /* declarção explícita */
    outline-width: 2px;
    outline-style: solid;
    outline-color: blue;

    /* declaração abrevida */
    outline: 2px solid blue;
}
```