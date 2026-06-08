---
# Colophon page content — deployer-editable institutional prose.
#
# This is sample scaffold content for the starter template. Every section
# below is institution-specific prose that you, the deployer, should
# replace with your own: who publishes the archive, which collections it
# represents, how to cite it, the technology and license, and how to get
# in touch. It is authored HERE as a Hugo markdown content page, not in a
# theme template — the engine base template
# (themes/base/layouts/colofon/list.html) renders this page's .Content
# inside a prose-styled article.
#
# Three dynamic values stay out of the prose, supplied by engine
# shortcodes so a version bump re-renders only this page:
#   {{< version >}}        -> your instance version (hugo.toml [params] version)
#   {{< engine-version >}} -> the Zasqua engine version, stamped at build time
#   {{< year >}}           -> the current build year
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
