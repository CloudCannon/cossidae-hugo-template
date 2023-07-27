---
_schema: default
title: Configure the navigation and footer
nav_title: Configure the navigation and footer
nav_section: Customizing Alto
weight: 1
draft: false
---
You can easily configure Alto's Navigation and Footer items within CloudCannon.&nbsp;

## Configuring the navigation

Navigation in Alto is handled by front matter in Hugo, which can be easily edited in CloudCannon's Data Editor.

Each page has a 'Parent Section' property, which allows you to group related items in the sidebar.&nbsp;

You can also change the order of the page within the sidebar group using 'Weight'.

{{< figure src="/uploads/screenshot-2023-07-27-at-1-17-49-pm.png" title="Screenshot of Alto Page front matter in CloudCannon's Data Editor" >}}

## Configuring the footer

To configure the footer, use&nbsp;

Use the `data-rosey-attrs` attribute to translate HTML attributes on an element that already has a `data-rosey` tag. Multiple attributes can be translated by comma separation:

{{< diffcode >}}
```html
<!DOCTYPE html>
<html>
    <body>
        <h1 content="content text"
            alt="alt text"
            data-rosey="title"
+            data-rosey-attrs="content,alt"
        >Hello!</h1>
    </body>
</html>
```
{{< /diffcode >}}

<div class="c-card c-card--clickable"><div class="c-card__preview"><p class="u-hide-when-loaded">No preview available</p></div><div class="c-card__content"><div class="c-card__heading"><div class="c-card__icon"><cc-icon name="mdi:question_mark" class="u-hide-when-loaded"></cc-icon></div><div class="c-card__heading-content"><p class="c-card__text">Unknown Shortcode</p><p class="c-card__subtext">diffcode</p></div></div></div></div>

<img width="15" title="Click and drag to move" height="15" src="data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==" />



The name of the attribute will be appended to the `data-rosey` key with a period, thus the above example will produce the output translation keys:

```json
{
  "title":"Hello!",
  "title.content":"content text",
  "title.alt":"alt text",
}
```

## Explicitly tagging attributes

If you want to define a custom translation key, or want to tag an attribute on an element that is otherwise not translated, use the `data-rosey-attrs-explicit` attribute. This expects a JSON object of `<attribute>: <translation key>` pairs:

{{< diffcode >}}
```html
<!DOCTYPE html>
<html>
    <body>
        <img src="/img.png"
             content="My content text"
             alt="My alt text"
+             data-rosey-attrs-explicit='{"content":"content","alt":"alternative-text"}'
            />
        <h1 data-rosey="title">Hello!</h1>
    </body>
</html>
```
{{< /diffcode >}}

<div class="c-card c-card--clickable"><div class="c-card__preview"><p class="u-hide-when-loaded">No preview available</p></div><div class="c-card__content"><div class="c-card__heading"><div class="c-card__icon"><cc-icon name="mdi:question_mark" class="u-hide-when-loaded"></cc-icon></div><div class="c-card__heading-content"><p class="c-card__text">Unknown Shortcode</p><p class="c-card__subtext">diffcode</p></div></div></div></div>

<img width="15" title="Click and drag to move" height="15" src="data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==" />



The above example will produce the output translation keys:

```json
{
  "content":"My content text",
  "alternative-text":"My alt text",
  "title":"Hello!",
}
```