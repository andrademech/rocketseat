# *Anotações de aula*

- Aceso a [Trilha Fundamentar](https://github.com/andrademech/rocketseat/tree/main/Fundamentar)

# AULA 01

# Cores
Usamos CSS para alteras cores do nosso documento.

## Tipos

* background-color (para caixas)
* color (para textos)
* border-color (para caixas)
* outros...

## Valores

Podemos definir valores por:

* palavra-chave (blue, transparent)
* hexadecimal (#990011)
* funções: rgb, rgba, hsl, hsla

```css
element {
    /* Keyword values */
    color: currentcolor;

    /* <named-color> values */
    color: red;
    color: orange;
    color: tan;
    color: rebeccapurple;

    /* <hex-color> values 0-F */
    color: #090; /* RED GREEN BLUE */
    color: #009900;
    color: #090a;
    color: #009900aa;

    /* <rgb()> values */
    color: rgb(34, 12, 64, 0.6); /* 0-255 */
    color: rgba(34, 12, 64, 0.6);
    color: rgb(34 12 64 / 0.6);
    color: rgba(34 12 64 / 0.3);
    color: rgb(34.0 12 64 60%);
    color: rgba(34.6 12 64 / 30%);

    /* <hsl()> values */
    color: hsl(30, 100%, 50%, 0.6); /* Hue - Saturation - Luminance */
    color: hsla(30, 100%, 50%, 0.6);
    color: hsl(30 100% 50% / 0.6);
    color: hsla(30 100% 50% / 0.6);
    color: hsl(30.0 100% 50% / 60%);
    color: hsla(30.2 100% 50% / 60%);

    /* Global values */
    color: inherit; /* Herda a cor do elemento anterior */
    color: initial; /* Volta a sua cor inicial */
    color: unset; /* Pega a cor do contexto */
}

```

# AULA 02

## Background

- Define um fundo para nosso elemento
- Sua área de atuação é a caixa toda
- Por padrão, é transparente

### Exemplos

- Usar cores solidas
- Usar imagens
- Controlar
    - a posição das imagens
    - se elas se repetem ou não
    - o tamanho delas na caixa
- Usar cor e imagem juntas
- Usar cor gradiente

### Background-image-repeat

```css
div {
    /* Values */

    background-repeat: repeat-x;
    background-repeat: repeat-y;
    background-repeat: repeat;
    background-repeat: space;
    background-repeat: round;
    background-repeat: no-repeat;

    /* Podedmos usar 2 valores: horizontal | vertical */
    background-repeat: repeat space;
    background-repeat: repeat repeat;
    background-repeat: round space;
    background-repeat: no-repeat round;
} 
```

### Background-position

```css
div {
    /* Pricipais valores */
    background-position: top;
    background-position: bottom;
    background-position: left;
    background-position: right;
    background-position: center;
}
```
### Background-size

```css
div {
    /* Values */
    background-size: cover;
    background-size: contain;

    /* Podemos usar 2 valores, o primeiro é para a largura da imagem e o segundo é para a altura */
    background-size: 40% auto;
    background-size: 2em 25%;
    background-size: auto 8px;
    background-size: auto auto;
}
```
### Background-origin-clip

A propriedade background-origin é quem define o ponto de origem de uma imagem específica.
```css
div {
    /* Principais valores */
    background-origin: border-box;
    background-origin: padding-box;
    background-origin: content-box;
}
```


O background-clip define se a cor ou imagem do background iniciam debaixo de sua área de borda, preenchimento ou conteúdo.

```css
div {
    /* Principais valores */
    background-clip: border-box;
    background-clip: padding-box;
    background-clip: content-box;
    background-clip: text;
}
```

### Background-attachment

```css
div {
    /* Principais valores */
    background-attachment: scroll;
    background-attachment: fixed;
    background-attachment: local;
}
```
### Gradient

linear-gradient( ) é a função usada para criar gradient linear com o CSS.
```css
div {
    background: linear-gradient(45deg, red, yellow);
}
```
radial-gradient( ) é a função usada para criar gradient circular.

```css
div {
    background: radial-gradient(green, red, yellow);
    background: radial-gradient(rgba(255, 255, 255, 0), rgba(255, 0, 0, 0.2));
}
```

