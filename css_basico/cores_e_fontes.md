# CORES

Com o CSS, é possível definir as cores dos textos, do fundo de elementos ou até da página inteira. Para isso, utilizam-se principalmente as seguintes propriedades:

* ```color```: define a cor do texto;
* ```background-color```: define a cor de fundo.

Os valores dessas propriedades podem ser definidos de 4 formas principais: nomes de cores, hexadecimal, RGB e HSL.

## Nomes das cores

O CSS possui diversas cores já nomeadas, que podem ser usadas sem a necessidade de códigos. Alguns exemplos incluem cores básicas como white, black e blue, além de outras menos comuns, como tomato, gold e aqua.

> Para consultar a lista completa de cores nomeadas, é recomendado buscar referências oficiais do CSS.

### Cores em hexadecimal

O formato hexadecimal é a forma mais utilizada para definir cores no CSS. Ele consiste em uma sequência de 6 caracteres hexadecimais (de **0** a **9** e de **a** a **f**), precedidos pelo símbolo **#**. Nesse tipo de código:

* Os dois primeiros caracteres representam o vermelho (red);
* Os dois seguintes, o verde (green);
* Os dois últimos, o azul (blue).

Também existe uma forma reduzida com 3 caracteres, usada quando os **pares** são iguais. Alguns exemplos estão abaixo.

* #ffaacc = #fac - light pink
* #fff- white
* #000000 - black
* #ff0000 - red

### Cores em RGB

No formato RGB, a cor é definida por três valores numéricos, variando de 0 a 255, que representam, respectivamente, tons de vermelho (Red), verde (Green) e azul (Blue). Por exemplo:

* rgb(255, 255, 255) - white
* rgb(0, 0, 0) - black
* rgb(255, 0, 0) - red

### Cores em HSL

HSL é um modelo de cores no CSS baseado em:

* H (Hue/Matiz): a cor em si, de 0 a 360;
    * 0 = vermelho;
    * 120 = verde;
    * 240 = azul;
* S (Saturation/Saturação): intensidade da cor, de 0 a 100%;
* L (Lightness/Luminosidade): quão clara ou escura é a cor, de 0 a 100%.

Um exemplo é:

* hsl(0, 100%, 50%) - red

## Transparência

Em CSS, a transparência é controlada pelo canal alpha, que define o nível de opacidade de uma cor. A forma de aplicá-la varia conforme o modelo de cor utilizado:

<dl>
    <dt>Cores por **nome**</dt>
    <dd>
        Não permitem a aplicação direta de transparência. Para isso, é necessário utilizar modelos que suportem o canal alpha, como rgba() ou hsla().
    </dd>
    <dt>Cores em **RGB/HSL**</dt>
    <dd>
        Para adicionar transparência, utiliza-se o formato RGBA/HSLA, que adiciona o canal alpha ao RGB/HSL. O valor do alpha varia de 0 (totalmente transparente) a 1 (totalmente opaco).</dd>
    <dd>
        <code>rgba(0, 255, 0, 0.5)</code> e <code> hsla(120, 100%, 50%, 0.5)</code>
    <dd>
    <dt>Cores em **hexadecimal**<dt>
    <dd>
        A transparência é definida usando 8 dígitos, em vez de 6. Os dois últimos dígitos representam o valor do alpha. Também é possível usar a forma reduzida, com 4 dígitos, quando os pares de caracteres são iguais
    </dd>
    <dd>
        <code>#ff000088</code> ou <code>#f008</code>
    </dd>

</dl>

---

# TEXTOS

É possível personalizar os textos de diversas formas em CSS. Antes disso, é importante considerar algumas informações básicas:

* Os navegadores assumem, por padrão, que o tamanho base das fontes é 16px;
* Os títulos (```h1``` a ```h6```) vêm em negrito por padrão.

Com base nisso, é possível aplicar modificações e estilos às fontes de forma consciente e consistente.

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

> Os tamanhos padrões das principais tags nos navegadores mais comuns são:
> *  &lt;h1&gt;: 32px
> *  &lt;h2&gt;: 14px;
> *  &lt;h3&gt;: 18.72px;
> *  &lt;h4&gt;: 16px;
> *  &lt;h5&gt;: 13.28px;
> *  &lt;h6&gt;: 10.72px;
> *  &lt;p&gt;: 16px;

## Transformação do texto

É possível alterar a forma de exibição do texto sem precisar reescrevê-lo, utilizando a propriedade CSS ```text-transform```. Essa propriedade controla a capitalização das letras e aceita os seguintes valores: **uppercase, lowercase, capitalize e none (valor padrão)**. Um exemplo de uso é:

```css
h1 {
    text-transform: uppercase;
}
```

---

