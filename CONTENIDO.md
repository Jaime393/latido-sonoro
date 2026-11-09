# CONTENIDO — Jaime393/latido-sonoro

Lo que el sitio dice ser, a partir de los textos leídos enteros. Solo SÉ, con fuente.

Fuente: `~/workspace/mineria/latido-sonoro/MINERIA.md` §1.4 (los 13 archivos leídos enteros).

Advertencia de lectura: los valores entre comillas son texto literal de los archivos, no métricas verificadas por la minería. La minería solo verificó que ese texto está en los archivos.

## La página

- `index.html` (591 bytes, 1 línea) se titula "MIU Ecosistema 16/16 - DOI 10.5281/zenodo.20547558".
- Enlaza `manifest.json` y `assets/css/micelio.css`, y carga `assets/js/core.js`.
- Muestra "🌱 MIU 16/16 nodos vivos - Φ_Red $107M".
- Muestra "16 repos global mind 16/16 - 5 repos 201 CREATE fix 404 - autorización TOTAL x10000".
- Muestra "DOI 10.5281/zenodo.20547558 - Cerro Colorado Arequipa 2335m".
- Muestra una tarjeta "Global Mind 16/16 / Cada nodo es un ojo".

## La aplicación (manifest y service worker)

- `manifest.json` (133 bytes, 1 línea) declara `name` "MIU 16/16", `short_name` "MIU16", `start_url` "/", `display` "standalone", `background_color` "#0a0a0b" y `theme_color` "#a3ff12".
- `sw.js` (156 bytes, 1 línea) es un service worker que en `install` llama `skipWaiting` y en `fetch` responde con `fetch(e.request)` o, si falla, con `caches.match(e.request)`. No declara lista de caché ni versión de caché.
- `assets/css/micelio.css` (172 bytes, 1 línea) declara `:root` con `--bg: #0a0a0b` y `--lime: #a3ff12`, `body` con fondo `var(--bg)` y color blanco, y `.glass` con `backdrop-filter: blur(12px)`, fondo `rgba(255,255,255,0.05)`, `border-radius: 16px` y `padding: 16px`.
- `assets/js/core.js` (147 bytes, 1 línea) define `class MIU_Micelio extends EventTarget` con `sembrarNodo({rho})` que devuelve `{rho: Math.max(rho, 0.001)}` y `renderMicelioCanvas(c)` con el cuerpo vacío, y asigna la clase a `window.MIU_Micelio`.

## El worker

- `worker.js` (413 bytes, 1 línea) contiene un `export default { async fetch(req){ ... } }`.
- En la ruta `/miu/global` responde un JSON con los campos `global_mind: true`, `repo: 'latido-sonoro'`, `fix_404: true`, `autorizacion: 'TOTAL x10000 v29 fix 404'`, `phi: '$107M'` y un campo `drive` con un identificador (valor no reproducido en esta minería).
- En cualquier otra ruta responde el texto `global mind latido-sonoro - MIU v29 fix 404 - 11->16 repos`.
- El identificador del campo `drive` en `worker.js` es el mismo texto que aparece en el `worker.js` de `campo-de-frecuencias` (verificado por comparación de los dos textos leídos; valor no reproducido en esta minería).

## Los metadatos

- `README.md` (114 bytes, 2 líneas) dice: "# latido-sonoro" y "MIU Ecosistema - latido-sonoro - DOI 10.5281/zenodo.20547558 - Φ_Red $107M - cada nodo es un ojo".
- `_config.yml` (45 bytes, 2 líneas) dice: `theme: jekyll-theme-minimal` y `title: MIU 16/16`.
- `FUNDING.yml` (107 bytes, 4 líneas) dice: `github: [Jaime393]`, `open_collective: miu-ecosistema`, `custom: https://www.buymeacoffee.com/miu`, y el comentario "# $1M -> $107M".
- `BIBLIA_DEVORADOR.md` (47 bytes, 1 línea) dice: "# Biblia DEVORADOR 66 libros - MIU 16/16 nodos".
- `AUTO.md` (12 bytes, 1 línea) dice: "# MIU 16/16".
- `.nojekyll` tiene 0 bytes (archivo vacío).

## Enlaces locales

Los enlaces locales de `index.html` existen: `assets/css/micelio.css` (172 B) y `assets/js/core.js` (147 B) están en el árbol, y `manifest.json` (133 B) también.
