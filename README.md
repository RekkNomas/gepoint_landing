# GetPoint Landing (Astro + Tailwind v4)

Landing estática basada en https://www.getpoint.cl/ con foco en fidelidad visual, mejor composición responsive y performance.

## Requisitos

- Node.js >= 22.12
- npm

## Ejecutar en local

```bash
npm install
npm run dev
```

## Despliegue en Cloudflare Pages

El proyecto puede conectarse directo a Cloudflare Pages desde GitHub.

### Variables recomendadas

- `SITE_URL=https://www.gpsolution.es`

### Archivo de configuración

- `wrangler.jsonc` define `pages_build_output_dir` y la URL base del sitio.

### Flujo

- Cloudflare Pages toma `main` como rama de producción.
- El output publicado es `dist/`.
- Canonical, OG y sitemap usan `SITE_URL` si está definida.

## Stack

- Astro
- Tailwind CSS v4 (configuración CSS-first en `src/styles/global.css` con `@theme`)
- Sin JS de cliente para el slider (animación CSS-only + `prefers-reduced-motion`)

## Notas de performance

- Hero y logo principal con `preload` desde el layout.
- Imágenes bajo el fold con `loading="lazy"` y dimensiones explícitas.
- Estructura semántica para SEO + metadatos OG/Twitter.
- CSS con tokens semánticos de marca para consistencia visual.

## Assets

Los assets fueron descargados a `public/assets/getpoint/` desde las URLs autorizadas del sitio original.
