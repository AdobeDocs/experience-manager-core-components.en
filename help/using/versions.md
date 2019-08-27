---
title: Core Components Versions
seo-title: Core Components Versions
description: Core Components are published as releases which may contain more than one version of the same core components. This document explains what releases and versions are and how to understand compatibility with Core Components and AEM.
seo-description: Core Components are published as releases which may contain more than one version of the same core components. This document explains what releases and versions are and how to understand compatibility with Core Components and AEM.
uuid: a916a923-8c5e-456a-84b5-b52228e21434
contentOwner: User
content-type: reference
topic-tags: introduction
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: a3a98b2f-65bf-4493-82ad-01717938fdbc
---

# Core Components Versions{#core-components-versions}

The current release of the Core Components is 2.4.0 and is compatible with AEM 6.5. It was released in May 2019 as an minor update to release 2.0.0. Release 2.0.0 introduced new components along with v2 updates of existing components.

See the section [Release History and Compatibility](#versions-and-releases) of this document for more information.

You can also check out the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html), which showcases the current release of the Core Components and gives examples of their usage.

## Versions and Releases {#versions-and-releases}

Core Components are distributed via GitHub. This allows Adobe to more quickly add functionality to the components and also allow for community input outside of the AEM release cycle.

The Core Components are made available with defined AEM versions with which they are compatible. This means that one AEM version may support multiple versions or releases of the Core Components. This gives more flexibility than the former Foundation Components, which were tied to a specific version of AEM.

### Versions {#versions}

The major iteration of the Core Components are the **versions**. Each component has a version. Versions are denoted with **v** appended with a nonzero, positive integer such as v1 and v2. Versions are incremented only for changes that are not backward-compatible, which is normally the case for the introduction of new features and functionality.

Developers and administrators can recognize versions of the core components by a number in their resource type paths, and in the fully qualified Java class names of their implementations. This version number represents a major version as defined by [semantic versioning guidelines](https://semver.org/).

For more details about core component versions, see the [developer documentation of the Core Components](guidelines.md).

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

## Release History and Compatibility {#release-history-and-compatibility}

The Core Components were first released with AEM 6.3 and are designed to be flexible and compatible with all supported AEM versions. Because of this a release of the components can contain multiple versions of the same component.

The following tables illustrate the compatibility of the releases of the Core Components along with which component versions are contained in which releases.

### Release History & Supported AEM Versions {#release-history-supported-aem-versions}

The following table, the contents of which are [available on GitHub with full release details](https://github.com/adobe/aem-core-wcm-components/releases), gives an overview of the releases of the Core Components and their compatibility with AEM releases and Java versions.

|Release|Description|AEM 6.3|AEM 6.4|AEM 6.5|Java|Release Date|
|---|---|---|---|---|---|---|
|[2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0)|This release introduced the new Embed and Experience Fragment components|6.3.3.0+|6.4.2.0+|6.5.0.0+|8, 11|September 2019|
|[2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0)|This release introduced the new Accordion, Button, Container and Download components.|6.3.3.0+|6.4.2.0+|6.5.0.0+|8, 11|25 June 2019|
|[2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0)|This release introduced the Content Fragment List Component|6.3.3.0+|6.4.2.0+|6.5.0.0+|8, 11|7 May 2019|
|[2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2)|This release focused on refinements to the component library, but also contains some feature enhancements for the Separator Component|6.3.3.0+|6.4.2.0+|6.5.0.0+|8|14 March 2019|
|[2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0)|This release focused on the component library as well as introducing the new separator component, but also contains some feature enhancements for the Image Component|6.3.3.0+|6.4.2.0+|-|8|11 February 2019|
|[2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2)|This release mainly focused on bug fixes, but also contains some feature enhancements for the Carousel component|6.3.3.0+|6.4.2.0+|-|8|27 November 2018|
|[2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0)|Tabs and Carousel components introduced, improvements to the image, page, and title components and enhanced tracking|6.3.3.0+|6.4.2.0+|-|8|16 October 2018|
|[2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0)|Teaser Component introduced, Image Component improvements, and numerous bug fixes|6.3.3.0+|6.4.2.0+|-|8|13 July 2018|
|[2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8)|Bugfix release|6.3.2.0+|6.4.0.0+|-|8|12 June 2018|
|[2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6)|Additional under-the-hood improvements, bug fixes, and small improvements including support of image flip.|6.3.2.0+|6.4.0.0+|-|8|11 April 2018|
|[2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4)|Mostly under-the-hood improvements, bug fixes, plus some minor improvements to the Image, Page, and Content Fragment Components|6.3.2.0+|6.4.0.0+|-|8|7 March 2018|
|[2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0)|Navigation, Language Navigation, and Quick Search components introduced. Style system implemented for all components.|6.3.2.0+|6.4.0.0+|-|8|16 January 2018|
|[1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0)|Implementation of JSON export on all components, introduction of the Content Fragment component|6.3.1.0|6.4.0.0+|-|8|10 October 2017|
|[1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6)|Several fixes for the Image component|6.3.0.0+|6.4.0.0+|-|8|4 August 2017|
|[1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4)|Fixes of Page Component, Image Component, various global fixes and improvements|6.3.0.0+|6.4.0.0+|-|8|26 April 2017|
|[1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2)|Fixes for animated GIF images in Image component|6.3.0.0+|6.4.0.0+|-|7|22 March 2017|
|[1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0)|Initial release of Core Components|6.3.0.0+|6.4.0.0+|-|7|20 March 2017|

>[!NOTE]
>
>As with AEM, Adobe recommends that developers use the [latest release and versions of the Core Components](https://github.com/adobe/aem-core-wcm-components/releases/latest) available that is compatible with the version of AEM that they are running in order to benefit from the most up-to-date fixes and features.

### Component Versions & Releases {#component-versions-and-releases}

The following table details which versions of which components are contained in which releases of the Core Components.

||Release 1.0.0 - 1.0.6|Release 1.1.0|Release 2.0.0 - 2.0.8|Release 2.1.0|Release 2.2.-2.2.0|2.3.0|
|---|---|---|---|---|---|---|
|**[Page](page.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Title](title.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Image](image.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[List](list.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Breadcrumb](breadcrumb.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Social Media Sharing](sharing.md)**|v1|v1|v1|v1|v1|v1|
|**[Form Container](form-container.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Text](form-text.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Options](form-options.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Hidden](form-hidden.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Button](form-button.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
| **[Content Fragment](content-fragment-component.md)**||Sandbox|v1|v1|v1|v1|
|**[Navigation](navigation.md)**|||v1|v1|v1|v1|
|**[Language Navigation](language-navigation.md)**|||v1|v1|v1|v1|
|**[Quick Search](quick-search.md)**|||v1|v1|v1|v1|
|**[Teaser](teaser.md)**||||v1|v1|v1|
|**[Tabs](tabs.md)**|||||v1|v1|
|**[Carousel](carousel.md)**|||||v1|v1|
|**[Separator](separator.md)**||||||v1|

## Documentation {#documentation}

[Authoring with Core Components](authoring.md) describes the usage of the core components and the features that are exposed to content authors and template authors. Each component is documented in detail.

[Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html) is a showcase of the current version of most Core Components, illustrating how they can be used.

[Developing Core Components](developing.md) describes the technical capabilities of the Core Components, how to use them in your projects, how to customize, and best practices.

[Core Components Introduction](introduction.md) gives an overview of Core Components compatibility across versions, use cases, and support.
