---
title: Integrando na Web
type: imeplayer
layout: docs
parent_section: imeplayer
order: 2
---

> Esse guia tem como objetivo auxiliar na integração do **Ime Player**  em uma **página** ou **aplicativo Web**. Esse guia é primariamente destinado à **administradores de sistemas** e o conhecimento básico de HTML e CSS é um requisito.


## Iniciando a integração

Para integrar o Ime Player em seu html, você deverá incluir o seguinte trecho dentro do `<body>`:

```html
<iframe
  id="player"
  width="100%" height="360"
  style="border: 0"
  allow="xr-spatial-tracking,gyroscope,accelerometer,fullscreen"
  src="https://player.imersys.com/video/366335646"
>
</iframe>

```


Pronto! Uma característica importante do Ime Player é que a integração ocorre sem a necessidade de instalações. Ou seja, uma vez você aplique o trecho de código a cima em seu aplicativo ou página Web a visualização será a seguinte:

<iframe
      id="player"
      width="100%" height="360"
      style="border: 0"
      allow="xr-spatial-tracking,gyroscope,accelerometer,fullscreen"
      src="https://player.imersys.com/video/366335646">
</iframe>

## Configuração

### Fullscreen

Uma característica importante nos vídeos 360 graus é a visualização imersiva, mesmo quando não utilizado um headset de Realidade Virtual. Então muito provavelmente você vai querer integrar o Ime Player em sua aplicação cobrindo toda tela do seu dispositivo no modo fullscreen. Para isso será necessário definir alguns parâmetros na folhas de estilos CSS. Por exemplo:

```html
<html>
<head>
  <style>
    body {
      overflow: hidden;
    }
    .player {
      position: absolute;
      border: 0;
      top: 0;
      left: 0;
    }
  </style>
</head>
<body>
  <iframe
    id="player"
    class="player"
    height="100%" width="100%"
    allow="xr-spatial-tracking,gyroscope,accelerometer,fullscreen"
    src="https://player.imersys.com/video/366335646">
  </iframe>
</body>
</html>
```

### Mobile (Android, iOS)

Outra característica desejada é a visualização de vídeos nos dispositivos mobile. Então não se esqueça também de adicionar o parâmetro `meta` dentro do `<head>` (para que a visualização seja na escala compatível com o tamanho da tela do seu dispositivo) e o script `imeplayer-embed`.

```html
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body {
      overflow: hidden;
    }
    .player {
      position: absolute;
      border: 0;
      top: 0;
      left: 0;
    }
  </style>
</head>
<body>
  <iframe
    id="player"
    class="player"
    height="100%" width="100%"
    allow="xr-spatial-tracking,gyroscope,accelerometer,fullscreen"
    src="https://player.imersys.com/video/366335646">
  </iframe>
  <script defer src="//unpkg.com/imeplayer-embed@latest/dist/embed.js"></script>
</body>
</html>
```

### Chaves de autenticação

Em breve...

## Agora é com você!

Qualquer dúvidas que você tenha na integração, a equipe da Imersys estará super disposta a ajudar. Envie um e-mail para suporte@imersys.com.