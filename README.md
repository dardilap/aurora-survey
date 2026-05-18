# Aurora — CISO LATAM Survey

Encuesta pública para validación de propuesta producto con CISOs LATAM.

**URL:** https://dardilap.github.io/aurora-survey/

## Setup

Form action target: `https://formsubmit.co/dardilap@gmail.com`

**IMPORTANTE — Activación primera vez:**
1. Owner debe completar la encuesta una vez con datos de prueba
2. Recibirá email de formsubmit.co con link de activación
3. Clickear el link para autorizar recepción de respuestas reales
4. Después de eso, todas las respuestas llegan al email automáticamente

## Estructura

- `index.html` — encuesta principal (22 preguntas, 7 secciones)
- `thank-you.html` — landing post-submit

## Confidencialidad

Las respuestas individuales nunca se comparten. Solo agregados anónimos con n>=5.

## Stack

- HTML5 + Tailwind CDN (sin build)
- formsubmit.co para envío (gratis, sin auth requerida)
- localStorage para autoguardar progreso
- Mobile-responsive + dark mode
