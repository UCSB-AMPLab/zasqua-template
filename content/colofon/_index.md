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
# EN: After the text of this page the engine adds the sections it builds from
# `exports/publisher.json` and `exports/repositories.json`: publisher, credits,
# represented archives, how to cite, license, privacy, takedown policy and
# contact, each one only when the records have its data.
#
# ES: Después del texto de esta página, el motor agrega las secciones que arma
# con `exports/publisher.json` y `exports/repositories.json`: «Responsable del
# sitio», «Créditos», «Archivos representados», «Cómo citar», «Licencia»,
# «Privacidad y datos», «Política de retiro de contenidos» y «Contacto», cada
# una solo cuando los registros traen los datos que necesita.
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

Say which version of this archive this is, where its source code is
published, and link to its release notes.

## Technology

This archive is a set of static files — HTML, JSON, and images — with
client-side search. It needs no application server or database at request
time, so it is inexpensive to host and straightforward to preserve.

## License

State the license that applies to your descriptions and digitized
materials. You can write it here, or in `terms_of_use` in
`exports/publisher.json`, which the engine shows under its own License
heading; if you use the file, delete this section.
