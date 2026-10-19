# Dental Siloé — tareas para Google (19/10/2026)

## Implementado en código

- Title y descripción en español, canonical y directivas de indexación.
- Open Graph / Twitter para compartir la página.
- Imagen social y Apple Touch Icon.
- sitemap.xml y robots.txt para un sitio de una página.
- Datos estructurados `Dentist` con información limitada a lo conocido.
- `site` de Astro con URL actual de Netlify.

## Pasos en Google Search Console (requieren tu cuenta)

1. Entra en https://search.google.com/search-console y añade una propiedad **Prefijo de URL** con `https://dentalsiloe.netlify.app/` (si no tienes dominio propio).
2. Verifica la propiedad mediante el método que Google te ofrezca, como metaetiqueta HTML. **No compartas contraseñas ni códigos privados**; si te ofrece una metaetiqueta, inserta la etiqueta en el `<head>` de `src/layouts/Layout.astro`, reconstruye y despliega.
3. Tras publicar, comprueba en el navegador `https://dentalsiloe.netlify.app/robots.txt` y `/sitemap.xml`.
4. En Search Console, sección **Sitemaps**, añade `sitemap.xml`.
5. En **Inspección de URLs**, inspecciona `https://dentalsiloe.netlify.app/`, usa **Probar URL publicada** y si es apta solicita **Indexación**.
6. Revisa luego el estado de **Páginas / Indexación**; indexación y posicionamiento no son instantáneos ni garantizados.

## Google Maps / Perfil de Empresa

- Busca Dental Siloé en Google Maps y confirma con el propietario quién administra la ficha. No crees duplicados.
- Con autorización, revisar categoría, nombre, URL pública, horarios, fotos, dirección y contacto. Las modificaciones pueden exigir verificación de Google.
- Validar que el marcador en Maps corresponda al consultorio.

## Pruebas finales

- `npm install` y `npm run build`; Netlify debe usar Build command `npm run build` y Publish directory `dist`.
- Comprueba menú móvil, WhatsApp en móvil/PC, enlaces de Google Maps, ausencia de scroll horizontal.
- Ejecuta PageSpeed Insights en móvil y desktop: https://pagespeed.web.dev/.
- Revisa Lighthouse de accesibilidad, contrastes, títulos, imágenes y consola del navegador.
- Guarda capturas de la web publicada, responsive, pruebas, versión de GitHub y entrega para EFSRT.

## Pendientes de verificación con el consultorio

- Tratamientos reales, profesionales, años de experiencia y cualquier testimonio.
- Confirmar horarios (actualmente obtenidos de Maps), dirección exacta y permisos para gestionar la ficha.
- Cuando cambien a un dominio propio, actualizar `site`, URL canónica, sitemap, Open Graph y Search Console.
