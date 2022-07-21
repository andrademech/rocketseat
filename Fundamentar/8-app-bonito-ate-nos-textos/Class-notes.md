# Anotações de aula

- [X] [Trilha Fundamentar](https://github.com/andrademech/rocketseat/tree/main/Fundamentar)

# Trabalhando com fontes

Tipografia transmite mensagem

- mensagem
- tamanho
- estilo

--------
## Basic Font Propoerties

* font-family
* font-weight
* font-style
* font-size

----------
## Font Family

* Tipo de fonte de um elemento
* Lista de fontes e ordem de priridade
* Inclui *fallback* font

```css
p {
    font-family: "Times New Roman", Times, serif;
}
```

- serif
- sans
----------
## Font Weight

* Peso da fonte
```css
p {
    font-weight: bold;
}
```

## Font Style

* Estilo da fonte

```css
p {
    font-style: italic;
}
```
----------

## Font Size

* O tamanho da fonte

```css
p {
    font-size: 18px;
}
```

## Web fonts

- fontes do sistema x fontes web
- como usar fontes para we?

    * @font-face
    * @import
    * link

## font-variant

* variações na apresentação fonte

```css
p {
    font-variant: small-caps;
}
```
## font-stretch

* alargamento ou encolhimento da fonte
* aceita palavra-chave como: expanded, condensed, normal
* aceita porcentagens de 50 a 200%

```css
p {
    font-stretch: expanded;
}
```

## letter-spacing

* Espaços entre caracteres

```css
p {
    letter-spacing: 4px;
}
```

## word-spacing

* Espaços entre palavras

```css
p {
    word-spacing: 4px;
}
```
