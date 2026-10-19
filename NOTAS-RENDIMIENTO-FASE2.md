# Dental Siloé — Segunda revisión de rendimiento

## Cambios precisos
- `src/layouts/Layout.astro`: la hoja de estilos de Google Fonts se carga de forma no bloqueante (`media="print"` y `onload`), con alternativa `<noscript>`. Se conservan **Bricolage Grotesque y Figtree**, sin cambiar familias ni pesos. Esto es una prueba de optimización; puede observarse un breve cambio de tipografía mientras se descargan las fuentes y debe verificarse visualmente.
- `src/pages/index.astro`: se indican las dimensiones originales (800 × 1074) de la fuente de imagen móvil en `<picture>`, manteniendo intacta su presentación CSS.

No se cambió la estructura, las fotografías ni el diseño. Tampoco se tocaron sitemap, robots, verificación de Google ni WhatsApp.

## Publicación y comprobación
1. Integrar los cambios en tu repositorio existente: sustituir `src/layouts/Layout.astro` y `src/pages/index.astro`.
2. Ejecutar `npm ci` y `npm run build` con Node >= 22.19, y luego `git add`, `git commit`, `git push`.
3. Esperar a que Netlify indique Published. Comprobar la tipografía al cargar y al navegar, tanto en móvil como en escritorio.
4. Ejecutar PageSpeed Insights al menos 2–3 veces (sus puntuaciones varían). Comprobar especialmente LCP y CLS. Si aparece un cambio visual indeseado de tipografía, volver temporalmente al `link rel="stylesheet"` original.

## Limitación de esta entrega
No se alojaron las fuentes localmente: no estaban incorporadas en el ZIP y no fue posible descargar sus archivos fuente en el entorno. La carga de Google Fonts permanece externa, pero deja de bloquear el primer pintado. No se pudo ejecutar `npm ci` completamente en este entorno (dependencias no presentes en caché).
