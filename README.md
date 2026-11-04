# Guía Pamplona Arena Games 26

Web app (PWA) con los WODs por categoría de los **Pamplona Arena Games 26** (Navarra Arena, Pamplona · 14 – 15 nov 2026), pensada para el móvil. Guía no oficial.

👉 **https://pamplona-arena-games.vercel.app/**

- 🏋️ **WODs**: cada WOD se abre en tu categoría, con pestañas para ver el de Scaled, Intermedio o RX. Incluye «Lo que cambia entre categorías», el flow paso a paso, los standards de tu nivel y el enlace al briefing oficial.
- ℹ️ **Info y horarios**: fechas, sede, categorías, formato y enlaces oficiales. Los horarios se añadirán cuando la organización publique los heats.
- 🔗 **Enlace por categoría**: `#eq-esc`, `#eq-int-hhmm` (por defecto), `#eq-int-hhhm`, `#eq-rx`, `#ind-elite-m`, `#ind-elite-f`. La categoría elegida se queda guardada en el móvil.
- 📱 **PWA**: se instala en el móvil, funciona sin conexión y se actualiza sola con cada versión nueva.

## Datos

En `index.html`: `EVENT`, `CATS`, `WODS` (pasos, comparativa, flow, standards) y `SCHEDULE` (vacío hasta que salgan los heats, una fila por heat).
Fuentes: publicación de @pamplonarenagames del WOD 1 y briefing PDF de Circle21 (4 nov 2026).

Para añadir un WOD o los horarios, edita `index.html` y **sube la versión del caché en `sw.js`** (`pag-v1` → `pag-v2`). Al abrirla, la app siempre pide la página a la red; subir la versión hace además que las apps que estaban abiertas en segundo plano se recarguen solas al volver a ellas.

---

Herramienta diseñada por [DigitalWorkApps](https://digitalworkapps.netlify.app)
