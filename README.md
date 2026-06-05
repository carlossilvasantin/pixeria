# pixeria.com

Landing page estática para PIXERIA — el estudio de IA de Admira Xperience.

## Estructura

- `index.html` — landing completa (hero, pilares, flujo, integraciones, stock, tech, CTAs)
- `assets/styles.css` — tokens matrix-green terminal + responsive
- `CNAME` — pixeria.com (para GitHub Pages)
- `robots.txt`, `sitemap.xml`

## Desarrollo local

```bash
cd pixeria
python -m http.server 9410
# o
npx serve .
```

Abre http://localhost:9410

## Deploy (GitHub Pages)

1. Sube esta carpeta a un repo (o a la raíz del que ya usa GH Pages).
2. En Settings → Pages → Source: Deploy from a branch (main) / root.
3. El CNAME apunta a pixeria.com — configura el dominio en tu registrar + DNS para que apunte a las IPs de GH Pages o usa Cloudflare proxy.

## Futuro

- Cuando se decida, mover o clonar el studio (admira-studio/) aquí como `/studio` o subdominio.
- Posible integración de un teaser interactivo (formulario de brief que llame al worker /xai/image o /tts como demo público).

## Branding

- Verde matrix terminal (#00ff41) fiel al actual admira-studio y overlay Pixer Feed del game.
- Tipografía mono (JetBrains Mono recomendado).
- Consistente con el resto del ecosistema Admira (usa los mismos mensajes de Telegram, worker y R2).

## Créditos

Parte del grupo Admira · Xperience · 2026.
