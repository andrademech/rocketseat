# Anotações de aula

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

- content-box|border-box

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
|--------------------------------|--------------------------------|
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


