# LuchoWeb (Vercel + Netlify-ready)

Base única y consolidada para despliegue estático.

## Estructura final
- `index.html`: sitio completo (HTML + CSS + JS)
- `_redirects`: fallback SPA (`/* /index.html 200`)
- `404.html`: fallback extra redirigiendo a `index.html`
- `netlify.toml`: configuración de deploy para Netlify
- `vercel.json`: configuración de rewrites/headers para Vercel

## Deploy recomendado en Netlify
- Build command: *(vacío o no-op)*
- Publish directory: `.`
- Branch: la rama correcta

## Deploy recomendado en Vercel
- Framework preset: **Other**
- Root Directory: `.`
- Build command: vacío
- Output directory: vacío

Si sale `404: NOT_FOUND` en Vercel, casi siempre es por:
1. Root Directory incorrecto (no está apuntando al repo raíz).
2. Proyecto conectado a otra rama distinta de la que tiene `index.html`.
3. Deploy anterior cacheado sin redeploy.

Con esta base no hay duplicados (`public/`) ni doble fuente de verdad.
