---
title: Authoring with Core Components
seo-title: Authoring with Core Components
description: In AEM, components are the structural elements that constitute the content of the pages being authored - Core Components offer flexible and feature-rich authoring functionality.
seo-description: In AEM, components are the structural elements that constitute the content of the pages being authored - Core Components offer flexible and feature-rich authoring functionality.
uuid: 4a54cd4c-3d89-4683-8301-bf1e634736e3
content-type: reference
topic-tags: authoring
discoiquuid: 8751e490-d427-44f2-b767-51935afda988
---

# Authoring with Core Components{#authoring-with-core-components}

In Adobe Experience Manager, components are the structural elements that constitute the content of the pages being authored. This section covers the Core Components, which provide essential content types to create pages.

The Core Components offer flexible and feature-rich authoring functionality. The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) illustrates how the core components can be used.

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Core Components [require AEM 6.3 or higher](versions.md#main-pars_title_236368006) and do not work with the Classic UI.

## Authoring with Core Components {#authoring-with-core-components}

Authoring with the Core Components does not differ substantially from the [Foundation Components](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/default-components-foundation.html).

However, as an author, you will notice several advantages of the Core Components, including:

* Simple to use and well-integrated with the [page editor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-content.html)
* Feature-rich capabilities to accommodate many use cases as [illustrated in We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)
* [Pre-configurable](#main-pars_title_1323733785) to define which features are available to page authors
  * Via the [template editor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1909278313) for [editable templates](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/page-templates-editable.html)
  * Via [design mode](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/default-components-designmode.html) for [static templates](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/page-templates-static.html)

* Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-4/managing/using/web-accessibility.html)  

* Built to support [responsive layout](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/responsive-layout.html)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-content.html).

Components are grouped according to categories called component groups to easily organize and filter the components. The component group name is displayed with the component in the [component browser](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-content.html#main-pars_title_17) and it is also possible to filter by group to easily find the right component.

>[!NOTE]
>
>The Core Components are by default part of a hidden group and are not visible within the component browser.
>
>Add the required components to a visible group or customize them for them to be available for authors.

## Pre-Configuring Core Components {#pre-configuring-core-components}

Configuring Foundation Components was the job of a developer. However with Core Components, a template author can now configure a number of capabilities via the template editor or in design mode.

For example if an image component should not allow image upload from the file system, or if a text component should only allow certain paragraph formatting, these features can be enabled or disabled with a simple click.

See [Creating Page Templates](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1909278313) for more information.

### Edit and Design Dialogs {#edit-and-design-dialogs}

Because the Core Components can be pre-configured by template authors to define what options are allowed as part of a template, and then further configured by the page author to define actual page content, each component can have options in two different dialogs.

||Description|What it Controls|Examples|
|--- |--- |--- |--- |
|**Edit Dialog**|Options that a **page author** can modify during normal page editing for the placed components|The content displayed by the component and how it will ultimately appear on the page.|Formatting of content text, rotate an image on a page|
|**Design Dialog**|Options that a **template author** can modify when configuring a page template.|What options the page author has available when editing the component|Which text formatting options are available, which image in-place options are available|

### Component Styling {#component-styling}

The styles of most Core Components can be defined using the AEM style system.

* A template author can define which styles are available for a particular component in the Design Dialog of that component.
* The content author can then choose which styles to apply when adding the component and creating content.

For further details see the [Style System](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/style-system.html) documentation.

>[!NOTE]
>
>In AEM 6.3, [feature pack 20593](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/featurepack/cq-6.3.0-featurepack-20593) is required to enable the style system feature and can be downloaded from Package Share.

## List of Core Components Available {#list-of-core-components-available}

The following is a list of the available Core Components linked to pages describing their edit and design dialog capabilities in detail.

The current version of the Core Components features the following components.

* [Breadcrumb](breadcrumb.md)
* [Form Button](form-button.md)
* [Form Container](form-container.md)
* [Content Fragment](content-fragment-component.md)
* [Form Hidden](form-hidden.md)
* [Form Options](form-options.md)
* [Form Text](form-text.md)
* [Image](image.md)
* [Language Navigation](language-navigation.md)
* [List](list.md)
* [Navigation](navigation.md)
* [Page](page.md)
* [Quick Search](quick-search.md)
* [Social Media Sharing](sharing.md)
* [Teaser](teaser.md)
* [Text](text.md)
* [Title](title.md)

>[!CAUTION]
>
>Some versions of individual Core Components may only be compatible with certain versions of AEM.
>
>See the individual help page (linked to in the previous list) for the specific component for compatibility information or reference the [Core Components Versions](versions.md) document for more information.

>[!NOTE]
>
>Depending on your instance you may have customized components developed explicitly for your requirements. These may even have the same name as some of the components discussed here.
>The form core components are not related to AEM Forms.

## Developer Resources {#developer-resources}

See the [Developing Core Components](developing.md) developer documentation for technical information regarding core components.
