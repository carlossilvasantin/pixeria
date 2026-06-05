# pixeria.com

Landing page estática para PIXERIA — el estudio de IA de Admira Xperience.

## Estructura

- `tools/index.html` — landing completa (hero, pilares, flujo, integraciones, stock, tech, CTAs) → se sirve en /tools
- `tools/assets/styles.css` — tokens matrix-green terminal + responsive
- `CNAME` — pixeria.com (para GitHub Pages)
- `robots.txt`, `sitemap.xml` (a nivel raíz del sitio)

## Desarrollo local

```bash
cd pixeria
python -m http.server 9410
# o
npx serve .
```

Abre http://localhost:9410

## Deploy (GitHub Pages)

La landing vive bajo `/tools`.

1. La estructura del repo tiene los archivos de la landing dentro de `tools/`.
2. Publica desde la rama `main` (o `gh-pages`).
3. Con el CNAME `pixeria.com` activado en el repo, la landing estará en `https://pixeria.com/tools/`.
4. Configura GitHub Pages en Settings → Pages → Deploy from a branch (main o gh-pages) / root.

## Futuro

- Cuando se decida, mover o clonar el studio (admira-studio/) aquí como `/studio` o subdominio.
- Posible integración de un teaser interactivo (formulario de brief que llame al worker /xai/image o /tts como demo público).

## Branding

- Verde matrix terminal (#00ff41) fiel al actual admira-studio y overlay Pixer Feed del game.
- Tipografía mono (JetBrains Mono recomendado).
- Consistente con el resto del ecosistema Admira (usa los mismos mensajes de Telegram, worker y R2).

## Créditos

Parte del grupo Admira · Xperience · 2026.
