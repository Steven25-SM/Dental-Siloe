# Optimización de rendimiento — Dental Siloé

Se conservó el diseño, las funciones actuales de WhatsApp y la configuración SEO.

## Cambios
- Logotipo del header: `/logotipo-optimizado.webp` (aprox. 46 KiB antes 1209 KiB).
- Ícono WhatsApp: `/whatsapp-logo-optimizado.webp` (aprox. 9 KiB antes 823 KiB), manteniendo transparencia.
- Fotografía del Hero móvil: se optimizó EN LA MISMA RUTA `/fotos/hero-mobile.webp` (aprox. 47 KiB antes 518 KiB). Si se sustituye esta foto en el futuro, conviene volver a comprimirla.
- Fotografía de entrada: se optimizó EN LA MISMA RUTA `/fotos/entrada-consultorio.webp` (aprox. 68 KiB antes 729 KiB).
- Fotografías de servicios: nuevas versiones WebP con rutas actualizadas en `index.astro`.
- Favicon del navegador utiliza ahora el archivo pequeño `/favicon.ico`.
- Se agregó preload para la fotografía inicial móvil.
- Se mantuvieron `public/googlea33cc2767e7ea0a3.html`, `public/sitemap.xml`, `public/robots.txt`, configuración canonical y datos estructurados.

## Publicación
1. Reemplazar o actualizar en el repositorio con los archivos de este proyecto, manteniendo las credenciales privadas fuera de Git.
2. Ejecutar `npm ci` y `npm run build` con Node.js 22.19+ (o versión compatible con Astro).
3. Hacer push a GitHub y esperar la publicación de Netlify.
4. Volver a medir la URL publicada con PageSpeed Insights (Móvil y Ordenador).

## Pendiente de comprobación
- La compilación no se logró completar en el entorno de preparación por falta de dependencias disponibles y timeout de instalación.
- La puntuación PageSpeed debe medirse nuevamente; 90+ no está garantizado.
- La alerta específica de contraste debe revisarse al finalizar la paleta aprobada por los dueños.
- Las imágenes ilustrativas de servicios no son fotografías verificadas del equipo de Dental Siloé.
