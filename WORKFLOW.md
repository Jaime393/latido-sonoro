# WORKFLOW — Jaime393/latido-sonoro

Descripción del workflow `.github/workflows/miu-auto-deploy.yml` (506 bytes, 21 líneas), a partir del texto leído entero. Solo SÉ, con fuente.

Fuente: `~/workspace/mineria/latido-sonoro/MINERIA.md` §1.4 (lectura de texto con `get_file_contents`). Los pasos del workflow se describen como texto leído; no se ejecutaron en esta minería.

## El workflow

- Nombre: "MIU Auto-Deploy Sin PAT".
- Disparadores: `workflow_dispatch` y `push` a `main`.
- Permisos: declara `permissions: contents: write` dos veces.
- Único job: `deploy`, en `ubuntu-latest`.
- Pasos: checkout; escribir "# MIU 16/16" en `AUTO.md`; configurar git con usuario `miu-tejedor` y correo `miu@local`; añadir `AUTO.md`; hacer commit con mensaje "MIU Auto" solo si hay cambios; hacer push a `main`.
- No contiene ningún paso de build, de pruebas ni de despliegue a Pages.

## La coincidencia exacta (SÉ)

- El contenido de `AUTO.md` es "# MIU 16/16" (12 bytes, 1 línea).
- El último commit (`f75f399`, 2026-08-23T16:46:40Z) tiene autor y committer `miu-tejedor` (`miu@local`) y mensaje "MIU Auto".
- Contenido, autor, correo y mensaje coinciden exactamente con lo que el workflow escribe y configura.

Fuente de la coincidencia: lectura de texto de `AUTO.md` y de `miu-auto-deploy.yml` (§1.4 del borrador) y `list_commits` (§1.2 del borrador).
