---
title: Including Client Libraries
description: There are a number of different ways to include client libraries depending on your use case.
---

# Including Client Libraries {#including-client-libraries}

There are a number of different ways to include [client libraries](/help/developing/archetype/uifrontend.md#clientlibs) depending on your use case. This document provides examples and sample [HTL snippets](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) for each.

## Recommended Default Usage {#recommended-default-usage}

If you don't have time to investigate what's best in your situation, then include your client libraries by placing the following HTL lines inside your page `head` element:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

This will include both the CSS and the JS in your page `head`, but adding the `defer` attribute to your JS `script` includes, so that the browsers wait for the DOM to be ready before executing your scripts, and therefore optimizing the page load speed.

## Basic Usage {#basic-usage}

The basic syntax to include both JS and CSS of a client library category, which will generate all the corresponding CSS `link` elements and/or JS `script` elements, is as follows:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

To do the same for multiple client library categories at once, an array of strings can be passed to the `categories` parameter:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## CSS or JS Only {#css-js-only}

Frequently, one wants to place the CSS includes in the HTML `head` element, and the JS includes just before the closing of the `body` element.

In the `head`, to include only the CSS, and not the JS, use `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Before the `body` closing, to include only the JS, and not the CSS, use `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Attributes {#attributes}

To apply attributes to the generated CSS `link` elements and/or JS `script` elements, a number of parameters are possible:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base',
    media='print',
    async=true,
    defer=true,
    onload='console.log(\'loaded: \' + this.src)',
    crossorigin='anonymous'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

CSS `link` attributes that can be passed to `jsAndCssIncludes` and `cssIncludes`:

* `media`: string

JS `script` attributes that can be passed to `jsAndCssIncludes` and `jsIncludes`:

* `async`: boolean
* `defer`: boolean
* `onload`: string
* `crossorigin`: string

## Inlining {#inlining}

In some cases, either for optimization, or for email or [AMP,](amp.md) it might be required to inline the CSS or JS into the output of the HTML.

To inline the CSS, `cssInline` can be used, in which case you must write the surrounding `style` element:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Similarly, to inline the JS, `jsInline` can be used, in which case you must write the surrounding `script` element:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```
