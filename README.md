# Zasqua starter template

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
npx zasqua build     # builds the bundled sample data into public/
npx zasqua dev       # serves a live preview at http://localhost:1313
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
2. **Modules** — enable or disable features in `zasqua.manifest.toml`, then
   run `npx zasqua validate` to confirm your data matches.
3. **Data** — put your six JSON export files in `exports/`. Run
   `npx zasqua init` to scaffold a manifest from data you already have.
4. **Branding** — to customize colours, fonts, and layouts, add an overlay
   theme. The site runs on the engine's neutral base theme until you do.
5. **Colophon** — edit `content/colofon/_index.md` with your institution's
   rights, provenance, and licensing statement.

## Full guide and hosting

The complete deployment guide — data contract, validation, theming, and
hosting (Netlify, Vercel, GitHub Pages, Cloudflare Pages, or any static
host) — lives in the engine repository:

> https://github.com/UCSB-AMPLab/zasqua — see `docs/guide.md`.

## License

This template is released under the **GNU Affero General Public License
v3.0** (`LICENSE`). The Zasqua engine is likewise AGPL-3.0. See `NOTICE`
for attribution of the bundled sample data.
