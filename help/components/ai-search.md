---
title: Content AI Search Component
description: The Content AI Search component provides your site visitors with an generative AI-powered search.
role: Developer, Admin, User
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

# Content AI Search Component {#content-ai-search-component}

The Content AI Search component provides your site visitors with an generative AI-powered search.

{{traditional-aem}}

## Usage {#usage}

The Content AI Search component lets visitors search a [Content Source](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) directly from a page, and optionally see a generative AI-produced summary of the results. It combines a standard full-text/semantic search box with a toggle-able **Show AI-generated summary** panel powered by AEM Content AI.

The [edit dialog](#edit-dialog) allows the content author to define the content scope of hte search, search behavior, and generative settings. There is no design dialog as there are no settings available at the template level.

>[!NOTE]
>
>To use the Content AI Search Component, you must have access to a Content AI Source and your administrator must have enabled the component for your project. See the document [Configuring Content AI Search Component](/help/developing/ai-search.md) for more information.

## Version and Compatibility {#version-and-compatibility}

The current version of the Content AI Search Component is v1, which was introduced with release 2.32.0 of the Core Components in July 2026, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|---|---|---|---|---|
|v1|-|-|-|Ongoing|

For more information about Core Component versions and releases, see the document [Core Components Versions.](/help/versions.md)

## Sample Component Output {#sample-component-output}

To experience the Content AI Search Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library.](https://adobe.com/go/aem_cmp_library_ai_search)

## Technical Details {#technical-details}

The latest technical documentation about the Content AI Search Component [can be found on GitHub.](https://adobe.com/go/aem_cmp_tech_ai_search_v1)

Further details about developing Core Components can be found in the [Core Components developer documentation.](/help/developing/overview.md)

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to define the content scope of hte search, search behavior, and generative settings. There is no design dialog as there are no settings available at the template level.

### Content Scope Tab {#content-scope}

![Content Scope tab of edit dialog](/help/assets/content-ai-search-edit-content-scope.png)

* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer.](/help/developing/data-layer/overview.md)
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.
* **Content Source Type** - This field defines the type of content source. Selecting a type populates the **Content Source** drop-down with matching sources.
  * **ACQUISITION** - The default value used for public, anonymous-access sources indexed via a crawl/acquisition pipeline
  * **AEM_AUTHOR** - A Content-AI-side source whose content was ingested from an AEM author instance
  * **AEM_PUBLISH** -A Content-AI-side source whose content was ingested from an AEM publish instance
  * **CUSTOM** - A source registered outside AEM's own ingestion pipelines
* **Content Sources** - This defines the Content Source this component searches.
  * Available entries match Content Sources that already exist and are **Available** and also match the type set in **Content Source Type**
  * Please see the document [Set up and manage your Content AI Sources](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) for details.

### Search Behavior Tab {#search-behavior}

![Search Behavior tab of the edit dialog](/help/assets/content-ai-search-edit-search-behavior.png)

* **Results Layout** - This option defines how the search results are displayed to the visitor.
  * **Cards** - This option displays the results in a grid format.
  * **List** - This option displays the results in a list format.
* **Results Size** - Defines the number of results fetched per search request.
  * The default value is `12`.
  * Visitors can load more results when additional matches are available.
* **Placeholder Text** - This is the text shown in the empty search input field before the visitor enters a search query.

### Generative Search Tab {#generative-search}

![Generative Search tab of the edit dialog](/help/assets/content-ai-search-edit-generative-search.png)

* **Show generative summary toggle to visitors** - When unchecked, visitors can not change whether the AI summary is shown.
  * The default value is enabled.
* **Show generative summary by default** - This option controls the default state of the visitor-facing toggle for the AI-generated summary.
  * The default value is enabled.
* **GenSearch Error Fallback** - Defines how the search should behave or error.
  * **Results only (hide error)** - If there is an error, show only the results that were returned, not the error and no retry button. This is the default value.
  * **Show error with retry** - If there is an error, show the error with a retry button.
  * **Show error message only** - If there is an error, show only the error message, no results.
