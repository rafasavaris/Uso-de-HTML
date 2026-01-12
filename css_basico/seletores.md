# O que são seletores?

Os seletores são a base do CSS. Eles definem exatamente quais elementos do HTML serão estilizados. Os seletores podem ser de 3 tipos, sendo eles: tag, classe ou id.

## Tag

Este seletor aplica o estilo a todas as tags de um mesmo tipo em toda a página. É ideal para definições globais, como o tipo de fonte de todos os parágrafos. O exemplo abaixo mostra uma estilização da tag &lt;p&gt;.

```css
p {
    background-color: pink;
}
```

Para aplicar um estilo a todos os elementos da página de uma só vez, utilizamos o Seletor Universal, representado pelo símbolo asterisco (*).

## Classe

O seletor de classe é usado quando queremos aplicar o mesmo estilo a diferentes elementos, independentemente da tag. Uma mesma classe pode ser usada em vários elementos da página. Para usar, coloque um ponto (.) antes do nome da classe.

No HTML: 

```html
<h1 class="destaque">
```
No CSS:

```css
.titulo {
    font-size: 10px;
    color: white;
}
```

## ID

Diferente da classe, o ID é único. Ele deve ser usado para identificar um elemento exclusivo na página (como um menu de navegação ou um rodapé específico). O navegador prioriza o ID sobre a classe e a tag. Para usar, coloque uma cerquilha/hashtag (#) antes do nome do ID.

No HTML: 

```html
<h1 id="cabecalho-principal"> Titulo!!! </h1>
```

No CSS:

```css
#tituloPrincipal {
    color: red;
}
```

---

## Combinações

É possível combinar o estilo de vários elementos sem depender de tag, classe ou id. Para isso, utilizamos as combinações no próprio CSS. Além disso, é possível especificar mais o estilo de um determinar elemento.

### Multiplos seletores

Quando vários elementos devem compartilhar exatamente a mesma estilização, podemos agrupá-los separando os seletores por vírgula. É possível agrupar os 3 tipos de seletores.

```css
.texto, div, #titulo {
    padding: 10px;
    color: red;
}
```

### Seletor combinado

Alguns elementos HTML possuem múltiplas classes ou uma combinação de classe e ID. Para selecionar um elemento que possua todas as condições simultaneamente, escrevemos os seletores juntos, sem espaço. Se houver espaço, o navegador entenderá como uma relação de pai e filho. Isso também funciona para combinações de tag e classe.

```html
<p class="texto normal">Texto normal!</p>
<p class="texto negrito">Texto negrito!</p>
```

```css
.texto.negrito {
    /* estilo */
}
```

### Filhos

O HTML possui uma estrutura hierárquica. O seletor de descendência aplica o estilo a um elemento que esteja dentro de outro, independentemente de quão "profundo" ele esteja na árvore. Para isso, usa-se apenas um espaço entre os seletores.

```css
div p {
    /* estilo de qualquer p dentro de qualquer div em qualquer nível de hierarquia*/
}
```

### Filhos diretos

Diferente do anterior, este seletor aplica o estilo apenas aos elementos que são filhos imediatos do pai (primeiro nível de hierarquia). É representado pelo símbolo >.

```css
div > p {
    /* estilo */
}
```

### Irmãos

O combinador ~ seleciona elementos que compartilham o mesmo pai e aparecem depois do elemento mencionado, mesmo que existam outras tags entre eles.

```css
/* Seleciona todos os <p> que venham após uma <div>, desde que estejam no mesmo nível */
div ~ p {
    color: gray;
}
```

### Irmão direto

O caractere + seleciona o elemento que é o irmão imediato, ou seja, que aparece exatamente após o primeiro elemento especificado, sem nada entre eles.

```css
/* Seleciona apenas o primeiro <p> que aparece logo após uma <div> */
div + p {
    margin-top: 20px;
}
```