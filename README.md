# Zasqua starter template

**[Versión en español abajo](#plantilla-inicial-de-zasqua)**

A starting point for publishing your own archive with **Zasqua**, the
open-source archival publishing engine. Fork this repository, install, and
build — a working, searchable site comes up with sample data so you can see
the result before adding your own.

Zasqua turns a six-file JSON description of your holdings into a fast,
fully static, bilingual (English / Spanish) discovery site: multilevel
finding aids, authority records for people, organizations and places, and
in-browser full-text search. There is no database and no server to run —
the output is plain HTML you can host anywhere.

## Quick start

```bash
# Fork on GitHub (keeps a visible link to the upstream starter), then:
gh repo fork UCSB-AMPLab/zasqua-template --clone --fork-name my-archive
cd my-archive

npm install          # pulls the @ucsb-ampl/zasqua engine + toolchain
npm run build        # builds the bundled sample data into public/
npm run dev          # serves a live preview at http://localhost:1313
```

`npm install` pulls the engine (`@ucsb-ampl/zasqua`) and everything it needs
(Hugo Extended, Pagefind, Tailwind) from the npm registry. You receive
engine updates by bumping the `@ucsb-ampl/zasqua` version in `package.json`
and reinstalling — not by syncing the fork. Your fork holds only your
configuration, data, and any theme overrides.

## What is in this repository

| Path | What it is |
|------|------------|
| `package.json` | Declares the Zasqua engine as a dependency |
| `hugo.toml` | Hugo configuration and your site's identity strings |
| `zasqua.manifest.toml` | Which modules are enabled (hierarchy, entities, places, …) |
| `exports/` | The six-file data contract — sample data you replace with your own |
| `content/colofon/` | The colophon page (institutional statement) |

The sample data is real, published archival material (see `NOTICE`).
Replace the files in `exports/` with your own before publishing.

## Configure your instance

1. **Identity** — set your site name, links, and footer text in the
   `[params]` block of `hugo.toml`.
2. **Language** — set the interface language in `zasqua.manifest.toml`
   (`[ui] language`): `en-US` or `es-CO`. That one line switches the whole
   interface; you do not edit `hugo.toml` for it.
3. **Modules** — enable or disable features in `zasqua.manifest.toml`, then
   run `npm run validate` to confirm your data matches.
4. **Data** — put your six JSON export files in `exports/`. Run
   `npx zasqua init` to scaffold a manifest from data you already have.
5. **Branding** — to customize colors, fonts, and layouts, add an overlay
   theme. The site runs on the engine's neutral base theme until you do.
6. **Colophon** — edit `content/colofon/_index.md` with your institution's
   rights, provenance, and licensing statement.

## Hosting

`npm run build` writes a static site to `public/` — plain HTML, JSON, and
images with client-side search, no server or database. Host it anywhere:
copy `public/` to Netlify, Vercel, GitHub Pages, Cloudflare Pages, or any
static web server. The complete deployment guide — data contract, validation,
theming, and hosting — lives in the engine repository:

> https://github.com/UCSB-AMPLab/zasqua — see `docs/guide.md`.

## License

This template is released under the **GNU Affero General Public License
v3.0** (`LICENSE`). The Zasqua engine is likewise AGPL-3.0. See `NOTICE`
for attribution of the bundled sample data.

---

# Plantilla inicial de Zasqua

**[English version above](#zasqua-starter-template)**

Un punto de partida para publicar tu propio archivo con **Zasqua**, el motor
de publicación de archivos digitales de código abierto. Haz un fork de este
repositorio, instala y construye: aparece un sitio funcional y con búsqueda,
con datos de muestra, para que veas el resultado antes de agregar tus propios
datos.

Zasqua convierte la descripción de tus fondos —seis archivos JSON— en un
sitio de consulta rápido, totalmente estático y bilingüe (inglés / español):
descripciones archivísticas de varios niveles, registros de autoridad de
personas, organizaciones y lugares, y búsqueda de texto completo en el
navegador. No hay base de datos ni servidor que mantener: el resultado es
HTML plano que puedes alojar donde quieras.

## Inicio rápido

```bash
# Haz el fork en GitHub (deja un enlace visible a la plantilla de origen) y:
gh repo fork UCSB-AMPLab/zasqua-template --clone --fork-name mi-archivo
cd mi-archivo

npm install          # descarga el motor @ucsb-ampl/zasqua y sus herramientas
npm run build        # construye los datos de muestra incluidos en public/
npm run dev          # sirve una vista previa en http://localhost:1313
```

`npm install` descarga el motor (`@ucsb-ampl/zasqua`) y todo lo que necesita
(Hugo Extended, Pagefind, Tailwind) del registro de npm. Actualizas el motor
subiendo su versión en `package.json` y reinstalando, no sincronizando el
fork. Tu fork solo guarda tu configuración, tus datos y tus personalizaciones
de tema.

## Qué hay en este repositorio

| Ruta | Qué es |
|------|--------|
| `package.json` | Declara el motor de Zasqua como dependencia |
| `hugo.toml` | Configuración de Hugo y los textos de identidad de tu sitio |
| `zasqua.manifest.toml` | Qué módulos están activos (jerarquía, entidades, lugares, …) |
| `exports/` | El contrato de datos de seis archivos — datos de muestra que reemplazas |
| `content/colofon/` | La página de colofón (declaración institucional) |

Los datos de muestra son material archivístico real y publicado (mira
`NOTICE`). Reemplaza los archivos de `exports/` con los tuyos antes de
publicar.

## Configura tu instancia

1. **Identidad** — define el nombre del sitio, los enlaces y el texto del pie
   de página en el bloque `[params]` de `hugo.toml`.
2. **Idioma** — define el idioma de la interfaz en `zasqua.manifest.toml`
   (`[ui] language`): `en-US` o `es-CO`. Esa sola línea cambia toda la
   interfaz; no tienes que tocar `hugo.toml` para eso.
3. **Módulos** — activa o desactiva funciones en `zasqua.manifest.toml` y
   luego ejecuta `npm run validate` para confirmar que tus datos coinciden.
4. **Datos** — coloca tus seis archivos JSON en `exports/`. Ejecuta
   `npx zasqua init` para generar un manifiesto a partir de datos que ya
   tengas.
5. **Personalización** — para cambiar colores, tipografías y plantillas,
   agrega un tema de personalización. Hasta que lo hagas, el sitio funciona
   con el tema base neutro del motor.
6. **Colofón** — edita `content/colofon/_index.md` con la declaración de
   derechos, procedencia y licencia de tu institución.

## Alojamiento

`npm run build` genera un sitio estático en `public/`: HTML, JSON e imágenes
con búsqueda del lado del cliente, sin servidor ni base de datos. Alójalo
donde quieras: copia `public/` a Netlify, Vercel, GitHub Pages, Cloudflare
Pages o cualquier servidor web estático. La guía de despliegue completa
—contrato de datos, validación, personalización y alojamiento— está en el
repositorio del motor:

> https://github.com/UCSB-AMPLab/zasqua — mira `docs/guide.md`.

## Licencia

Esta plantilla se publica bajo la **Licencia Pública General Affero de GNU
v3.0** (`LICENSE`). El motor también es AGPL-3.0. Mira `NOTICE` para
la atribución de los datos de muestra incluidos.
