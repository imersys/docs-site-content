---
title: Integrando na Web
---

Esse guia tem como objetivo auxiliar na integração do **VR Player**  em uma **página** ou **aplicativo Web**. Esse guia é primariamente destinado à **administradores de sistemas** e o conhecimento básico de HTML é um requisito necessário.


## Iniciando a integração

Para integrar o VR Player, você deverá criar um arquivo .html e incluir o seguinte trecho `iframe` dentro do `<body>`:

```html
<html>
  <body>
    <iframe width="640" height="360"
            src="https://player.imersys.com/video/366335646"
            scrolling="no" frameborder="0">
    </iframe>
  </body>
</html>
```

Uma característica importante do VR Player é que a integração ocorre sem a necessidade de instalações. Ou seja, uma vez você aplique o trecho de código a cima em seu aplicativo ou página Web a visualização será a seguinte:

<iframe src="https://player.imersys.com/video/366335646"
        width="640" height="360"
        scrolling="no" frameborder="0">
</iframe>

## Configuração

### Fullscreen

Os navegadores não permitem que iframes fiquem fullscreen por padrão. Para permitir isso, portanto, o iframe precisa explicitamente a opção `allowfullscreen` (e para uma compatibilidade ainda maior com outros navegadores os desenvolvedores recomendam a prática de adicionar também as opções `webkitallowfullscreen` e `mozallowfullscreen`). Exemplo:

```html
<iframe allowfullscreen webkitallowfullscreen mozallowfullscreen
        width="640" height="360"
        src="https://player.imersys.com/video/366335646"
        scrolling="no" frameborder="0"
        allow="vr,gyroscope,accelerometer,fullscreen">
</iframe>

```

### Chaves de autenticação

Em breve...