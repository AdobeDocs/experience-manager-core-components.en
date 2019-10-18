---
title: AEM Project Archetype Front-End Build
seo-title: AEM Project Archetype Front-End Build
description: A project template for AEM-based applications
seo-description: A project template for AEM-based applications
contentOwner: bohnert
content-type: reference
topic-tags: authoring
topic-tags: core-components
---

# AEM Project Archetype Front-End Build {#aem-project-archetype-front-end-build}

The AEM Project Archetype includes an optional dedicated front end build mechanism based on Webpack with the following features.

* Full TypeScript, ES6 and ES5 support (with applicable Webpack wrappers)
* TypeScript and JavaScript linting using a TSLint ruleset
* ES5 output, for legacy browser support
* Globbing
  * No need to add imports anywhere
  * All JS and CSS files can now be added to each component
    * Best practice is under `/clientlib/js`, `/clientlib/css`, or `/clientlib/scss`
  * No `.content.xml` or `js.txt`/`css.txt` files needed as everything is run through Webpack
  * The globber pulls in all JS files under the `/component/` folder.
    * Webpack allows CSS/SCSS files to be chained in via JS files.
    * They are pulled in through the two entry points, `sites.js` and `vendors.js`.
  * The only file consumed by AEM is the output files `site.js` and `site.css` in `/clientlib-site` as well as `dependencies.js` and `dependencies.css` in `/clientlib-dependencies`
* Chunks
  * Main (site js/css)
  * Vendors (dependencies js/css)
* Full Sass/Scss support (Sass is compiled to CSS via Webpack).

## Installation {#installation}

1. Install [NodeJS](https://nodejs.org/en/download/) (v10+), globally. This will also install npm.
1. Navigate to ui.frontend in your project and run `npm install`.

## Usage {#usage}

The following npm scripts drive the frontend workflow:

`npm run dev` - full build with JS optimization disabled (tree shaking, etc) and source maps enabled and CSS optimization disabled.
`npm run prod` - full build with JS optimization enabled (tree shaking, etc), source maps disabled and CSS optimization enabled.

## Output {#output}

### General {#general}

* Site - site.js and site.css are created in a clientlib-site folder.
* Dependencies - dependencies.js and dependencies.css are created in a clientlib-dependencies folder.

### JavaScript {#javascript}

* Optimization - for production builds, all JS that is not being used or called is removed.

### CSS {#css}

* Autoprefixing - all CSS is run through a prefixer and any properties that require prefixing will automatically have those added in the CSS.
* Optimization - at post, all CSS is run through an optimizer (cssnano) which normalizes it according to the following default rules:
  * Reduces CSS calc expression wherever possible, ensuring both browser compatibility and compression.
Converts between equivalent length, time and angle values. Note that by default, length values are not converted.
  * Removes comments in and around rules, selectors & declarations.
  * Removes duplicated rules, at-rules and declarations. Note that this only works for exact duplicates.
  * Removes empty rules, media queries and rules with empty selectors, as they do not affect the output.
  * Merges adjacent rules by selectors and overlapping property/value pairs.
  * Ensures that only a single @charset is present in the CSS file and moves it to the top of the document.
  * Replaces the CSS initial keyword with the actual value, when the resulting output is smaller.
  * Compresses inline SVG definitions with SVGO.
* Cleaning - explicit clean task for wiping out the generated CSS, JS and Map files on demand.
* Source Mapping - development build only.

>[!NOTE]
>The front end build option utilizes dev-only and prod-only webpack config files that share a common config file. This way the development and production settings can be modified independently.