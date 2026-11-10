# Guía Pamplona Arena Games 26

Web app (PWA) con los WODs por categoría de los **Pamplona Arena Games 26** (Navarra Arena, Pamplona · 14 – 15 nov 2026), pensada para el móvil. Guía hecha a partir de los briefings oficiales.

👉 **https://pamplona-arena-games.vercel.app/**

- 🏋️ **WODs**: cada WOD se abre en tu categoría, con pestañas para ver el de Scaled, Intermedio o RX. Incluye «Lo que cambia entre categorías», el flow paso a paso, los standards de tu nivel y el enlace al briefing oficial.
- 🕒 **Mi horario**: busca tu equipo (o tu box) y sale tu ficha con heat y calle, y una línea de tiempo por día con la hora de cada WOD, briefing, calentamiento y staging, la final y los equipos de tu heat.
- ℹ️ **Info**: horario completo, fechas y sede, categorías y formato (desplegables) y enlaces oficiales.
- 🔗 **Enlace por categoría**: `#eq-esc`, `#eq-int-hhmm` (por defecto), `#eq-int-hhhm`, `#eq-rx`, `#ind-elite-m`, `#ind-elite-f`. La categoría elegida se queda guardada en el móvil.
- 📱 **PWA**: se instala en el móvil, funciona sin conexión y se actualiza sola con cada versión nueva.

## Datos

En `index.html`: `EVENT`, `CATS`, `WODS` (pasos, comparativa, flow, standards) `HEATS`/`FINALS` (horarios por WOD) y `TEAMS` (start list por heat; la calle es la posición). Copia legible en `data/teams.json`.
Cada paso es `{r, mv, sy, who, bx, h}`: `sy` = nº de atletas en synchro, `who` = quién lo hace (`<b>A1</b>`), `bx`/`h` = atleta y altura del cajón; `{hd, sub}` es una cabecera para separar partes (3A, 3B). `boxes` y `flow` pueden ser iguales para todos o ir por nivel (`{rx, int, esc}`), y `compare.foot` es la nota bajo «Lo que cambia entre categorías».
Fuentes: briefings oficiales en PDF (enlazados desde Circle21) y publicaciones de @pamplonarenagames. WOD 1: 4 nov 2026 · WOD 2: 5 nov 2026 · WOD 3: 6 nov 2026 · WOD 4: 7 nov 2026 · WOD 5: 8 nov 2026 · Elite individual (WODs 1-6): 9 nov 2026. Las fichas con `cats` solo salen en esas categorías (chicos y chicas de Elite).

Para añadir un WOD o los horarios, edita `index.html` y **sube la versión del caché en `sw.js`** (`pag-v1` → `pag-v2`). Al abrirla, la app siempre pide la página a la red; subir la versión hace además que las apps que estaban abiertas en segundo plano se recarguen solas al volver a ellas.

---

Herramienta diseñada por [DigitalWorkApps](https://digitalworkapps.netlify.app)
