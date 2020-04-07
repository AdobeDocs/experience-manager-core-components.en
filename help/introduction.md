---
title: Core Components Introduction
description: Core Components were introduced to provide robust and extensible base components, built on the latest technology and best practices. 
---

# Core Components Introduction{#core-components-introduction}

In Adobe Experience Manager, components are the structural elements that constitute the content of the pages being authored. Components have always been a fundamental element of the AEM experience, making page creation simple but powerful for the author and the development of components flexible and extensible for the developer.

The Core Components are a set of standardized Web Content Management (WCM) components for AEM to speed up development time and reduce maintenance cost of your websites.

## Resources {#resources}

* **[Component Library:](https://www.adobe.com/go/aem_cmp_library)** A collection of examples to view the components in their various configurations.
* **Component Documentation (this document):** For developers and authors, with details about each component.
* Get Started:
  * **[WKND Tutorial:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** A two-day tutorial for building a new site.
  * **[Summit Tutorial:](https://expleague.azureedge.net/labs/L767/index.html)** A two-hour tutorial for building a new site (from a Lab at US Summit 2019).
  * **[Gems Webinar:](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** A guided tour of the Core Components (recorded on Dec 2018).

## Features {#features}

|||
|--|---|
|Production-Ready| The Core Components are 27 robust components that are well tested, widely used, and that perform well.|
|Cloud-Ready| Whether on [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), on [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), or on-premise, they just work.|
|Versatile| The components represent generic concepts with which the authors can assemble nearly any layout.|
|Configurable| Template-level [content policies](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) define which features the page authors are allowed to use or not use.|
|Accessible| They comply [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, and support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)).|
|SEO-Friendly| The HTML output is semantic and provides [schema.org](https://schema.org) microdata annotations.|
|WebApp-Ready| The [streamlined JSON output](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) allows client-side rendering, still with a possibility of [in-context editing](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).|
|Design Kit| A [UI kit for Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) allows designers to create wireframes that they can then [style as needed](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd).|
|Themeable| The components implement the [Style System](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/).|
|Customizable| Several patterns allow [easy customization](developing/customizing.md), from adjusting the HTML to advanced functionality reuse.|
|Versioning| The [versioning policy](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) ensures that the Core Components won't break your site when improving things that might impact you.|
|Localizable|Smart reference resolution allows certain components to find and [render corresponding localized content automatically](get-started/localization.md).|
|Open Sourced| If something is not as it should, [contribute your improvements!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md)|

## Available Components {#available-components}

The current version of the Core Components features the following components.

* [Accordion](components/accordion.md)
* [Breadcrumb](components/breadcrumb.md)
* [Button](components/button.md)
* [Container](components/container.md)
* [Carousel](components/carousel.md)
* [Content Fragment](components/content-fragment-component.md)
* [Content Fragment List](components/content-fragment-list.md)
* [Download](components/download.md)
* [Embed](components/embed.md)
* [Experience Fragment](components/experience-fragment.md)
* [Form Button](components/forms/form-button.md)
* [Form Container](components/forms/form-container.md)
* [Form Hidden](components/forms/form-hidden.md)
* [Form Options](components/forms/form-options.md)
* [Form Text](components/forms/form-text.md)
* [Image](components/image.md)
* [Language Navigation](components/language-navigation.md)
* [List](components/list.md)
* [Navigation](components/navigation.md)
* [Page](components/page.md)
* [Quick Search](components/quick-search.md)
* [Separator](components/separator.md)
* [Social Media Sharing](components/sharing.md)
* [Tabs](components/tabs.md)
* [Text](components/text.md)
* [Title](components/title.md)

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Some versions of individual Core Components may only be compatible with certain versions of AEM.
>
>See the individual help page (linked to in the previous list) for the specific component for compatibility information or reference the [Core Components Versions](versions.md) document for more information.

## When to Use Core Components {#when-to-use-core-components}

As the Core Components are all-new, and offer multiple benefits, it is recommended for new AEM projects to use them. For existing projects, a migration should be part of a larger project effort, for example a rebranding or overall refactoring.

For specific use recommendations, see [When to Use the Core Components?](developing/overview.md#when-to-use-the-core-components) in the [Developing Core Components](developing/overview.md) document.

## Gems Session Overview {#gems-session-overview}

For an introduction to the Core Components, the features they offer, and how they are leveraged in AEM, check out the AEM Gems Session [AEM Core Components.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) is a series of technical deep dives delivered by Adobe experts. This series complements the product documentation and of all the other technical channels, allowing developers to get in touch and go deep on a specific topic.

## Developing with the Core Components {#developing-core-components}

The Core Components provide robust and extensible base components that implement several patterns that allow easy customization, from simple styling to advanced functionality reuse. See the [Core Components developing documentation](developing/overview.md) for more information.

Get started developing AEM Sites with Core Components by following [the WKND tutorial.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

Don't forget to start your own AEM project leveraging the [AEM Project Archetype](developing/archetype/overview.md) with the latest Core Components built in!

## Core Components Support {#core-components-support}

Core Components are an integral part of AEM and supported as is, under the same terms and conditions as if they were delivered as part of the Quickstart.

Like other product features, the general rule of end-of-life is:

* Components are first announced to be deprecated before being removed
* At the earliest they are then removed from the AEM release following the announcement.

This gives customers at least one release cycle to move to the new version of the component, before support ends.

The version of each component clearly states the AEM versions that it supports. When support ceases for a version of AEM, then so does the support of the Core Components for that version of AEM.

For details about the support of component customizations, see the [Customizing Core Components](developing/customizing.md) page of the relevant Core Components Version.

## Foundation Component Support {#foundation-component-support}

Since the Foundation Components have served as a basis of so much project development over many versions, they will continue to be supported into the foreseeable future.

However, Adobe's development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.
