---
_schema: default
title: Rosey Build
nav_title: Rosey Build
nav_section: Rosey CLI
weight: 12
draft: false
---
Rosey's `build` command ingests your built static site along with any locale files, and produces a multilingual site ready to deploy.

## CLI flags

### Serve

Runs a local webserver on the dest folder after a successful build.

<table><thead><tr><th>CLI Flag</th></tr></thead><tbody><tr><td><code>--serve</code></td></tr></tbody></table>

## Required options

### Source

The directory of your built static website (the output folder of your SSG build).

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--source &lt;SOURCE&gt;</code></td><td><code>ROSEY_SOURCE</code></td><td><code>source</code></td></tr></tbody></table>

## Options

### Dest

The directory to output the multilingual site to. Defaults to your source directory suffixed with `_translated`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--dest &lt;DIR&gt;</code></td><td><code>ROSEY_DEST</code></td><td><code>dest</code></td></tr></tbody></table>

### Locales

The directory to read translated Rosey locale files from. Defaults to `rosey/locales`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--locales &lt;DIR&gt;</code></td><td><code>ROSEY_LOCALES</code></td><td><code>locales</code></td></tr></tbody></table>

### Default language

The default language for the site (i.e. the language of 'source.json'). Defaults to `en`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--default-language &lt;STRING&gt;</code></td><td><code>ROSEY_DEFAULT_LANGUAGE</code></td><td><code>default_language</code></td></tr></tbody></table>

### Exclusions

A regular expression used to determine which files not to copy as assets. Defaults to `\.(html?|json)$`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--exclusions &lt;REGEX&gt;</code></td><td><code>ROSEY_EXCLUSIONS</code></td><td><code>exclusions</code></td></tr></tbody></table>

### Images source

The source folder that Rosey should look for translated images within. If omitted, Rosey will look for images in the source folder.

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--images-source &lt;DIR&gt;</code></td><td><code>ROSEY_IMAGES_SOURCE</code></td><td><code>images_source</code></td></tr></tbody></table>

### Redirect page

Path to a custom redirect template that Rosey should use for the base URL.

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--redirect-page &lt;FILE&gt;</code></td><td><code>ROSEY_REDIRECT_PAGE</code></td><td><code>redirect_page</code></td></tr></tbody></table>

### Separator

The separator that was used between Rosey namespaces when generating keys. Defaults to `:`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--separator &lt;CHAR&gt;</code></td><td><code>ROSEY_SEPARATOR</code></td><td><code>separator</code></td></tr></tbody></table>

### Tag

The HTML attribute prefix that Rosey should read from. Defaults to `data-rosey`

<table><thead><tr><th>CLI Flag</th><th>ENV Variable</th><th>Config Key</th></tr></thead><tbody><tr><td><code>--tag &lt;STRING&gt;</code></td><td><code>ROSEY_TAG</code></td><td><code>tag</code></td></tr></tbody></table>