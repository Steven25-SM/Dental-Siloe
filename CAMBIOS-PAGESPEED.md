# Optimización PageSpeed — Dental Siloé

Se mantuvieron la estructura y el aspecto de la landing.

- Comprimido y redimensionado `public/logotipo-optimizado.webp`; corregidos los atributos de anchura y altura del Navbar.
- Convertido a WebP `antes-y-despues-rehabilitacion-oral.png` y actualizada la referencia y dimensiones en `index.astro`.
- Optimizados `fotos/consultorio-hero.webp` (imagen principal de escritorio), `fotos/hero-mobile-propuesta-01.webp` (principal en móvil/tableta), `fotos/hero-mobile.webp`, `image-1-optimizado.webp` y `whatsapp-logo-optimizado.webp`.
- El `preload` móvil ahora solicita la fotografía que se muestra arriba del pliegue, no la de la sección Nosotros.
- Reducido `favicon.png` a dimensiones compatibles con su declaración en HTML.

Los hallazgos sobre CSS bloqueante son propios de la hoja de estilos base de Astro/Tailwind; no se ha aplicado una modificación arriesgada para eliminarla. Las puntuaciones reales dependen del despliegue y deben volverse a medir con PageSpeed Insights.

## Uso

`npm install` y `npm run build`. Publicar el `dist/` que se genera después de compilar.

El ZIP omite `.git`, `.astro` y `dist` anteriores porque son artefactos/cache y no se necesitan para restaurar el proyecto.
