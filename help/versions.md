---
title: Core Components Versions
description: Core Components are published as releases which may contain more than one version of the same core components. This document explains what releases and versions are and how to understand compatibility with Core Components and AEM.
---

# Core Components Versions {#core-components-versions}

The current release of the Core Components is 2.8.0 and is compatible with [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) and [on-premise AEM](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html) installations. It was released in December 2019 as an important update to release 2.0.0. Release 2.0.0 introduced new components along with v2 updates of existing components.

## Release History and Compatibility {#release-history-and-compatibility}

The Core Components were first released with AEM 6.3 and are designed to be flexible and compatible with all supported AEM versions. Because of this a release of the components can contain multiple versions of the same component.

The following tables illustrate the compatibility of the releases of the Core Components along with which component versions are contained in which releases.

### Release History & Requirements {#release-history-requirements}

The following table, the contents of which are [available on GitHub with full release details](https://github.com/adobe/aem-core-wcm-components/releases), gives an overview of the releases of the Core Components and their compatibility with AEM releases and Java versions.

|Release|Description|AEM 6.3|AEM 6.4|AEM 6.5|AEM as a Cloud Service|Java|Release Date|
|---|---|---|---|---|---|---|---|
|[2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0)|This release enabled integration with the Adobe Client Data Layer and introduced the Progress Bar component.|-|6.4.4.0+|6.5.0.0+|Continual|8, 11|29 May 2020|
|[2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0)|This release focused on fixes with small enhancements.|6.3.3.4+|6.4.4.0+|6.5.0.0+|Continual|8, 11|5 December 2019|
|[2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0)|This release introduced the new Embed component|6.3.3.4+|6.4.4.0+|6.5.0.0+|Continual|8, 11|25 September 2019|
|[2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0)|This release introduced the new Experience Fragment component|6.3.3.4+|6.4.4.0+|6.5.0.0+|Continual|8, 11|6 September 2019|
|[2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0)|This release introduced the new Accordion, Button, Container, and Download components.|6.3.3.0+|6.4.2.0+|6.5.0.0+|Continual|8, 11|25 June 2019|
|[2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0)|This release introduced the Content Fragment List Component|6.3.3.0+|6.4.2.0+|6.5.0.0+|Continual|8, 11|7 May 2019|
|[2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2)|This release focused on refinements to the component library, but also contains some feature enhancements for the Separator Component|6.3.3.0+|6.4.2.0+|6.5.0.0+|Continual|8|14 March 2019|
|[2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0)|This release focused on the component library as well as introducing the new separator component, but also contains some feature enhancements for the Image Component|6.3.3.0+|6.4.2.0+|-|-|8|11 February 2019|
|[2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2)|This release mainly focused on bug fixes, but also contains some feature enhancements for the Carousel component|6.3.3.0+|6.4.2.0+|-|-|8|27 November 2018|
|[2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0)|Tabs and Carousel components introduced, improvements to the image, page, and title components and enhanced tracking|6.3.3.0+|6.4.2.0+|-|-|8|16 October 2018|
|[2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0)|Teaser Component introduced, Image Component improvements, and numerous bug fixes|6.3.3.0+|6.4.2.0+|-|-|8|13 July 2018|
|[2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8)|Bugfix release|6.3.2.0+|6.4.0.0+|-|-|8|12 June 2018|
|[2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6)|Additional under-the-hood improvements, bug fixes, and small improvements including support of image flip.|6.3.2.0+|6.4.0.0+|-|-|8|11 April 2018|
|[2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4)|Mostly under-the-hood improvements, bug fixes, plus some minor improvements to the Image, Page, and Content Fragment Components|6.3.2.0+|6.4.0.0+|-|-|8|7 March 2018|
|[2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0)|Navigation, Language Navigation, and Quick Search components introduced. Style system implemented for all components.|6.3.2.0+|6.4.0.0+|-|-|8|16 January 2018|
|[1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0)|Implementation of JSON export on all components, introduction of the Content Fragment component|6.3.1.0|6.4.0.0+|-|-|8|10 October 2017|
|[1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6)|Several fixes for the Image component|6.3.0.0+|6.4.0.0+|-|-|8|4 August 2017|
|[1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4)|Fixes of Page Component, Image Component, various global fixes and improvements|6.3.0.0+|6.4.0.0+|-|-|8|26 April 2017|
|[1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2)|Fixes for animated GIF images in Image component|6.3.0.0+|6.4.0.0+|-|-|7|22 March 2017|
|[1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0)|Initial release of Core Components|6.3.0.0+|6.4.0.0+|-|-|7|20 March 2017|

>[!NOTE]
>
>As with AEM, Adobe recommends that developers use the [latest release and versions of the Core Components](https://github.com/adobe/aem-core-wcm-components/releases/latest) available that is compatible with the version of AEM that they are running in order to benefit from the most up-to-date fixes and features.

### Component Versions & Releases {#component-versions-and-releases}

The following table details which versions of which components are contained in which releases of the Core Components.

||Release 1.0.0 - 1.0.6|Release 1.1.0|Release 2.0.0 - 2.0.8|Release 2.1.0|Release 2.2.0-2.2.0|Release 2.3.0-2.3.2|Release 2.4.0|Release 2.5.0|Release 2.6.0|Release 2.7.0-2.8.0|Release 2.9.0+|
|---|---|---|---|---|---|---|---|---|---|---|---|
|**[Page](components/page.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Title](components/title.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Image](components/image.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[List](components/list.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Breadcrumb](components/breadcrumb.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Social Media Sharing](components/sharing.md)**|v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|
|**[Form Container](components/forms/form-container.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Text](components/forms/form-text.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Options](components/forms/form-options.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Hidden](components/forms/form-hidden.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Button](components/forms/form-button.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
| **[Content Fragment](components/content-fragment-component.md)**||Sandbox|v1|v1|v1|v1|v1|v1|v1|v1, v2|v1, v2|
|**[Navigation](components/navigation.md)**|||v1|v1|v1|v1|v1|v1|v1|v1|v1|
|**[Language Navigation](components/language-navigation.md)**|||v1|v1|v1|v1|v1|v1|v1|v1|v1|
|**[Quick Search](components/quick-search.md)**|||v1|v1|v1|v1|v1|v1|v1|v1|v1|
|**[Teaser](components/teaser.md)**||||v1|v1|v1|v1|v1|v1|v1|v1|
|**[Tabs](components/tabs.md)**|||||v1|v1|v1|v1|v1|v1|v1|
|**[Carousel](components/carousel.md)**|||||v1|v1|v1|v1|v1|v1|v1|
|**[Separator](components/separator.md)**||||||v1|v1|v1|v1|v1|v1|
|**[Content Fragment List](components/content-fragment-list.md)**|||||||v1|v1|v1|v1|v1|
|**[Accordion](components/accordion.md)**||||||||v1|v1|v1|v1|
|**[Button](components/button.md)**||||||||v1|v1|v1|v1|
|**[Container](components/container.md)**||||||||v1|v1|v1|v1|
|**[Download](components/download.md)**||||||||v1|v1|v1|v1|
|**[Experience Fragment](components/experience-fragment.md)**|||||||||v1|v1|v1|
|**[Embed](components/embed.md)**||||||||||v1|v1|
|**[Progress Bar](components/progress-bar.md)**|||||||||||v1|

## Versions and Releases {#versions-and-releases}

Core Components are distributed via GitHub. This allows Adobe to more quickly add functionality to the components and also allow for community input outside of the AEM release cycle.

The Core Components are made available with defined AEM versions with which they are compatible. This means that one AEM version may support multiple versions or releases of the Core Components. This gives more flexibility than the former Foundation Components, which were tied to a specific version of AEM.

### Versions {#versions}

The major iteration of the Core Components are the **versions**. Each component has a version. Versions are denoted with **v** appended with a nonzero, positive integer such as v1 and v2. Versions are incremented only for changes that are not backward-compatible, which is normally the case for the introduction of new features and functionality.

Developers and administrators can recognize versions of the core components by a number in their resource type paths, and in the fully qualified Java class names of their implementations. This version number represents a major version as defined by [semantic versioning guidelines](https://semver.org/).

For more details about core component versions, see the [developer documentation of the Core Components](developing/guidelines.md).

### Releases {#releases}

The core components are made available through **releases** and [represent the actual published artifacts available on GitHub](https://github.com/adobe/aem-core-wcm-components/releases). Releases are denoted with a decimal number of the format X.Y.Z and collect all core components together as a deliverable package.

* **Major releases** can introduce new versions of existing components along with entirely new components as well as standard bug fixes. This is represented by an increment in the X component of the release number.  
* **Important releases** can introduce new functionality to existing versions of components along with bug fixes. This is represented by an increment in the Y component of the release number.  
* **Minor releases** contain only bug fixes. This is represented by an increment in the Z component of the release number.

>[!NOTE]
>
>Releases can contain multiple versions of the same component.
>
>The same version of a component can appear in multiple releases.

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
