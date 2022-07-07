# Anotações de aula

-  [Trilha Fundamentar](https://github.com/andrademech/rocketseat/tree/main/Fundamentar)

# Aula 01

# Box Model

- Fundamental para fazer layouts para a web
- Maior facilidade para aplicar o CSS

## O que é?

Uma caixa retangular.
Essa caixa possui propriedades de uma caixa (2D)

- Tamanho (largura x altura)    width | height
- Conteúdo                      content
- Bordas                        border
- Preenchimento interno         padding
- Espaços fora da caixa         margin

*Cada elemento na sua página, será considerado uma caixa.*

----------------------------------------------------------------

# Aula 02

## Box-sizing

Como será calculado o tamanho total da caixa?

- content-box | border-box

```css
div {
    box-sizing: border-box;
}
```
----------------------------------------------------------------

# Aula 03

## display: block vs display: inline

- Como as caixas se comportam em relação às outras caixas
- Comportamento externo das caixas

| **block**                      | **inline**                     |
|--------------------------------|--------------------------------|
| Ocupa toda a linha, colocando  | Elemento ao lado do outro      |
| o próximo elemento abaixo desse|                                |
|                                |                                |
| width e height são respeitados | width e height não funcionam   |
|--------------------------------|--------------------------------|
| padding, margin, border irão   | Somente valores horizontais de |
| funcionar normalmente.         | margin, padding e border       |
|--------------------------------|--------------------------------|

exemplos
block: `<p> <div> <section>`, todos os headings `<h1><h2>`
inline: `<a> <strong> <span> <em>`

----------------------------------------------------------------

# Aula 04

## Margin

Espaços entre os elementos

- margin-top | margin-right | margin-bottom | margin-left
- values: `<length>` | `<percentage>`| auto

*A sequência sempre é: top, right, bottom e left*

```css
div {
    /* shorthand */
    margin: 12px 16px 10px 4px; /*top, right, bottom e left*/
    margin: 12px 16px 0; /*top, right + left e bottom*/
    margin: 8px 16px; /* top + bottom e  right + left*/
    margin: 8px; /*todos os lados*/
}
```

*Cuidado com o margin collapsin (top se junta ao bottom)*

```css
div {
    border: 1px solid red;
    width: 100px;
    height: 100px;

    margin: 8px 0; /*margin padrão em 8px*/
}
```
*quando o elemento está ao lado do outro(display:inline), as margin se somam*

*quando o elemento está ao abaixo do outro (display:block), as margin não se somam*

----------------------------------------------------------------

# Aula 05

## padding

Padding vem do Inglês => preenchimento

Preenchimento interno da caixa

- padding-top | padding-right | padding-bottom | padding-left
- values: `<length>` | `<percentage>`

```css
div {
    /* shorthand */
    padding: 12px 16px 10px 4px; /*top, right, bottom e left*/
    padding: 12px 16px 0; /*top, right + left e bottom*/
    padding: 8px 16px; /* top + bottom e  right + left*/
    padding: 8px; /*todos os lados*/
}
```
*Padding poderá causar diferença na largura de um elemento*

----------------------------------------------------------------

# Aula 06

## border (e outline)

As bordas da caixa

- value: `<border-style>` | `<border-width>` | `<border-color>` | 
    - style: solid | dotted | dashed | double | groove | ridge | inset | outset
    - width: `<length>`
    - color: `<color>`

```css
div {
    /* shorthand */
    border-top: solid 2px; /* top | right | bottom | left */

    /* style */
    border: solid;

    /* width: `<length>` | style */
    border: 2px dotted;

    /* style | color */
    border: outset #f33;

    /* width | style | color */
    border: medium dashed green
}
```

### E outline?

O outline difere em 4 sentidos:
- Não modifica o tamanho da caixa, pois não é parte do Box Model
- Poderá ser diferente de retangular
- Não permite ajuste individual
- Mais usado pelo user agente para acessibilidade
