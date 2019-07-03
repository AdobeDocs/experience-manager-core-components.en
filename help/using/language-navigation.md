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

Often websites are provided in multiple languages for different regions. The language navigation component allows a visitor to view the same page in different languages/locales.

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

## Edit Dialog {#edit-dialog}

The edit dialog allows the definition of the global site navigation root as well as how deep into the structure the navigation should go.

![](assets/screen_shot_2018-01-12at133353.png)

* **Navigation Root**
  Defines the root page of the navigation structure.
  * Use the **Open Selection Dialog** button to easily navigate the content structure and select the root.
* **Language Structure Depth**
  Depth of the global language structure relative to the navigation root.

## Design Dialog {#design-dialog}

Using the design dialog, the template author can set the default values for the same options available in the edit dialog.

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Navigation Root**
  Default value of the navigation root when a content author places the Language Switcher Component on a content page
* **Language Structure Depth**
  Default value of the language structure depth when a content author places the Language Switcher Component on a content page

### Styles Tab {#styles-tab}

The Language Navigation Component supports the AEM [Style System](authoring.md#component-styling).