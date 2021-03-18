---
title: Language Navigation Component
description: The language navigation component provides a language/country navigation for a site, so that visitors can navigate to the same page in a different locale.
role: Architect, Developer, Administrator, Business Practitioner
---

# Language Navigation Component{#language-navigation-component}

The Language Navigation Component provides a language/country navigation for a site, so that visitors can navigate to the same page in a different locale.

## Usage {#usage}

Websites are often provided in multiple languages for different regions. The language navigation component allows a visitor to view the same page in different languages/locales. So if you are a reader on the Swiss German version of the website, you can easily switch to the US English version of the same page. The Language Navigation component handles understanding the site language structure and finds the corresponding page automatically.

* For an example of how the localization feature of the Language Navigation Component works, see [the section below](#example).
* For an example of how the localization features of the other Core Components work together, see the [Localization Features of the Core Components page](/help/get-started/localization.md).

The [edit dialog](#edit-dialog) allows the definition of the global site navigation root as well as how deep into the structure the navigation should go. Using the [design dialog](#design-dialog), the template author can set the default values for the same options.

## Version and Compatibility {#version-and-compatibility}

The current version of the Language Navigation Component is v1, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_langnav).

## Technical Details {#technical-details}

The latest technical documentation about the Language Navigation Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Design Dialog {#design-dialog}

The edit dialog allows the definition of the global site navigation root as well as how deep into the structure the navigation should go.

Typically these configurations only need to be done at the page template level. However, they can be changed on the page level via the [edit dialog](#edit-dialog).

### Properties Tab {#properties-tab}

![Language Navigation Component's design dialog](/help/assets/language-navigation-design.png)

* **Navigation Root**
  * This is where the language navigation of the site should start.
  * The language structure of the site begins on the next level below this root.
* **Language Structure Depth**
  * This is how many levels of the content tree below the **Navigation Root** represent the language structure of the site. Examples:
    * `1` typically means that you only have the choice of language.
    * `2` typically means that you have a choice of language and country.
    * `3` typically means that you have a choice of language, country, and region.

#### Example {#example}

Let's say that your content looks something like this:

```
/content
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

For the site WKND, you would probably want to place the Language Navigation component on a page template as part of the header. Once part of the template, you can set the **Navigation Root** of the component to `/content/wknd` since that is where your localized content for that site begins. You would also want to set the **Language Structure Depth** to be `2` since your structure is of two levels (country then language).

With the **Navigation Root** value, the Language Component knows that after `/content/wknd` that that the navigation begins and it can generate language navigation options by recognizing the next two levels in the content tree as the site's language navigation structure (as defined by the **Language Structure Depth** value).

No matter what page a user is viewing, the Language Navigation component is able find the corresponding page in another language, by knowing the location of the current page and working backwards to the root, and then forwards to the corresponding page.

### Styles Tab {#styles-tab}

The Language Navigation Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Edit Dialog {#edit-dialog}

Typically the Language Navigation component only needs to be added to and configured on the page templates of a site. However if the Language Navigation component needs to be added to an individual content page, the edit dialog allows a content author to configure the same values as described in the [design dialog](#design-dialog).

Additionally you can set an **ID**. This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).

* If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
* If an ID is specified, it is the responsibility of the author to make sure that it is unique.
* Changing the ID can have an impact on CSS, JS and Data Layer tracking.

![Language Navigation Component's edit dialog](/help/assets/language-navigation-edit.png)

## Adobe Client Data Layer {#data-layer}

The Language Navigation Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
