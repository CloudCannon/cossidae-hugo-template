---
_schema: default
title: Rosey Generate
nav_title: Rosey Generate
nav_section: Rosey CLI
weight: 11
draft: false
---
Rosey's `generate` command ingests your built static site, and produces a `base.json` file containing all content that needs to be translated.

## Required options

### Source

The directory of your built static website (the output folder of your SSG build).

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--source &lt;SOURCE&gt;</code></td><td><code>ROSEY_SOURCE</code></td><td><code>source</code></td></tr></tbody></table>

## Options

### Base

The path to generate the Rosey base locale file to. Defaults to `rosey/base.json`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--base &lt;FILE&gt;</code></td><td><code>ROSEY_BASE</code></td><td><code>base</code></td></tr></tbody></table>

### Separator

The separator to use between Rosey namespaces when generating keys. Defaults to `:`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--separator &lt;CHAR&gt;</code></td><td><code>ROSEY_SEPARATOR</code></td><td><code>separator</code></td></tr></tbody></table>

### Tag

The HTML attribute prefix that Rosey should read from. Defaults to `data-rosey`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--tag &lt;STRING&gt;</code></td><td><code>ROSEY_TAG</code></td><td><code>tag</code></td></tr></tbody></table>

### Version

The Rosey locale version to generate and build from. Version 1 should only be used for compatibility with legacy sites. Defaults to version `2`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--version &lt;NUMBER&gt;</code></td><td><code>ROSEY_VERSION</code></td><td><code>version</code></td></tr></tbody></table>