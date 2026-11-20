# Compresor de video

Herramienta de Amigos for Christ para comprimir videos y extraer audio. Funciona por completo en el navegador: los archivos no se suben a ningún servidor.

## Abrir la herramienta

**[Abrir el compresor de video](https://amigos-for-christ-inc.github.io/Compresor-video/)**

Funciona mejor en Chrome o Edge en una computadora. El enlace funciona cuando GitHub Pages está activado en el repositorio (Settings → Pages → Deploy from a branch → `main` / `(root)`).

También puedes descargar `compresor-video/index.html` y abrirlo con doble clic.

## Qué hace

- **Varios archivos en cola:** se procesan uno tras otro y se pueden guardar por separado o todos juntos en un `.zip`.
- **Tres modos de compresión:** peso objetivo en MB, nivel de calidad (alta, media, baja, mínima) o bitrate manual.
- **Formatos de video:** MP4 (H.264, H.265, AV1) y WEBM (VP9, VP8, AV1), según lo que permita el navegador.
- **Imagen:** resolución de 240p a 4K, de 15 a 60 fps, encuadre (16:9, 9:16, 1:1, 4:5, 4:3), rotación, espejo, brillo, contraste, saturación y blanco y negro, con vista previa en vivo.
- **Tiempo:** recorte por archivo y velocidad de 0.5× a 2× sin cambiar el tono de la voz.
- **Solo el audio:** extrae el audio en MP3, WAV, M4A (AAC) u Opus, con calidad, muestreo, mono, volumen, normalización y entrada y salida suaves.

## Cómo funciona

- El video se reproduce de forma oculta, se dibuja en un `canvas` y se vuelve a grabar con `MediaRecorder` al bitrate calculado. Por eso tarda más o menos lo que dura el video (salvo que se suba la velocidad). La pestaña debe quedar abierta y visible mientras se procesa.
- El audio en MP3 y WAV se decodifica con la Web Audio API y se codifica con [lamejs](https://github.com/zhuker/lamejs), sin reproducir el archivo completo.
- Dependencias por CDN: [JSZip 3.10.1](https://stuk.github.io/jszip/) y lamejs 1.2.1. Fuente: Raleway (Google Fonts).
- Identidad visual según el manual de marca de Amigos for Christ: Amigos Blue `#00758F`, Amigos Navy `#0A2240` y Highlight Blue `#96D1DE`.
