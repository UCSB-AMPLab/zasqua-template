---
# Colophon page content — deployer-editable institutional prose.
# Contenido de la página de colofón — prosa institucional que edita quien despliega.
#
# EN: This is sample scaffold content for the starter template. Every section
# below is institution-specific prose that you, the deployer, should replace
# with your own — and write it in your site's language (set [ui] language in
# zasqua.manifest.toml; also set the page title below). It is authored HERE as
# a Hugo markdown content page, not in a theme template — the engine base
# template (themes/base/layouts/colofon/list.html) renders this page's
# .Content inside a prose-styled article.
#
# ES: Este es contenido de muestra para la plantilla inicial. Cada sección de
# abajo es prosa específica de tu institución que tú, quien despliega, debes
# reemplazar con la tuya — y escríbela en el idioma de tu sitio (define [ui]
# language en zasqua.manifest.toml; cambia también el título de la página, más
# abajo). Se redacta AQUÍ como una página de contenido en markdown de Hugo, no
# en una plantilla del tema — la plantilla base del motor
# (themes/base/layouts/colofon/list.html) muestra el .Content de esta página
# dentro de un artículo con estilo de prosa.
#
# EN/ES: Three dynamic values stay out of the prose, via engine shortcodes, so
# a version bump re-renders only this page / Tres valores dinámicos quedan
# fuera de la prosa, mediante shortcodes del motor, para que un cambio de
# versión solo regenere esta página:
#   {{< version >}}        -> instance version / versión de la instancia
#   {{< engine-version >}} -> Zasqua engine version / versión del motor
#   {{< year >}}           -> current build year / año de construcción actual
#
# Version: v1.0.0
title: "Colophon"
---

This is a Zasqua archive. Replace this colophon with your own
institutional statement: describe the collection, who is responsible for
it, and the terms under which it is made available.

## Version and source

This site was published with version {{< engine-version >}} of the
[Zasqua engine](https://github.com/UCSB-AMPLab/zasqua), an open-source
tool for publishing archival descriptions as a static website. Because
Zasqua is licensed under the AGPL-3.0, the source code of the running
program is available to everyone who uses it.

## Represented archives

List the repositories and collections this site brings together, and say
a word about each holding institution.

## How to cite

Tell readers how you would like material from this archive cited, with an
example reference.

## Technology

This archive is a set of static files — HTML, JSON, and images — with
client-side search. It needs no application server or database at request
time, so it is inexpensive to host and straightforward to preserve.

## License and contact

State the license that applies to your descriptions and digitized
materials, and give a contact address for questions, corrections, and
takedown requests.
