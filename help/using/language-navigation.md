---
title: Language Navigation Component
seo-title: Language Navigation Component
description: null
seo-description: The language navigation component provides a language/country navigation for a site, so that visitors can navigate to the same page in a different locale.
uuid: ce736458-9cdf-4bc2-b90f-9c5a62fe1ca0
content-type: reference
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 8f232eb0-65d5-4075-8668-75f1366882c8
disttype: dist5
gnavtheme: light
groupsectionnavitems: no
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
---

# Language Navigation Component{#language-navigation-component}

The Language Navigation Component provides a language/country navigation for a site, so that visitors can navigate to the same page in a different locale.

## Usage {#usage}

Websites are often provided in multiple languages for different regions. The language navigation component allows a visitor to view the same page in different languages/locales. So if you are a reader on the Swiss German version of the website, you can easily switch to the US English version of the same page. The Language Navigation component handles understanding the site language stucture and finds the corresponding page autoamtically.

The [edit dialog](#edit-dialog) allows the definition of the global site navigation root as well as how deep into the structure the navigation should go. Using the [design dialog](#design-dialog), the template author can set the default values for the same options.

## Version and Compatibility {#version-and-compatibility}

The current version of the Language Navigation Component is v1, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.3|AEM 6.4|AEM 6.5|
|--- |--- |--- |--- |
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## Technical Details {#technical-details}

The latest technical documentation about the Language Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Design Dialog {#design-dialog}

The edit dialog allows the definition of the global site navigation root as well as how deep into the structure the navigation should go.

Typically these configurations only need to be done at the page template leve. However, they can be changed on the page level via the [edit dialog](#edit-dialog).

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Navigation Root**
  * This is where the langauge navigation of the site should start.
  * The language structure of the site begins on the next level below this root.
* **Language Structure Depth**
  * This is how many levels of the content tree below the **Navigation Root** represent the language structure of the site. Examples:
    * `1` typically means that you only have the choice of language.
    * `2` typcially means that you have a choice of language and country.
    * `3` typically means that you have a choice of langauge, country, and region.

#### Example {#example}

Let's say that your content looks something like this:

```
/content
+-- we-retail
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

For the site We.Retail, you would probably want to place the Language Navigation component on a page template as part of the header. Once part of the template, you can set the **Navigation Root** of the component to `/content/we-retail` since that is where your localized content for that site begins. You would also want to set the **Language Structure Depth** to be `2` since your structure is of two levels (country then laguage).

With the **Navigation Root** value, the Language Component knows that after `/content/we-retail` that that the navigation begins and it can generate language navigation options by recognizing the next two levels in the content tree as the site's language navigation structure (as defined by the **Language Structure Depth** value).

No matter what page a user is viewing, the Language Navigation component is able find the corresponding page in another language, by knowing the location of the current page and working backwards to the root, and then forwards to the corresponding page.

### Styles Tab {#styles-tab}

The Language Navigation Component supports the AEM [Style System](authoring.md#component-styling).

## Edit Dialog {#edit-dialog}

Typically the Langauge Navigation component only needs to be added to and configured on the page templates of a site. However if the Language Navigation component needs to be added to an individual content page, the edit dialog allows a content author to configure the same values as described in the [design dialog](#design-dialog).

![](assets/screen_shot_2018-01-12at133353.png)
