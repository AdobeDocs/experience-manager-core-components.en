---
title: Core Components Introduction
seo-title: Core Components Introduction
description: Core Components were introduced to provide robust and extensible base components, built on the latest technology and best practices. 
seo-description: Core Components were introduced to provide robust and extensible base components, built on the latest technology and best practices. 
uuid: b815c7d1-fbb0-4480-bd23-42606ff8b1eb
contentOwner: User
content-type: reference
topic-tags: introduction
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: c44bb0d7-5d91-4659-878e-a0658fe29aa2
---

# Core Components Introduction{#core-components-introduction}

In Adobe Experience Manager, components are the structural elements that constitute the content of the pages being authored. Components have always been a fundamental element of the AEM experience, making page creation simple but powerful for the author and the development of components flexible and extensible for the developer.

Core Components were introduced to provide robust and extensible base components, built on the latest technology and best practices, and adhering to accessibility guidelines and are compliant with the WCAG 2.0 AA standard. Core components make page authoring more flexible and customizable, and extending them to offer custom functionality is simple for the developer.

## Try Out the Core Components

If you want to get started straight away trying out the Core Components, head over to the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html). The Component Library is an online showcase of the current version of most of the Core Components, allowing you to interact with variations of the components as well as see sample HTML and JSON output.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Core Components - Core Features {#core-components-core-features}

The Core Components are:

|||
|--- |--- |
|Pre-Configurable|Templates can define how the page authors can use them.|
|Versatile|Authors can create most kind of content with them.|
|Easy-to-Use|Authors can efficiently create and manage content with them.|
|Production-Ready|Usable out-of-the-box! They are robust, well-tested, and perform well.|
|Accessible|They comply WCAG 2.0 standard, provide ARIA labels, and support keyboard navigation.|
|Easy to Style|The components implement the Style System and the markup follows BEM CSS naming.|
|SEO Friendly|The HTML output is semantic and provides schema.org microdata annotations.|
|PWA/SPA/App Ready|Their streamlined JSON output can also be used for client-side rendering.|
|Extensible|To cover custom needs but without starting from scratch, everything can be extended.|
|Open Source|If something is not as it should be, contribute improvements on GitHub (Apache License).|
|Versioned|The core components won’t break your site when improving things that might impact you.|
|[Localized](localization.md)|Smart reference resoltuion allows certain components to find and render corresponding localized content automatically|

## Available Components {#available-components}

The current version of the Core Components features the following components.

* [Accordion](accordion.md)
* [Breadcrumb](breadcrumb.md)
* [Button](button.md)
* [Container](container.md)
* [Carousel](carousel.md)
* [Content Fragment](content-fragment-component.md)
* [Content Fragment List](content-fragment-list.md)
* [Download](download.md)
* [Embed](embed.md)
* [Experience Fragment](experience-fragment.md)
* [Form Button](form-button.md)
* [Form Container](form-container.md)
* [Form Hidden](form-hidden.md)
* [Form Options](form-options.md)
* [Form Text](form-text.md)
* [Image](image.md)
* [Language Navigation](language-navigation.md)
* [List](list.md)
* [Navigation](navigation.md)
* [Page](page.md)
* [Quick Search](quick-search.md)
* [Separator](separator.md)
* [Social Media Sharing](sharing.md)
* [Tabs](tabs.md)
* [Text](text.md)
* [Title](title.md)

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Some versions of individual Core Components may only be compatible with certain versions of AEM.
>
>See the individual help page (linked to in the previous list) for the specific component for compatibility information or reference the [Core Components Versions](versions.md) document for more information.

## When to Use Core Components {#when-to-use-core-components}

As the Core Components are all-new, and offer multiple benefits, it is recommended for new AEM projects to use them. For existing projects, a migration should be part of a larger project effort, for example a rebranding or overall refactoring.

For specific use recommendations, see [When to Use the Core Components?](developing.md) in the [Developing Core Components](developing.md) document.

## Gems Session Overview {#gems-session-overview}

For an introduction to the Core Components, the features they offer, and how they are leveraged in AEM, check out the AEM Gems Session [AEM Core Components.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) is a series of technical deep dives delivered by Adobe experts. This series complements the product documentation and of all the other technical channels, allowing developers to get in touch and go deep on a specific topic.

## Developing with the Core Components {#developing-core-components}

The Core Components provide robust and extensible base components that implement several patterns that allow easy customization, from simple styling to advanced functionality reuse. See the [Core Components developing documentation](developing.md) for more information.

Get started developing AEM Sites with Core Components by following [this step by step tutorial.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

Don't forget to start your own AEM project leveraging the [AEM Project Archetype](overview.md) with the latest Core Components built in!

## Core Components Support {#core-components-support}

Core Components are an integral part of AEM and supported as is, under the same terms and conditions as if they were delivered as part of the Quickstart.

Like other product features, the general rule of end-of-life is:

* Components are first announced to be deprecated before being removed
* At the earliest they are then removed from the AEM release following the announcement.

This gives customers at least one release cycle to move to the new version of the component, before support ends.

The version of each component clearly states the AEM versions that it supports. When support ceases for a version of AEM, then so does the support of the Core Components for that version of AEM.

For details about the support of component customizations, see the [Customizing Core Components](customizing.md) page of the relevant Core Components Version.

## Foundation Component Support {#foundation-component-support}

Since the Foundation Components have served as a basis of so much project development over many versions, they will continue to be supported into the foreseeable future.

However, Adobe's development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.
