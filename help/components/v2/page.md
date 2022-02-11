---
title: Page Component (v2)
description: The Page Component is an extensible page component designed to work with the template editor and allow page header/footer and structure components to be assembled with the template editor.
role: Architect, Developer, Admin, User
---

# Page Component (v2) {#page-component}

The Page Component is an extensible page component designed to work with the [template editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) and allows page header/footer and structure components to be assembled with the template editor.

## Usage {#usage}

The Page Component forms the basis of all pages designed with the Core Components as well as editable templates. By using the Page Component, headers, footers, and the structure of the page can be defined as a template using the other Core Components.

Using the [design dialog](#design-dialog), custom client-side libraries can be defined for the page. Unlike other components which have an edit dialog accessible directly from the component, because the Page Component is the page itself, the [edit dialog](#edit-dialog) of the Page Component is the page properties window.

## Version and Compatibility {#version-and-compatibility}

This document describes v2 of the Page Component, which was introduced with release 2.0.0 of the Core Components in January 2018.

>[!CAUTION]
>
>This document describes v2 of the Page Component.
>
>For details of the current version of the Page Component, see the [Page Component](/help/components/page.md) document.

## Progressive Web App Support {#pwa-support}

Release 2.15.0 of the Core Components introduced support for AEM as a Cloud Service's built-in [Progressive Web Apps (PWA) features.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html) With a simple configuration at the site level, turn your AEM experience into a PWA!

### Technical Details {#technical-details}

The latest technical documentation about the Page Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_page_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

Because the component represents the entire page, settings that would normally be in an edit dialog are found in the [Page Properties](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) window.

## Design Dialog {#design-dialog}

Because the component represents the entire page, the design dialog is accessed via **Page Information -&gt; Page Policy** when editing the page template.

![Page Policy](/help/assets/page-policy.png)

>[!NOTE]
>
>In previous versions of AEM, **Page Policy** was called **Page Design**.

### Properties Tab {#properties-tab}

Using the Page Design window, you can define the client libraries to be loaded as well as the web resources library for the page.

* **Client Libraries** - This defines the client library categories to load. JavaScript is added at the body end and the CSS is added to the page head.
* **Client Libraries JavaScript Page Head** - This defines the JavaScript Client library categories to load in the page head.
  * Categories defined here that are also present in the **Client Libraries** field will have JavaScript loaded in the page head instead of at body end.  
  * No CSS will be loaded unless the category is also present in the **Client Libraries** field.

* **Web Resources Client Library** - The client library category that is used to serve web resources such as favicons.

* **Skip to main content element selector** - Used as an accessibility feature to skip directly to the main content of the page

![Page Component design dialog](/help/assets/page-design.png)

Libraries can be configured for both the **Client Libraries** and **Client Libraries JavaScript Page Head** fields as follows:

* To add a new field click or tap the **Add** button below the fields.
* To remove a field click or tap the trash can icon next to the field to be removed.
* To rearrange the load order, click or tap and drag the handle next to the field to be moved.

For more information about using client-side libraries see [Using Client Side Libraries](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>The ability to separately define client libraries for the page head was introduced with core components release 2.2.0.

### Styles Tab {#styles-tab}

The Page Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Page Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
