---
title: Experience Fragment Component
description: The Experience Fragment Component allows the content author to add an experience fragment variation to a page.
role: Architect, Developer, Admin, User
exl-id: 103f729a-084d-4b6a-a239-d8ef8902eb95
---
# Experience Fragment Component{#experience-fragment-component}

The Core Component Experience Fragment Component allows the content author to place an experience fragment variation on a page while supporting a localized site structure.

## Usage {#usage}

The Core Component Experience Fragment Component allows the content author to select from existing experience fragment variations and place one on the content page. The Experience Fragment component also supports a localized site structure.

* The component's properties can be defined in the [configure dialog](#configure-dialog).
* Defaults for the component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Localized Site Structure Support {#localized-site-structure}

The Experience Fragment Component is adaptive to localized site structures and renders the proper experience fragment based on the localization of the page. To do this, the experience fragment must meet the following conditions.

* The Experience Fragment Component is added to a template.
* That template is used to create a new content page that is part of a localized structure below `/content/<site>`.
* The experience fragment referenced on a content page is part of a localized experience fragment structure below `/content/experience-fragments` that follows the same patterns as the site below `/content/<site>` including using the same component names.

In this case, the fragment with the same localization (language, blueprint, or live copy) as the current page will be rendered as part of the template.

This behavior is limited to Experience Fragment Components added to templates. Experience Fragment Components added to individual content pages will render the exact experience fragment renditions configured within the component.

* For an example of how the localization features of the Experience Fragment Component works, see [the section below](#example).
* For an example of how the localization features of the Core Components work together, see the [Localization Features of the Core Components page](/help/get-started/localization.md).

### Example {#example}

Let's say that your content looks something like this:

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
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

Notice that the structure below `/content/experience-fragments/wknd` mirrors the structure of `/content/wknd`.

In this case, if the Experience Fragment component `/content/experience-fragments/wknd/us/en/footerTextXf` is placed on a template, the localized pages created based on that template will automatically render the localized experience fragment that corresponds to the localized content page.

So if you navigate to a content page under `/content/wknd/ch/de` that uses the same template, `/content/experience-fragments/wknd/ch/de/footerTextXf` will be rendered instead of `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

The Experience Fragment Component will attempt to find a corresponding localized component in the following order.

1. First it tries to find a language root.
1. If not found, it tries to find a blueprint.
1. If not found, it tries to find a live copy.
1. If not found, it defaults to the experience fragment configured in the component.

## Version and Compatibility {#version-and-compatibility}

The current version of the Experience Fragment Component is v1, which was introduced with release 2.6.0 of the Core Components in September 2019, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Experience Fragment Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_xf).

## Technical Details {#technical-details}

The latest technical documentation about the Experience Fragment Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to select the experience fragment variation that should be rendered on the page.

![Experience Fragment Component's edit dialog](/help/assets/experience-fragment-edit.png)

Use the **Open Selection Dialog** button to open the component selector to choose which experience fragment component variation to add to the content page.

If you add the Experience Fragment Component to a template, note that it will be automatically localized provided that the Experience Fragments are localized, so what is rendered on the page may vary from the component you explicitly select. [See the example above](#example) for more information.

You can also define an **ID**. This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).

* If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
* If an ID is specified, it is the responsibility of the author to make sure that it is unique.
* Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Experience Fragment Component and the defaults set when placing the Experience Fragment Component.

### Styles Tab {#styles-tab}

The Experience Fragment Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
