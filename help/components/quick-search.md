---
title: Quick Search Component
description: The Quick Search Component provides search capabilities to a website and presents search results so that visitors can search the site and filter the results, optionally using AI-powered semantic search via the Semantic Search toggle.
role: Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
TQID: https://experienceleague.adobe.com/wU-3pacdEz9ne8b53-mKJy-XxRdyz2gu4Jvj-yFgGOw
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
---

# Quick Search Component {#quick-search-component}

The Quick Search Component provides search capabilities to a website and presents search results so that visitors can easily find matching content and view results.

{{traditional-aem}}

## Usage {#usage}

The Quick Search component offers site visitors the ability to search for content, view the results in-place, and easily navigate to the matching pages. New results are fetched dynamically as the user scrolls the search results.

The [edit dialog](#edit-dialog) allows the content author to define where in the content tree the search should start and optionally to hide the Semantic Search toggle. Using the [design dialog](#design-dialog), the template author can set the default value for where in the content tree the search should begin, the maximum result set size, the minimum search term length, and whether the Semantic Search toggle is shown to visitors by default.

## Version and Compatibility {#version-and-compatibility}

The current version of the Quick Search Component is v3, which was introduced with [release 2.32.0](/help/versions.md) of the Core Components adding an optional Semantic Search toggle, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|--- |--- |--- |---|---|
|v3|-|Compatible*|Compatible*|Compatible|
|[v2](/help/components/v2/quick-search.md)|-|Compatible|Compatible|Compatible|
|[v1](/help/components/v1/quick-search.md)|Compatible with<br>[release 2.17.4](/help/versions.md) and prior|Compatible|-|Compatible|

*The Semantic Search toggle is only available with AEM as a Cloud Service.

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Quick Search Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library.](https://adobe.com/go/aem_cmp_library_search)

## Technical Details {#technical-details}

>[!NOTE]
>
>Protecting the Search Component or any AEM based application against DOS attacks should be implemented at a higher level, for example by using `mod_security` on the dispatcher.

The latest technical documentation about the Quick Search Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_search_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to define where in the content tree the search should start and to optionally hide the Semantic Search toggle.

![Quick Search Component's edit dialog](/help/assets/quick-search-edit-v3.png)

**Search Root** - The root page from where to start the search. The Search Root can be a blueprint master, language master or regular page.
* **ID** - This option allows control of the unique identifier of the component in the HTML and in the [Data Layer.](/help/developing/data-layer/overview.md)
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.
* **Hide Semantic Search toggle on this instance** - When checked, the Semantic Search toggle is hidden, regardless of what the [design dialog](#design-dialog) is configured to show.
  * Leave unchecked to use the template's default.
  * This option can not force the toggle to show on a placement where the design dialog hides it.

>[!NOTE]
>
>If the **Search Root** is not configured or can not be resolved, the Quick Search defaults to searching beneath the current page.

>[!NOTE]
>
>The Semantic Search toggle only returns AI-powered results when the environment is configured with AEM Content AI. On AEM 6.5 and AEM 6.5 LTS environments that are not configured with Content AI, hide the toggle [using the design dialog](#design-dialog) so visitors aren't offered a search mode that isn't functional.

## Design Dialog {#design-dialog}

Using the design dialog, the template author can set the default value for where in the content tree the search should begin as well as a maximum result set size, minimum search term length, and whether the Semantic Search toggle is shown to visitors by default.

### Properties Tab {#properties-tab}

![Quick Search Component's design dialog](/help/assets/quick-search-design-v3.png)

* **Search Root** - The default value of search root when a content author places the Quick Search Component on a content page
* **Results Size** - The maximum number of results fetched by a search request
* **Search Term Minimum Length** - Minimum length of the search term to start the search
* **Hide Semantic Search Toggle** - When checked, the **Semantic Search** toggle described in [Usage](#usage) isn't shown to site visitors by default, and the component behaves like [the v2 (full-text search only) component.](/help/components/v2/quick-search.md)
  * Unchecked by default.
  * Content authors can also override this for an individual Quick Search Component in the [edit dialog.](#edit-dialog)

>[!NOTE]
>
>The Semantic Search toggle only returns AI-powered results when the environment is configured with AEM Content AI. On AEM 6.5 and AEM 6.5 LTS environments that are not configured with Content AI, hide the toggle using the design dialog so visitors aren't offered a search mode that isn't functional.

>[!NOTE]
>
>**Results Size** and **Search Term Minimum Length** can only be set in design mode and therefore only at the template level, meaning content authors are not able to modify these values.

>[!CAUTION]
>
>**Results Size** and **Search Term Minimum Length** can have performance impacts if they are set too high or too low, respectively.

### Styles Tab {#styles-tab}

The Quick Search Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
