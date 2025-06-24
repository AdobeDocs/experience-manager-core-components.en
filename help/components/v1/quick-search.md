---
title: Quick Search Component (v1)
description: The Quick Search Component provides search capabilities to a website and presents search results so that visitors can search the site and filter the results.
role: Architect, Developer, Admin, User
exl-id: 60a043b7-d82c-4bc1-b91a-b77f748f7bc2
index: n
---

# Quick Search Component (v1) {#quick-search-component}

The Quick Search Component provides search capabilities to a website and presents search results so that visitors can easily find matching content and view results.

## Usage {#usage}

The Quick Search component offers site visitors the ability to search for content, view the results in-place, and easily navigate to the matching pages. New results are fetched dynamically as the user scrolls the search results.

The [edit dialog](#edit-dialog) allows the content author to define where in the content tree the search should start. Using the [design dialog](#design-dialog), the template author can set the default value for where in the content tree the search should begin as well as a maximum result set size and minimum search term length.

## Version and Compatibility {#version-and-compatibility}

The current version of the Quick Search Component is v1, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v1|Compatible with<br>[release 2.17.4](/help/versions.md) and prior|Compatible|Compatible|

>[!CAUTION]
>
>This document describes v1 of the Quick Search Component.
>For details of the current version of the Quick Search Component, see the [Quick Search Component](/help/components/quick-search.md) document.

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

### Technical Details {#technical-details}

>[!NOTE]
>
>Protecting the Search Component or any AEM based application against DOS attacks should be implemented at a higher level, for example by using `mod_security` on the dispatcher.

The latest technical documentation about the Quick Search Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_search_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to define where in the content tree the search should start.

![Quick Search Component's edit dialog](/help/assets/quick-search-edit.png)

**Search Root** - The root page from where to start the search. The Search Root can be a blueprint master, language master or regular page.
* **ID** - This option allows control of the unique identifier of the component in the HTML and in the [Data Layer.](/help/developing/data-layer/overview.md)
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

>[!NOTE]
>
>If the **Search Root** is not configured or can not be resolved, the Quick Search defaults to searching beneath the current page.

## Design Dialog {#design-dialog}

Using the design dialog, the template author can set the default value for where in the content tree the search should begin as well as a maximum result set size and minimum search term length.The design dialog allows the template author to define which text formatting options are available to the content authors.

### Properties Tab {#properties-tab}

![Quick Search Component's design dialog](/help/assets/quick-search-design.png)

* **Search Root**
  The default value of search root when a content author places the Quick Search Component on a content page
* **Results Size**
  The maximum number of results fetched by a search request
* **Search Term Minimum Length**
  Minimum length of the search term to start the search

>[!NOTE]
>
>**Results Size** and **Search Term Minimum Length** can only be set in design mode and therefore only at the template level, meaning content authors are not able to modify these values.

>[!CAUTION]
>
>**Results Size** and **Search Term Minimum Length** can have performance impacts if they are set too high or too low, respectively.

### Styles Tab {#styles-tab}

The Quick Search Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
