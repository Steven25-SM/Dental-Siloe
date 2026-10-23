# Dental Siloé — ajuste para monitores 2K y 4K

Este paquete parte de `Dental-Siloe-PageSpeed-Parche.zip` y conserva sus imágenes optimizadas.

## Qué se modificó
- Solo `src/styles/global.css`: bloque V11 al final del archivo.
- Desde 1920 px: contenedor hasta 1520 px, tarjetas y tipografía proporcionadas.
- Desde 2560 px: contenedor hasta 1820 px, mayor espacio entre secciones, fotos y textos equilibrados.
- Desde 3440 px: límite de 1920 px de ancho para evitar líneas de texto excesivamente largas.
- El hero sigue cubriendo toda la pantalla y el texto tiene anchura controlada.
- Sin nuevas dependencias, fuentes, scripts ni imágenes.
- Sin alterar los breakpoints existentes para móviles, tablets y pantallas menores a 1920 px.

## Probar
1. `npm install` (si aún no están instaladas las dependencias).
2. `npm run build`.
3. `npm run dev` y probar 1920x1080, 2560x1440, 3840x2160 y el zoom del navegador.
4. Publicar en Netlify y revisar visualmente imágenes y textos en un monitor grande o el modo dispositivo del navegador.

Nota: los tamaños indicados son resoluciones de viewport en píxeles CSS, que pueden diferir de la resolución física por el escalado del sistema.
