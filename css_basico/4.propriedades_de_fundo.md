# PROPRIEDADES DE FUNDO

As propriedades de fundo permitem a personalização do plano de fundo dos elementos da página. A seguir, estão as principais propriedades disponíveis em CSS:

* ```background-color```: define a cor de fundo do elemento;
    * ```background-color: #fff```
* ```background-image```: define uma imagem como plano de fundo;
    * ```background-image: url("link")```
* ```background-repeat```: define como a imagem de fundo será repetida;
    * ```no-repeat```: não repete;
    * ```repeat```: repete nas duas direções;
    * ```repeat-x```: repete horizontalmente;
    * ```repeat-y```: repete verticalmente.
* ```background-position```: define a posição da imagem de fundo dentro do elemento. É possível informar dois valores, referentes aos eixos X (horizontal) e Y (vertical). Caso ambos sejam iguais, um único valor é suficiente;
    * Valores comuns: ```top```, ```bottom```, ```left```, ```right``` e ```center```. **Left** e **right** estarão ao centro, mas deslocados para a respectiva direção. **Valores em pixels ou porcentagens** também são aceitos.
* ```background-size```: define o tamanho da imagem de fundo;
    * ```cover```: cobre todo o elemento;
    * ```contain```: mantém a proporção da imagem;
    * Valores em pixels ou porcentagens são aceitos também.
* ```background-attachment```: define se a imagem de fundo se move com o conteúdo ou permanece fixa;
    * ```scroll```: se move com o conteúdo;
    * ```fixed```: permanece fixa.

## Propriedades abreviadas (shorthand)

É possível abreviar todas as propriedades de fundo em uma única declaração utilizando a propriedade ```background```. Os valores são escritos em sequência, separados por espaços e sem vírgulas. Por exemplo:

```
background: #fff url("imagem.jpeg") no-repeat center
```

---