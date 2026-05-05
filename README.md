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

## Despliegue automático en Cloudflare Pages

Este repo queda listo para desplegar en Cloudflare Pages con GitHub Actions.

### Secrets requeridos

- `CLOUDFLARE_ACCOUNT_ID`
- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_PAGES_PROJECT_NAME`

### Flujo

- Cada push a `master` o `main` ejecuta build y despliegue.
- El output publicado es `dist/`.

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
