# Parche PageSpeed final — Dental Siloé (23/10/2026)

Base: Dental-Siloe-Responsive-2K-4K.zip. Conserva las optimizaciones de imágenes y las reglas 2K/4K.

## Cambios

1. `src/layouts/Layout.astro`: usa `global.css?inline` para incluir en el `<head>` el CSS generado por Tailwind. Evita la dependencia extra de `/_astro/index....css` que Lighthouse clasifica como recurso que bloquea el renderizado. No elimina CSS ni lo carga tarde, para evitar parpadeos y cambios de geometría.
2. Google Fonts: `display=swap` -> `display=optional`. Evita que la fuente Bricolage Grotesque, si llega tarde, sustituya al fallback durante la primera visita y mueva el título (CLS). En una primera carga lenta podría mostrarse la fuente de sistema; en cargas con la fuente en caché puede aparecer la fuente original. Esto es deliberado.
3. Conservados: imágenes optimizadas, layout adaptado a 2K/4K, scripts y metadatos.

## Comprobación necesaria

```bash
npm install
npm run build
npm run dev
```

Publica en Netlify y mide de nuevo **Móvil** en PageSpeed Insights. Revisa `CLS` (objetivo <0.1) y la sección de recursos que bloquean el renderizado. El resultado no puede garantizarse sin compilar y ejecutar una medición real; otras fuentes de cambios de diseño pueden existir.

NOTA: Inline CSS incrementa el HTML y reduce caché CSS independiente, una decisión consciente para un único sitio de una página con CSS compilado ~8.8 KiB. No lo reutilices a ciegas en webs grandes.
