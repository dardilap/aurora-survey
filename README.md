# Aurora — CISO LATAM Survey

Landing page que redirige al Google Form oficial de la encuesta CISO LATAM.

**URL pública:** https://dardilap.github.io/aurora-survey/
→ redirige automáticamente a Google Form:
https://docs.google.com/forms/d/e/1FAIpQLSc7F1ZQxW66l_fLyxdmUDTV9SYXUtKQSsiZrAJlIQ9L1D61qw/viewform

## Por qué Google Forms (vs HTML custom)

- Google infra (99.99% uptime) — sin outages como formsubmit.co
- Respuestas en Google Sheet automático
- Email notifications nativas
- Sin dependencias externas (Cloudflare, formsubmit, etc.)
- Owner full control (editar form, exportar respuestas)

## Estructura

- `index.html` — landing con branding Aurora + redirect inmediato a Google Form
  - JS redirect en 300ms (para alcanzar a ver branding)
  - Meta refresh en 2s (fallback si JS off)
  - Link manual visible como último fallback

## Por qué mantener esta URL como wrapper

- Una sola URL canónica para distribución (`dardilap.github.io/aurora-survey/`)
- Posible cambio futuro del Google Form sin tener que re-distribuir URL
- Branding Aurora visible 300ms antes de aterrizar en Google
- Posible analytics/tracking si se agrega en el futuro

## Cambiar el Google Form destino

Editar el URL en 3 lugares del `index.html`:
1. `<meta http-equiv="refresh" content="2; url=...">`
2. `window.location.replace('...')` en `<script>`
3. `<a href="...">` del link manual
