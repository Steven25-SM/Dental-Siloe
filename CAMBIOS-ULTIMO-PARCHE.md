# Dental Siloé — Último parche PageSpeed (móvil)

Base: `Dental-Siloe-Parche-Final-CLS-CSS.zip`. Se conservan los parches PageSpeed y 2K/4K previos.

## CLS de Hero móvil
- `src/pages/index.astro`: se declaran ancho y alto **700 × 900** en el `<source>` móvil de `<picture>`. El `<img>` conserva 1400 × 788 para escritorio. Esto comunica al navegador la proporción correcta antes de descargar la imagen móvil.
- `src/styles/global.css`: reserva `aspect-ratio: 7 / 9` en el hero a <= 767px y mantiene `object-fit: contain`. Objetivo: evitar el desplazamiento del bloque `.hero-content` reportado por Lighthouse.

## Entrega de imágenes
- `logotipo-320.webp` y `logotipo-480.webp`: variantes responsive en Navbar, con `srcset`/`sizes`; conserva la transparencia.
- `antes-y-despues-rehabilitacion-oral-640.webp`: variante pequeña, seleccionada mediante `srcset`/`sizes`.
- `fotos/hero-mobile-480.webp`: variante más pequeña para la fotografía de Nosotros.

## Comprobaciones
1. `npm install` (si faltan dependencias); `npm run build`.
2. Publicar en Netlify; comprobar Hero en 360, 390, 430, 768, 1024 y 1920 px, además de 2K/4K.
3. Medir PageSpeed móvil varias veces y mirar CLS (objetivo <0.1) y ahorro de imágenes. Las cifras fluctúan; no se garantiza puntuación 100.

No se ha alterado la paleta, los textos, el flujo de navegación ni las secciones de la landing.
