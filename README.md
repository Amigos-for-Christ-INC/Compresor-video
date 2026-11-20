# Compresores de video

Herramientas que funcionan por completo en el navegador: los archivos no se suben a ningún servidor.

| Carpeta | Qué hace |
|---|---|
| `compresor-video/` | Comprime varios videos en cola (por peso objetivo, calidad o bitrate), con recorte, encuadre, rotación, velocidad y ajustes de imagen y sonido. También extrae solo el audio en MP3, WAV, M4A u Opus. Usa la identidad visual de Amigos for Christ. |
| `compresor-discord/` | Comprime un video para que quede por debajo del límite de Discord (20 MB por defecto). |

## Cómo usarlas

Abre el `index.html` de cada carpeta en Chrome o Edge en una computadora. Si el repositorio tiene GitHub Pages activado, quedan disponibles en:

- `https://<usuario-u-organización>.github.io/<repositorio>/compresor-video/`
- `https://<usuario-u-organización>.github.io/<repositorio>/compresor-discord/`

## Cómo funcionan

- El video se reproduce de forma oculta, se dibuja en un `canvas` y se vuelve a grabar con `MediaRecorder` al bitrate calculado. Por eso tarda más o menos lo que dura el video (salvo que se suba la velocidad).
- El audio en MP3 y WAV se decodifica con la Web Audio API y se codifica con [lamejs](https://github.com/zhuker/lamejs), sin reproducir el archivo completo.
- Dependencias por CDN: [JSZip 3.10.1](https://stuk.github.io/jszip/) y lamejs 1.2.1. Fuente: Raleway (Google Fonts).
- La pestaña debe quedar abierta y visible mientras se procesa un video.
