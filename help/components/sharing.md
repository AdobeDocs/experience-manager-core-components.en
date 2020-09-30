---
title: Social Sharing Component
description: The Core Component Social Sharing Component is a Facebook and Pinterest sharing widget.
---

# Social Sharing Component{#social-sharing-component}

The Core Component Social Sharing Component is a Facebook and Pinterest sharing widget.

## Usage {#usage}

The Social Sharing Component adds Facebook and Pinterest sharing links to the page. It is often included in page headers or footers.

Unlike other components, the settings for the Social Sharing Component is done by the template author via [Initial Page properties](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) and by the content author via [Page Properties](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Version and Compatibility {#version-and-compatibility}

The current version of the Social Sharing Component is v1, which was introduced with release 1.0.0 of the Core Components, and is described in this document.

The following table details all supported versions of the component and the AEM versions with which the versions of the component is compatible.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Social Sharing Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_sharing).

### Technical Details {#technical-details}

The latest technical documentation about the Sharing Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

![Sharing Component's edit dialog](/help/assets/sharing-edit.png)

* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

Because sharing requires special page headers, any sharing must be enabled at the page level. Therefore, for the content author additional edit options for the sharing component are available through the sharing tab the [page properties](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Design Dialog {#design-dialog}

Because sharing requires special page headers, any sharing must be enabled at the page level. Therefore, for the template author the design options for the sharing component are available through the [initial page properties](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).
