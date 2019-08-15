---
title: AEM Project Archetype
seo-title: AEM Project Archetype
description: A project template for AEM-based applications
seo-description: A project template for AEM-based applications
contentOwner: bohnert
content-type: reference
topic-tags: authoring
topic-tags: core-components
---

# AEM Project Archetype {#aem-project-archetype}

The AEM Project Archetype creates a minimal, best-practices-based Adobe Experience Manager project as a starting point for your own AEM projects. The properties that must be provided when using this archetype allow you to specify the names for all parts of this project as well as control certain optional features.

>[!NOTE]
>The latest AEM Project Archetype and full technical details [can be found on GitHub](https://github.com/adobe/aem-project-archetype).

>[!NOTE]
>See the [Getting Started with AEM Sites - WKND Tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) in the AEM documentation for an example of how to use the archteype.

## Features {#features}

The archetype has a number features that are intended to offer a convenient starting point for new AEM projects:

* English and French pages with example content
* A content template based on the editable template feature with example content policy
* Page component based on the [AEM Page Core Component](page.md)
* Examples of content components implemented with the recommended proxy pattern and an example helloworld custom component all based on [AEM Core Components](introduction.html).
* Examples of [form components](form-container.md)
* Configurations for device emulators, drag-and-drop setup, and internationalization
* Client libraries following BEM naming conventions as well as component-specific styles
* Example bundles including sample models, servelets, filters, and schedulers
* Unit, integration, and client-side tests

## Why Use the Archetype {#why-use-the-archetype}

Using the AEM Project Archetype sets you on the path towards building a best-practices-based AEM project with just a few keystrokes. All of the pieces are already in place so that while the resulting project is minimal, it already implements all of the [key features](#features) of AEM so that you simply must build on top and extend.

Of course there are many elements that go into a successful AEM project, but using the AEM Project Archetype is a sound foundation and is strongly recommended for any AEM project.

## What You Get Using the Archetype {#what-you-get}

The AEM Archetype is made up of modules:

* **core**: is a Java bundle containing all core functionality like OSGi services, listeners, and schedulers, as well as component-related Java code such as servlets and request filters.
* **ui.apps**: contains the `/apps` and `/etc` parts of the project, i.e. JS and CSS clientlibs, components, templates, runmode-specific configs, as well as Hobbes tests.
* **ui.content**: contains sample content using the components from the ui.apps module.
* **ui.tests**: is a Java bundle containing JUnit tests that are executed server-side. This bundle is not to be deployed onto production.
* **ui.launcher**: contains glue code that deploys the ui.tests bundle (and dependent bundles) to the server and triggers the remote JUnit execution.

## Requirements

The current version of the archetype has the following requirements:

* Adobe Experience Manager 6.3.3.0 or higher
* Apache Maven (3.3.9 or newer)
* Adobe Public Maven Repository in maven settings, see this [Knowledge Base article for details](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

For a list of supported AEM versions of previous archetype versions, see the [historical supported AEM versions](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md).

## How to Use the Archetype {#how-to-use-the-archetype}

To get started you can most simply use the [AEM Eclipse extension](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/aem-eclipse.html) and follow the New Project wizard and choosing **AEM Sample Multi-Module Project** to use a released version of the archetype.

Of course you can also invoke Maven directly.

```
mvn archetype:generate \
 -DarchetypeGroupId=com.adobe.granite.archetypes \
 -DarchetypeArtifactId=aem-project-archetype \
 -DarchetypeVersion=XX
```

Where `XX` is the [version number](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) of the latest AEM Project Archetype.

### Properties

The following properties are available when using the artchetpye.

Name                        | Default | Description
----------------------------|---------|--------------------
`groupId`                     |         | Base Maven `groupId`
`artifactId`                  |         | Base Maven ArtifactId
`version`                     |         | Version
`package`                     |         | Java Source Package
`appsFolderName`              |         | `/apps` folder name
`artifactName`                |         | Maven Project Name
`componentGroupName`          |         | AEM component group name
`contentFolderName`           |         | `/content` folder name
`confFolderName`              |         | `/conf` folder name
`cssId`                       |         | prefix used in generated css
`packageGroup`                |         | Content Package Group name
`siteName`                    |         | AEM site name
`optionAemVersion`            |  6.5.0  | Target AEM version
`optionIncludeExamples`       |    y    | Include a Component Library example site
`optionIncludeErrorHandler`   |    n    | Include a custom 404 response page
`optionIncludeFrontendModule` |    n    | Include a dedicated frontend module

>[!NOTE]
> If the archetype is executed in interactive mode the first time, properties with default values can't be changed (see [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) for more details). The value can be changed when the property confirmation at the end is denied and the questionnaire gets repeated, or by passing the parameter in the command line (e.g. `-DoptionIncludeExamples=n`).

### Profiles

The generated maven project support different deployment profiles when running `mvn install` within the reactor.

Profile ID                        | Description
--------------------------|------------------------------
`autoInstallBundle`         | Installs core bundle with the maven-sling-plugin to the felix console
`autoInstallPackage`        | Installs the ui.content and ui.apps content package with the content-package-maven-plugin to the package manager to the default author instance on localhost, port 4502. Hostname and port can be changed with the `aem.host` and `aem.port` user-defined properties.
`autoInstallPackagePublish` | Install the ui.content and ui.apps content package with the content-package-maven-plugin to the package manager to default publish instance on localhost, port 4503. Hostname and port can be changed with the `aem.host` and `aem.port` user-defined properties.
`integrationTests` | Runs the provided integration tests on the AEM instance (only for the `verify` phase)

### Building and Installing

To build all the modules run in the project root directory, use the following Maven command.

```
mvn clean install
```

If you have a running AEM instance, you can build and package the whole project and deploy into AEM with the following Maven command.

```
mvn clean install -PautoInstallPackage
```

To deploy it to a publish instance, run this command.

```
mvn clean install -PautoInstallPackagePublish
```

Alternatively, to deploy to a publish instance, run this command.

```
mvn clean install -PautoInstallPackage -Daem.port=4503
```

Or to deploy only the bundle to the author, run this command.

```
mvn clean install -PautoInstallBundle
```

## Testing

There are three levels of testing contained in the project and because they are different types of tests, they are executed in different ways or in different places.

* Unit test in core: This showcases classic unit testing of the code contained in the bundle. To test, execute:
  * `mvn clean test`
* Server-side integration tests: These run unit-like tests in the AEM-environment, i.e. on the AEM server. To test, execute:
  * `mvn clean verify -PintegrationTests`
* Client-side Hobbes.js tests: These are JavaScript-based browser-side tests that verify browser-side behavior. To test:
  1. Load AEM in your browser as you would to author a page.
  1. Open the page in [Developer mode](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/developer-mode.html)
  1. Open the left panel and switch to the **Tests** tab.
  1. Find the generated **MyName Tests** and run them.

## Next Steps

So you have built and installed the AEM Project Archteype. What now? Well, the archetype is small, but consists of many examples of powerful AEM features configured according to recommended best practices. Use these are indicatory of how you can leverage these features in your project. For any project you likely need to:

* [Customize components be extending the existint core components](customizing.md)
* [Add additional templates](https://helpx.adobe.com/content/help/en/experience-manager/6-5/sites/authoring/using/templates.html)
* [Adapt the localization structure](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/tc-prep.html)

## Front End Build

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

### Installation

1. Install [NodeJS](https://nodejs.org/en/download/) (v10+), globally. This will also install npm.
1. Navigate to ui.frontend in your project and run `npm install`.

### Usage

The following npm scripts drive the frontend workflow:

`npm run dev` - full build with JS optimization disabled (tree shaking, etc) and source maps enabled and CSS optimization disabled.
`npm run prod` - full build with JS optimization enabled (tree shaking, etc), source maps disabled and CSS optimization enabled.

### Output

#### General

* Site - site.js and site.css are created in a clientlib-site folder.
* Dependencies - dependencies.js and dependencies.css are created in a clientlib-dependencies folder.

#### JavaScript

* Optimization - for production builds, all JS that is not being used or called is removed.

#### CSS

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
