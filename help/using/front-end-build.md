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

The AEM Project Archetype includes an optional dedicated front-end build mechanism based on Webpack. To fully take advantage of this powerful and flexible feature, it is important to understand how front-end development fits into an AEM project.

## AEM Projects and Front-End Development {#aem-and-front-end-development}

In greatly-simplified terms, AEM projects can be thought of as consisting of two separate but related parts:

* Back-end development that drives the logic of AEM and produces Java libraries, OSGi services, etc.
* Front-end development that drives the presentation and behavior of the resulting web site to the user and produces Javascript and CSS libraries

Because these two development processes are focused on different parts of the project, back-end and front-end development can happen in parallel.

![](assets/front-end-flow.png)

However, any resulting project needs to use the output of both of these development efforts i.e. both back-end and front-end.

Running `npm run dev` starts the front-end build process that gathers the Javascript and CSS files and produces client libraries or clientlibs. clientlibs are deployable to AEM and allow you to store your client-side code in the repository, organize it into categories, and define when and how each category of code is to be served to the client.

When the entire AEM project archetype is run using `mvn clean install -pautoinstallPackage` all project artifacts including the clientlibs are then pushed to the AEM instance.

>[!TIP]
>Learn more about clientlibs in the [AEM development documentation](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

## Possible Front-End Development Workflows {#possible-workflows}

The front-end build module is a useful and very flexible tool, but imposes no particular opinion on how it should be used. The following are two examples of possible usage, but your individual project needs may dictate other use cases.

### Using Webpack Static Development Server {#using-webpack}

Using Webpack you can style and develop based on static output of AEM webpages within the ui.frontend module.

1. Preview page in AEM using page preview mode or passing in `wcmmode=disabled` in the URL
1. View page source and save as static HTML within the ui.frontend module
1. Start webpack and begin styling and generating the necessary Javascript and CSS
1. Run `npm run dev` to generate the clientlibs

In this flow, an AEM developer may perform steps one and two and pass the static HTML off to the front-end developer.

### Using Storybook {#using-storybook}

Using [Storybook](https://storybook.js.org) you can perform more atomic front-end development. Storybook artifacts can be stored wtihin the ui.frontend module and when ready for testing within AEM can be deployed as clientlibs by running `npm run dev`.

### Determining the Markup {#determining-markup}

Whichever front-end development workflow you decide to implement for your project, the back-end developers and front-end developers must first agree on the markup. Typically AEM defines the markup, which is provided by the core components. However this can be customized if necessary by the back-end developer.

## The ui.frontend Module {#ui-frontend-module}

The AEM Project Archetype includes an optional dedicated front-end build mechanism based on Webpack with the following features.

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

* `npm run dev` - full build with JS optimization disabled (tree shaking, etc) and source maps enabled and CSS optimization disabled.
* `npm run prod` - full build with JS optimization enabled (tree shaking, etc), source maps disabled and CSS optimization enabled.

## Output {#output}

### General {#general}

* Site - `site.js` and `site.css` are created in a clientlib-site folder.
* Dependencies - `dependencies.js` and `dependencies.css` are created in a clientlib-dependencies folder.

### JavaScript {#javascript}

* Optimization - For production builds, all JS that is not being used or called is removed.

### CSS {#css}

* Autoprefixing - All CSS is run through a prefixer and any properties that require prefixing will automatically have those added in the CSS.
* Optimization - At post, all CSS is run through an optimizer (cssnano) which normalizes it according to the following default rules:
  * Reduces CSS calc expression wherever possible, ensuring both browser compatibility and compression
Converts between equivalent length, time and angle values. Note that by default, length values are not converted.
  * Removes comments in and around rules, selectors & declarations
  * Removes duplicated rules, at-rules and declarations
    * Note that this only works for exact duplicates.
  * Removes empty rules, media queries and rules with empty selectors, as they do not affect the output
  * Merges adjacent rules by selectors and overlapping property/value pairs
  * Ensures that only a single @charset is present in the CSS file and moves it to the top of the document
  * Replaces the CSS initial keyword with the actual value, when the resulting output is smaller
  * Compresses inline SVG definitions with SVGO
* Cleaning - Includes explicit clean task for wiping out the generated CSS, JS and Map files on demand.
* Source Mapping - development build only

>[!NOTE]
>The front end build option utilizes dev-only and prod-only webpack config files that share a common config file. This way the development and production settings can be modified independently.
