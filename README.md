# 🛍️ Encuesta de Artículos - CeluCenter

Página web para que los gerentes voten por los artículos que quieren ver en las tiendas (mayoreo Buytiti - caja cerrada).

## Características

- ✅ 13 productos con foto, código, descripción y precio
- ✅ Voto único por dispositivo (localStorage)
- ✅ Countdown en tiempo real hasta la fecha de cierre
- ✅ Muestra ranking con ganador al cerrar la encuesta
- ✅ Diseño responsive (móvil, tablet, desktop)
- ✅ Estilo corporativo CeluCenter (Poppins, rojo/azul)

## Cómo usar

1. Configura la fecha límite en `index.html` → `const DEADLINE = new Date('YYYY-MM-DDTHH:MM:SS')`
2. (Opcional) Configura un backend en `BACKEND_URL` para集計 real de votos entre dispositivos
3. Sube a GitHub Pages o cualquier hosting estático
4. Comparte el link por WhatsApp a los gerentes

## Personalización rápida

- **Fecha límite:** línea 470 en `index.html`
- **Backend para集計:** línea 471 en `index.html` (opcional, ver sección)
- **Productos:** array `PRODUCTS` en `index.html`

## Backend opcional (para集計 real de votos)

Sin backend, cada dispositivo solo ve sus propios votos. Para集計 real entre todos los gerentes, configura `BACKEND_URL` apuntando a:

- **Google Sheets** (Apps Script Web App) — gratis, fácil de ver resultados
- **jsonbin.io** — gratis sin auth, devuelve JSON público
- **Bitrix24 webhook** — crea tareas/entradas en CRM
- **Webhook.site** — solo para testing

Ejemplo con jsonbin.io:
```js
const BACKEND_URL = 'https://api.jsonbin.io/v3/b/TU_BIN_ID';
```

## Stack

- HTML5 + CSS3 + Vanilla JS
- Sin dependencias
- Tamaño total: ~30KB + imágenes
