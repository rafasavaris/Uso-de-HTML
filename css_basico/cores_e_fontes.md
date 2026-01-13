# CORES

Com o CSS, é possível definir as cores dos textos, do fundo de elementos ou até da página inteira. Para isso, utilizam-se principalmente as seguintes propriedades:

* ```color```: define a cor do texto;
* ```background-color```: define a cor de fundo.

Os valores dessas propriedades podem ser definidos de três formas principais: nomes de cores, hexadecimal e RGB.

## Nomes das cores

O CSS possui diversas cores já nomeadas, que podem ser usadas sem a necessidade de códigos. Alguns exemplos incluem cores básicas como white, black e blue, além de outras menos comuns, como tomato, gold e aqua.

> Para consultar a lista completa de cores nomeadas, é recomendado buscar referências oficiais do CSS.

### Cores em hexadecimal

O formato hexadecimal é a forma mais utilizada para definir cores no CSS. Ele consiste em uma sequência de 6 caracteres hexadecimais (de **0** a **9** e de **a** a **f**), precedidos pelo símbolo **#**. Nesse tipo de código:

* Os dois primeiros caracteres representam o vermelho (red);
* Os dois seguintes, o verde (green);
* Os dois últimos, o azul (blue).

Também existe uma forma reduzida com 3 caracteres, usada quando os pares são iguais. Alguns exemplos estão abaixo.

* #fff- white
* #000000 - black
* #ff0000 - red

### Cores em RGB

No formato RGB, a cor é definida por três valores numéricos, variando de 0 a 255, que representam, respectivamente, tons de vermelho (Red), verde (Green) e azul (Blue). Por exemplo:

* rgb(255, 255, 255) - white
* rgb(0, 0, 0) - black
* rgb(255, 0, 0) - red

---

# TEXTOS

## Fontes

Em elementos textuais, é possível alterar a fonte a partir da propriedade ```font-family```. Essa propriedade recebe uma lista de fontes, separadas por vírgula, onde:

* A primeira é a fonte preferencial;
* Caso ela não esteja disponível, o navegador tenta a próxima;
* O processo continua até encontrar uma fonte válida.

Um exemplo pode ser visto abaixo.

```css
h1 {
    font-family: arial, helvetica, sans-serif;
}
```

> É uma boa prática finalizar a lista com **serif** ou **sans-serif**. Assim, caso nenhuma fonte específica esteja disponível, o navegador utilizará uma fonte padrão compatível com a família escolhida.

## Importando fontes

Existem duas formas principais de adicionar fontes externas em um arquivo CSS, ambas colocadas no topo de um arquivo ```.css```. Elas são:

```@font-face```: usado para importar fontes armazenadas no próprio servidor. Para utilizar:
```css
@font-face {
    font-family: myFont;
    src: url(font.woff)
}
```

```@import```: usado para importar fontes armazenadas na web. Seu uso é:
```css
@import url("link")
```

## Alinhamento de texto

Para alinhar textos dentro de um elemento, utiliza-se a propriedade ```text-align```. Os valores mais comuns são: **left, right, center e justify**. Por exemplo:

```css
p {
    text-align: center;
}
```

## Tamanho da fonte

O tamanho da fonte é definido pela propriedade ```font-size```, que aceita diversas unidades de medida do CSS. Por exemplo:

```css
p {
    font-size: 10px;
}
```

---

