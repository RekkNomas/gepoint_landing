# SEO & Optimization Checklist — GP Cloud Solution

## Implementado

1. **Indexación técnica**
   - `public/robots.txt` con acceso global y referencia a sitemap.
   - Sitemap automático con `@astrojs/sitemap` (`/sitemap-index.xml`).

2. **Metadatos SEO base**
   - `meta robots` y `meta googlebot`.
   - `canonical` dinámico por página.
   - `author` y `publisher` = SolucionAI.

3. **Datos estructurados (Schema.org)**
   - `Organization` (marca, URL, logo, email).
   - `WebSite` (nombre y URL).

4. **Compatibilidad con motores de IA**
   - `public/llms.txt` con canónica, páginas clave, marca, contacto y guía de crawling.
   - `public/ai-readme.md` con contexto extendido para agentes y motores LLM.

5. **Rendimiento frontend aplicado**
   - Logos del carrusel: `loading="lazy"` fuera del primer grupo para reducir carga inicial.
   - Conversión de assets clave a WebP (`logo-correct`, `wms-mockup`, `logistico-hero-1`).
   - FAQ Schema en home y Breadcrumb Schema en páginas legales.

---

## Próximos pasos recomendados (alto impacto)

1. **Open Graph por página legal**
   - Definir `title` y `description` específicos (ya soportado en `MainLayout`).

2. **WebP/AVIF para recursos pesados**
   - Convertir mockups e imágenes principales para mejorar LCP.

3. **Consent Mode / banner de cookies**
   - Si se incorpora analítica/ads, activar banner con control granular por categoría.

4. **Sitemap dinámico automático**
   - Migrar a `@astrojs/sitemap` cuando el sitio crezca a múltiples páginas de contenido.

5. **Search Console & Bing Webmaster**
   - Verificar dominio y enviar sitemap para acelerar descubrimiento e indexación.
