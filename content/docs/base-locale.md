---
_schema: default
title: Using Snippets
nav_title: Using Snippets in Alto
nav_section: Root
weight: 2
draft: false
---
Alto comes with twelve pre-configured Snippets for a range of common documentation requirements:

* Summary divider
* Code blocks with syntax highlighting
* Figure
* GitHub Gist embed
* Front matter parameter
* Reference
* Relative reference
* Tweet embed
* Vimeo embed
* YouTube embed
* Diffcode formatter
* Tree diagram formatter

To use a Snippet within CloudCannon, click the 'Snippet' button in the Content Editor, and set your parameters.

## Adding your own Snippets

In order to&nbsp;

## Base locale file structure

A Rosey v2 base locale file looks like so:

```json
{
    "version": 2,
    "keys": {
        "title": {
            "original": "My Website",
            "pages": {
                "index.html": 1
            },
            "total": 1
        },
        "about:label": {
            "original": "About Me",
            "pages": {
                "index.html": 1,
                "about.html": 2
            },
            "total": 3
        }
    }
}
```

At the top level, `version` represents the Rosey locale version, and `keys` contains all content to be translated. `keys` is an object, with each top-level JSON key in this object representing a unique translation. These top-level keys (`title` and `about:label` in this example) can be used for translation memory between Rosey runs.

Looking at the `keys["about:label"]` object from the above example:

```json
{
    "original": "About Me",
    "pages": {
        "index.html": 1,
        "about.html": 2
    },
    "total": 3
}
```

Here `original` represents the value Rosey extracted from your HTML, and is the value that should be translated. The `pages` and `total` keys present some helpful metadata that isn't used by Rosey itself, but can be integrated into your translation process to provide extra context about the translation string.

Once you have this file, it's time to create Rosey locale files with your translations. See the [Translated Locale Files](/docs/locales/) documentation for how these should be created.