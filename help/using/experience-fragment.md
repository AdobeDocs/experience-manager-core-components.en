---
title: Experience Fragment Component
seo-title: Experience Fragment Component
description: The Experience Fragment Component allows the content author to add an experience fragment variation to a page.
seo-description: The Experience Fragment Component allows the content author to add an experience fragment variation to a page.
content-type: reference
topic-tags: authoring
topic-tags: core-components
index: y
internal: n
---
# Experience Fragment Component{#experience-fragment-component}

The Core Component Experience Fragment Component allows the content author to place an experience fragment variation on a page while supporting a localized site structure.

## Usage {#usage}

The Core Component Experience Fragment Component allows the content author to select from existing experience fragment varations and place one on the content page. The Experience Fragment component also supports a localized site structure.

* The components's properties can be defined in the [configure dialog](#configure-dialog).
* Defaults for the component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Localized Site Structure Support {#localized-site-structure}

The Experience Fragment Component can be adaptive to the localized site structure and render the proper experience fragment based on the localization of the page. To do this, the experience fragment must meet the following conditions.

* The Experience Fragment Component is added to a template.
* That template is used to create a new content page that is part of a localized structure below `/content`.
* The experience fragment referenced on the content page is part of a localized experience fragment structure below `/content/experience-fragments` that follows the same patterns as the site below `/content`.

In this case, the fragment with the same localization (language, blueprint, or live copy) as the current page will be rendered.

### Example {#example}

Let's say that your content looks something like this:

```
/content
+-- experience-fragments
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Notice that the structure of the experience fragments mirror the structure of the We.Retail content.

In this case, if the Experience Fragment component is placed on a template and references an experience fragment varation under `/content/experience-fragments/language-masters`, the localized pages created based on that template will automatically render the localized experience fragment for that corresponds to the localized content page.

## Version and Compatibility {#version-and-compatibility}

The current version of the Experience Fragment Component is v1, which was introduced with release 2.6.0 of the Core Components in August 2019, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.3|AEM 6.4|AEM 6.5|
|--- |--- |--- |---|
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Experience Fragment Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/experience-fragment.html).

## Technical Details {#technical-details}

The latest technical documentation about the Experience Fragment Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/experience-fragment/v1/experience-fragment).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to select the experience fragment variation that should be rendered on the page.

![](assets/screen-shot-2019-08-23-10.49.21.png)

Use the **Open Selection Dialog** button to open the component selector to choose which experience fragment component variation to add to the content page.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Accordion Component and the defaults set when placing the Accordion Component.

![](assets/screen-shot-2019-08-23-10.48.36.png)

The Accordion Component supports the AEM [Style System](authoring.md#component-styling).