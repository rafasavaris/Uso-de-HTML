# O que é CSS?

CSS significa **Cascading Style Sheets** (Folhas de Estilo em Cascata) e foi criado para a estilização de páginas HTML. À medida que as páginas web evoluíram, surgiu a necessidade de torná-las visualmente mais atraentes. Inicialmente, foram criadas tags de estilização dentro do próprio HTML, o que fez com que a linguagem de marcação acumulasse duas funções: estruturação e estilização.

No entanto, essa mistura causou problemas como a falta de padronização e a dificuldade de manutenção do código. Para resolver isso, surgiu o CSS, que **separa a estrutura do design** e permite a **reutilização de estilos**.

## Função do CSS

A principal função do CSS é separar o conteúdo (HTML) da sua apresentação visual. Ele define como os elementos devem ser exibidos, permitindo inclusive que uma mesma página seja apresentada de formas diferentes dependendo do dispositivo (como monitores, tablets ou celulares).

## Sintaxe

O CSS funciona através de **regras** aplicadas aos elementos HTML. Cada regra é composta por um **seletor** e um **bloco de declaração**. Dentro das chaves, definimos as **propriedades** e seus respectivos **valores**.

Cada propriedade é um par chave-valor, em que a chave corresponde a caracteristica da propriedade e o valor corresponde a como essa característica será aplicada. Uma propriedade no CSS aparece com o seu nome e o seu valor separados pelo caractere dois pontos (:). Após o valor de cada propriedade, deve-se colocar ponto e vírgula.

Por fim, é importante notar duas coisas no CSS:

* Em uma regra CSS, mais de uma propriedade pode ser escrita;
* O navegador lê as regras CSS de cima para baixo, assim, caso existir uma duplicação de propriedade, somente a última será considerada.

Abaixo, está um exemplo de regra CSS para a tag &lt;h1&gt;.

```css
h1 {
    background-color: white;
    color: black;
    padding: 10px;
}
```

* **Seletor**: h1 (indica que todos os elementos &lt;h1&gt; receberão este estilo);
* **Propriedades**: background-color, color e padding;
* **Valores**: white, black e 10px.

## Comentários

Para inserir comentários no CSS, basta colocar o texto entre /* e */. Esses trechos serão ignorados.

## CSS no HTML

Existem três maneiras de incluir CSS em um projeto. Elas possuem uma ordem de prioridade (hierarquia), onde o estilo mais específico costuma prevalecer sobre o mais geral.

### CSS inline

Aplicado diretamente na tag HTML através do atributo style. É a forma com maior prioridade, mas dificulta a manutenção, pois não permite a reutilização global de estilos.

```html
<p style="background-color: white; color: black; padding: 10px">Este é um parágrafo!</p>
```

O problema desse tipo de CSS é que é necessário repetir o mesmo estilo em várias tags se quiser, não é algo global.

### CSS embutido

Os estilos são definidos dentro da tag &lt;style&gt;, geralmente localizada no &lt;head&gt; do documento. É útil para estilos específicos de uma única página.

```html
<head>
    ...
    <style>
        h1{
            background-color: white;
            color: black;
            padding: 10px;
        }
    </style>
</head>
```

### CSS externo

É o método mais utilizado e recomendado. Os estilos são escritos em um arquivo separado com a extensão **.css** e vinculados ao HTML através da tag &lt;link&gt;. Isso permite que uma única folha de estilo controle o design de várias páginas simultaneamente.

```html
<head>
    ...
    <link ref="stylesheet" href="./estilos.css">
</head>
```

<details>
    <summary>Tag &lt;link&gt;</summary>
    <p>
        A tag <strong>&lt;link&gt;</strong> serve para estabelecer uma conexão entre o documento HTML e recursos externos. Ela é uma tag vazia, inserida obrigatoriamente dentro do <code>&lt;head&gt;</code>.
    </p>
    <p>Seus principais atributos são:</p>
    <ul>
        <li><strong>rel:</strong> (Relationship) Define a relação do arquivo com a página (ex: <code>stylesheet</code> para CSS ou <code>icon</code> para o ícone da aba).</li>
        <li><strong>href:</strong> (Hypertext Reference) Indica o caminho ou URL do arquivo que será carregado.</li>
        <li><strong>type:</strong> Define o tipo de formato do arquivo (ex: <code>text/css</code> ou <code>image/x-icon</code>).</li>
    </ul>
</details>

---