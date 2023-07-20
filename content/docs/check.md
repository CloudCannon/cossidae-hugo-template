---
_schema: default
title: Rosey Check
nav_title: Rosey Check
nav_section: Rosey CLI
weight: 13
draft: false
---
Rosey's `check` command compares your `base.json` translation file against your `rosey/locales/*` locale files. This command will highlight any translations that are missing in your locale files, as well as any translations that are out of date and need to be updated.

## Options

### Base

The path to read the Rosey base locale file from. Defaults to `rosey/base.json`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--base &lt;FILE&gt;</code></td><td><code>ROSEY_BASE</code></td><td><code>base</code></td></tr></tbody></table>

### Locales

The directory to read translated Rosey locale files from. Defaults to `rosey/locales`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--locales &lt;DIR&gt;</code></td><td><code>ROSEY_LOCALES</code></td><td><code>locales</code></td></tr></tbody></table>