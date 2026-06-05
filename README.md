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

## Deploy (Cloudflare Pages - principal)

La landing vive bajo `/tools`.

**URL pública actual:** https://pixeria.pages.dev/tools/

### Ventajas de Cloudflare Pages (vs GitHub Pages anterior):
- Unlimited bandwidth y requests.
- Preview deployments automáticos por cada commit/PR (URL única tipo `hash.pixeria.pages.dev/tools/`). 
- Mejor rendimiento global (CDN de Cloudflare).
- Fácil custom domain `pixeria.com`.
- Integración nativa con tu Worker (pixer-eleven), R2 y KV.
- Posibilidad de añadir Functions/edge logic después.
- Cache invalidation instantáneo.

### Cómo se actualiza:
- Conecta el repo GitHub "carlossilvasantin/pixeria" en el dashboard de Cloudflare Pages (una sola vez).
- A partir de ahí, cada `git push` a `main` hace deploy automático.
- O usa `npx wrangler pages deploy . --project-name=pixeria` para deploy manual rápido.

### Custom domain:
En Cloudflare dashboard → Pages → pixeria → Custom domains → Add `pixeria.com` (o `www.pixeria.com`).

El CNAME del repo se puede mantener o quitar.

God Mode sigue funcionando igual: edita, Export HTML, reemplaza `tools/index.html`, commit y push.

## Futuro

- Cuando se decida, mover o clonar el studio (admira-studio/) aquí como `/studio` o subdominio.
- Posible integración de un teaser interactivo (formulario de brief que llame al worker /xai/image o /tts como demo público).

## Branding

- Verde matrix terminal (#00ff41) fiel al actual admira-studio y overlay Pixer Feed del game.
- Tipografía mono (JetBrains Mono recomendado).
- Consistente con el resto del ecosistema Admira (usa los mismos mensajes de Telegram, worker y R2).

## God Mode (Editor de textos)

La web entera es editable en "God Mode":

- Activar: **Ctrl + Shift + G** (o Cmd+Shift+G)
- O: click 4 veces rápidas en el logo "PIXERIA"
- O: escribe la palabra `god ` (con espacio) en cualquier parte

Una vez activado:
- Todos los textos principales se vuelven editables directamente (como un editor de texto normal).
- Aparece un panel flotante con botones:
  - **Export HTML** → descarga el archivo listo para reemplazar `tools/index.html`
  - **Copy HTML**
  - **Reset**
- Pulsa **Esc** para salir.

Los cambios se guardan temporalmente en localStorage para que puedas recargar y continuar.

Después de editar → Export → reemplaza el archivo y haz commit/push.

Local test: `cd pixeria && python -m http.server 9411` → abre http://127.0.0.1:9411/tools/

## Créditos

Parte del grupo Admira · Xperience · 2026.