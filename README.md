# LuchoWeb (Netlify-ready)

Base única y consolidada para despliegue estático.

## Estructura final
- `index.html`: sitio completo (HTML + CSS + JS)
- `_redirects`: fallback SPA (`/* /index.html 200`)
- `404.html`: fallback extra redirigiendo a `index.html`
- `netlify.toml`: configuración de deploy para Netlify

## Deploy recomendado en Netlify
- Build command: *(vacío o no-op)*
- Publish directory: `.`
- Branch: la rama correcta

Con esta base no hay duplicados (`public/`) ni doble fuente de verdad.
