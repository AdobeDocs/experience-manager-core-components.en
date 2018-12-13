---
title: Authoring with Core Components
seo-title: Authoring with Core Components
description: null
seo-description: In Adobe Experience Manager, components are the structural elements that constitute the content of the pages being authored. The Core Components offer flexible and feature-rich authoring functionality.
uuid: 4a54cd4c-3d89-4683-8301-bf1e634736e3
contentOwner: User
content-type: reference
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 8751e490-d427-44f2-b767-51935afda988
index: y
internal: n
snippet: y
---

# Authoring with Core Components{#authoring-with-core-components}

In Adobe Experience Manager, components are the structural elements that constitute the content of the pages being authored. This section covers the Core Components, which provide essential content types to create pages.

The Core Components offer flexible and feature-rich authoring functionality. The [We.Retail reference site](/content/help/en/experience-manager/6-4/sites/developing/using/we-retail) illustrates how the core components can be used.

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](../using/using.md). Once integrated, they may be made available and pre-configured via the [template editor](/content/help/en/experience-manager/6-4/sites/authoring/using/templates) or in [design mode](/content/help/en/experience-manager/6-4/sites/authoring/using/default-components-designmode).

>[!CAUTION]
>
>Core Components [require AEM 6.3 or higher](../using/versions.md#main-pars_title_236368006) and do not work with the Classic UI.

## Authoring with Core Components {#authoring-with-core-components}

Authoring with the Core Components does not differ substantially from the [Foundation Components](/content/help/en/experience-manager/6-4/sites/authoring/using/default-components-foundation).

However, as an author, you will notice several advantages of the Core Components, including:

* Simple to use and well-integrated with the [page editor](/content/help/en/experience-manager/6-4/sites/authoring/using/editing-content)
* Feature-rich capabilities to accommodate many use cases as [illustrated in We.Retail](/content/help/en/experience-manager/6-4/sites/developing/using/we-retail)
* [Pre-configurable](#main-pars_title_1323733785) to define which features are available to page authors

    * Via the [template editor](/content/help/en/experience-manager/6-4/sites/authoring/using/templates#main-pars_title_1909278313) for [editable templates](/content/help/en/experience-manager/6-4/sites/developing/using/page-templates-editable)
    
    * Via [design mode](/content/help/en/experience-manager/6-4/sites/authoring/using/default-components-designmode) for [static templates](/content/help/en/experience-manager/6-4/sites/developing/using/page-templates-static)

* Built around [accessibility guidelines](/content/help/en/experience-manager/6-4/managing/using/web-accessibility)  

* Built to support [responsive layout](/content/help/en/experience-manager/6-4/sites/authoring/using/responsive-layout)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](/content/help/en/experience-manager/6-4/sites/authoring/using/editing-content).

Components are grouped according to categories called component groups to easily organize and filter the components. The component group name is displayed with the component in the [component browser](/content/help/en/experience-manager/6-4/sites/authoring/using/editing-content#main-pars_title_17) and it is also possible to filter by group to easily find the right component.

>[!NOTE]
>
>The Core Components are by default part of a hidden group and are not visible within the component browser.
>
>Add the required components to a visible group or customize them for them to be available for authors.

## Pre-Configuring Core Components {#pre-configuring-core-components}

Configuring Foundation Components was the job of a developer. However with Core Components, a template author can now configure a number of capabilities via the template editor or in design mode.

For example if an image component should not allow image upload from the file system, or if a text component should only allow certain paragraph formatting, these features can be enabled or disabled with a simple click.

See [Creating Page Templates](/content/help/en/experience-manager/6-4/sites/authoring/using/templates#main-pars_title_1909278313) for more information.

### Edit and Design Dialogs {#edit-and-design-dialogs}

Because the Core Components can be pre-configured by template authors to define what options are allowed as part of a template, and then further configured by the page author to define actual page content, each component can have options in two different dialogs.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <td> </td> 
   <td><strong>Description</strong></td> 
   <td><strong>What it Controls</strong></td> 
   <td><strong>Examples</strong></td> 
  </tr>
  <tr>
   <td><a href="/content/help/en/experience-manager/6-4/sites/authoring/using/editing-content#main-pars_title"><strong>Edit Dialog</strong></a></td> 
   <td>Options that a <strong>page author</strong> can modify during normal page editing for the placed components</td> 
   <td>The content displayed by the component and how it will ultimately appear on the page.</td> 
   <td>Formatting of content text, rotate an image on a page<br /> </td> 
  </tr>
  <tr>
   <td><a href="/content/help/en/experience-manager/6-4/sites/authoring/using/templates#main-pars_title_1909278313"><strong>Design Dialog</strong></a></td> 
   <td>Options that a <strong>template author</strong> can modify when configuring a page template.</td> 
   <td>What options the page author has available when editing the component</td> 
   <td>Which text formatting options are available, which image in-place options are available</td> 
  </tr>
 </tbody>
</table>

### Component Styling {#component-styling}

The styles of most Core Components can be defined using the AEM style system.

* A template author can define which styles are available for a particular component in the Design Dialog of that component.
* The content author can then choose which styles to apply when adding the component and creating content.

For further details see the [Style System](/content/help/en/experience-manager/6-4/sites/authoring/using/style-system) documentation.

>[!NOTE]
>
>In AEM 6.3, [feature pack 20593](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/featurepack/cq-6.3.0-featurepack-20593) is required to enable the style system feature and can be downloaded from Package Share.

## List of Core Components Available {#list-of-core-components-available}

The following is a list of the available Core Components linked to pages describing their edit and design dialog capabilities in detail.

The current version of the Core Components features the following components.

* [Breadcrumb](../using/breadcrumb.md)
* [Form Button](../using/form-button.md)
* [Form Container](../using/form-container.md)
* [Content Fragment](../using/content-fragment-component.md)
* [Form Hidden  
  ](../using/form-hidden.md)
* [Form Options](../using/form-options.md)
* [Form Text  
  ](../using/form-text.md)
* [Image](../using/image.md)
* [Language Navigation](../using/language-navigation.md)
* [List](../using/list.md)
* [Navigation](../using/navigation.md)
* [Page](../using/page.md)
* [Quick Search](../using/quick-search.md)
* [Social Media Sharing](../using/sharing.md)
* [Teaser](../using/teaser.md)
* [Text](../using/text.md)
* [Title](../using/title.md)

>[!CAUTION]
>
>Some versions of individual Core Components may only be compatible with certain versions of AEM.
>
>See the individual help page (linked to in the previous list) for the specific component for compatibility information or reference the [Core Components Versions](../using/versions.md) document for more information.

>[!NOTE]
>
>Depending on your instance you may have customized components developed explicitly for your requirements. These may even have the same name as some of the components discussed here.

>[!NOTE]
>
>The form core components are not related to AEM Forms.

## Developer Resources {#developer-resources}

See the [Developing Core Components](../using/developing.md) developer documentation for technical information regarding core components.
