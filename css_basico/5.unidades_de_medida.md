# UNIDADE DE MEDIDAS NO CSS

As unidades de medida no CSS são fundamentais para definir o tamanho e o posicionamento dos elementos em uma página. Por isso, a escolha da unidade adequada é essencial para garantir responsividade, acessibilidade e manutenção do código. No CSS, as unidades de medida podem ser divididas em dois grandes grupos:

**1. Unidades Absolutas**

* **px (pixel)**: menor unidade visível. Representa um pixel na tela. É uma medida fixa e não se adpta ao tamanho da tela.
* **cm**, **mm**, **in**, **pt** (ponto), **pc** (pica): unidades físicas. Menos usadas pois a resolução das telas varia muito.

**2. Unidades Relativas**

* **%**: valor calculado em relação ao elemento pai, com base no espaço disponível;
* **em**: relativo ao tamanho da fonte do elemento pai. Útil para crar escalas de fontes;
* **rem**: relativo ao tamanho da fonte da raiz (root) do documento (geralmente o corpo). Permite criar escalas de fontes globais;
* **vw** (viewport width): relativo à largura da viewport (janela do navegador);
* **vh** (viewport height): relativo à altura da viewport.

## Tamanho de elementos

Para fontes, utilizar ```font-size``` combinada com uma das unidades acima. Para outros elementos, usam-se as propriedades ```height``` e ```width```, também com as unidades acima.

### Tamanhos mínimo e máximo

É possível limitar o crescimento ou a redução de um elemento utilizando:

* **Máximo:** ```max-height``` e ```max-width```;
* **Mínimo:** ```min-height``` e ```min-width```;

## Considerações finais

* Para layouts responsivos, prefira unidades relativas;
* Leve em conta acessibilidade e facilidade de manutenção do código;
* Utilize unidades relativas para construir uma hierarquia visual clara e consistente.

---