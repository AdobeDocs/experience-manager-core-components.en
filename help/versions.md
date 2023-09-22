---
title: Core Components Versions
description: Core Components are published as releases which may contain more than one version of the same core components. This document explains what releases and versions are and how to understand compatibility with Core Components and AEM.
role: Architect, Developer, Admin, User
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
---
# Core Components Versions {#core-components-versions}

The current release of the Core Components is 2.23.4 and is compatible with [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html) and [on-premise AEM](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html) installations.

## Release History and Compatibility {#release-history-and-compatibility}

The Core Components are designed to be flexible and compatible with all supported AEM versions. Because of this a release of the components can contain multiple versions of the same component.

The following tables illustrate the compatibility of the releases of the Core Components along with which component versions are contained in which releases.

### Release History & Requirements {#release-history-requirements}

The following table, the contents of which are [available on GitHub with full release details](https://github.com/adobe/aem-core-wcm-components/releases), gives an overview of the releases of the Core Components and their compatibility with AEM releases and Java versions.

|Release|Description|AEM 6.4|AEM 6.5|AEM as a Cloud Service|Java|Release Date|
|---|---|---|---|---|---|---|
|[2.23.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.4)|This patch release included various bug fixes.|-|6.5.17.0+|Continual|8, 11|15 September 2023|
|[2.23.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.2)|This patch added Dynamic Media smart crop for remote assets to [Image](/help/components/image.md) and [Teaser Components](/help/components/teaser.md) and fixed a number of bugs.|-|6.5.17.0+|Continual|8, 11|4 August 2023|
|[2.23.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.0)|This release added addition support for Dynamic Media assets features.|-|6.5.17.0+|Continual|8, 11|6 June 2023|
|[2.22.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.12)|This patch release fixes two issues.|-|6.5.14.0+|Continual|8, 11|25 May 2023|
|[2.22.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.10)|This patch release fixes two regressions.|-|6.5.14.0+|Continual|8, 11|11 May 2023|
|[2.22.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.8)|This patch release brings back features which were accidentally removed in previous release.|-|6.5.14.0+|Continual|8, 11|9 May 2023|
|[2.22.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.6)|This patch release fixes a regression in the [Container Component.](/help/components/container.md)|-|6.5.14.0+|Continual|8, 11|21 April 2023|
|[2.22.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.4)|This is a patch release to fix an issues in the [Content Fragment List Component.](/help/components/content-fragment-list.md)|-|6.5.14.0+|Continual|8, 11|5 April 2023|
|[2.22.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.2)|This is a maintenance release to address two issues introduced in 2.22.0|-|6.5.14.0+|Continual|8, 11|31 March 2023|
|[2.22.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.0)|This release introduces a new version of the [List Component](/help/components/list.md) along with improvements to the [Teaser](/help/components/teaser.md) and update of the [PDF Viewer](/help/components/pdf-viewer.md) and [Carousel](/help/components/carousel.md)|-|6.5.14.0+|Continual|8, 11|9 February 2023|
|[2.21.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.2)|This is a patch release fixing an issue with the v1 and v2 [Teaser Components.](/help/components/teaser.md)|-|6.5.13.0+|Continual|8, 11|12 September 2022|
|[2.21.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.0)|This release includes a number of enhancements including publication of the LinkHandler API, improvements to the [Image Component](/help/components/image.md) and [Data Layer,](/help/developing/data-layer/overview.md) as well as improvements to multi-panel components.|-|6.5.13.0+|Continual|8, 11|12 September 2022|
|[2.20.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.8)|This release fixes an issue with delivery of SVG images via AdaptiveImageServlet.|-|6.5.13.0+|Continual|8, 11|4 August 2022|
|[2.20.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.6)|This patch release fixes an issue with the new [Table of Contents Component.](/help/components/tableofcontents.md)|-|6.5.13.0+|Continual|8, 11|7 July 2022|
|[2.20.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.4)|This patch release fixes an issue with the new [Table of Contents Component.](/help/components/tableofcontents.md)|-|6.5.13.0+|Continual|8, 11|29 June 2022|
|[2.20.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.2)|This is a patch release that fixes an issue in the new AEMaaCS [web-optimized asset delivery service.](/help/developing/web-optimized-image-delivery.md)|-|6.5.13.0+|Continual|8, 11|20 June 2022|
|[2.20.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.0)|This release adds a new [Table of Contents Component](/help/components/tableofcontents.md), adds support for AEMaaCS [web-optimized asset delivery service,](/help/developing/web-optimized-image-delivery.md) and includes bug fixes.|-|6.5.13.0+|Continual|8, 11|9 June 2022|
|[2.19.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.19.0)|This release adds a new version to the [Search Component](/help/components/quick-search.md) and features to the [Button Component](/help/components/button.md) as well as many accessibility improvements and bug fixes.|-|6.5.10.0+|Continual|8, 11|7 April 2022|
|[2.18.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.8)|This release fixes an issue for AEMaaCS.|-|6.5.10.0+|Continual|8, 11|17 March 2022|
|[2.18.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.6)|This is a patch release.|-|6.5.10.0+|Continual|8, 11|3 March 2022|
|[2.18.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.0)|This major release of the core components sees the introduction of a new link handler across new versions of multiple components along with many accessibility improvements and bug fixes.|-|6.5.10.0+ *|Continual|8, 11|16 February 2022|
|[2.17.14](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12)|This is a patch release.|6.4.8.4+|6.5.6.0+|Continual|8, 11|13 December 2021|
|[2.17.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12)|This is a patch release that fixes a regression introduced with the previous release.|6.4.8.4+|6.5.6.0+|Continual|8, 11|1 October 2021|
|[2.17.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.10)|This patch enhances the [List](/help/components/list.md) and [Navigation](/help/components/navigation.md) components to display the external URL for redirect targets, enables page images inheritance for the upcoming v2 of the [Teaser](/help/components/teaser.md) component, and contains additional bug fixes.|6.4.8.4+|6.5.6.0+|Continual|8, 11|31 August 2021|
|[2.17.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.8)|This patch release This is a patch release to fix a backward incompatible change which was introduced previously.|6.4.8.4+|6.5.6.0+|Continual|8, 11|2 August 2021|
|[2.17.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.6)|This patch release adds support for site maps for Pages and includes various accessibility improvements.|6.4.8.4+|6.5.6.0+|Continual|8, 11|29 July 2021|
|[2.17.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2)|This patch release includes a fix for the [Data Layer](/help/developing/data-layer/overview.md) not working with AEMaaCS.|6.4.8.4+|6.5.6.0+|Continual|8, 11|8 July 2021|
|[2.17.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0)|This release includes tech previews of many new component versions supporting link handler features as well as a tech preview of a featured image feature for the [Page Component.](/help/components/page.md) Several bug fixes are also included.|6.4.8.4+|6.5.6.0+|Continual|8, 11|16 June 2021|
|[2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4)|This is a patch release to fix an issue with the new Link Handler.|6.4.8.1+|6.5.5.0+|Continual|8, 11|19 May 2021|
|[2.16.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2)|This was a patch release mainly fixing an issue with the new Link Handler and added an enhancement to support multi-page applications for [PWA.](/help/components/page.md#pwa-support)|6.4.8.1+|6.5.5.0+|Continual|8, 11|15 May 2021|
|[2.16.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0)|This release focused on accessibility improvements as well as introducing a new Link Handler to existing components.|6.4.8.1+|6.5.5.0+|Continual|8, 11|22 April 2021|
|[2.15.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2)|This was a patch release mainly fixing issues with [Data Layer](/help/developing/data-layer/overview.md) backward compatibility and IT tests failing in certain situations.|6.4.8.1+|6.5.5.0+|Continual|8, 11|16 March 2021|
|[2.15.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0)|This release includes support for [progressive web apps (PWA) in the Page Component](/help/components/page.md#pwa-support) and supports version 2.0.0 of the [Adobe Data Layer.](/help/developing/data-layer/overview.md)|6.4.8.1+|6.5.5.0+|Continual|8, 11|23 February 2021|
|[2.14.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0)|This release includes new options for the [Embed Component](/help/components/embed.md) and introduces the Brand Slug at the [page](/help/components/page.md) level as well as addressing many issues.|6.4.8.1+|6.5.5.0+|Continual|8, 11|9 February 2021|
|[2.13.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2)|This was a patch release addressing an issue with the RTE when used on AEMaaCS |6.4.8.1+|6.5.5.0+|Continual|8, 11|16 December 2020|
|[2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0)|This release includes new Dynamic Media features for the [Image Component.](/help/components/image.md)|6.4.8.1+|6.5.5.0+|Continual|8, 11|4 December 2020|
|[2.12.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2)|This was a patch release for 2.12.0 including minor fixes.|6.4.8.1+|6.5.5.0+|Continual|8, 11|11 November 2020|
|[2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1)|This was a patch release for 2.12.0 that fixes a major bug in the [Image Component.](/help/components/image.md)|6.4.8.1+|6.5.5.0+|Continual|8, 11|5 November 2020|
|[2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0)|This release introduced [a new POST form handler;](/help/components/forms/form-container.md#post-data) the ability to include custom CSS, Javascript, and metadata [tags via context aware configuration;](/help/developing/including-clientlibs.md#context-aware-loading) and a `DataLayerBuilder` utility to [simplify data layer integration in custom components.](/help/developing/data-layer/integrations.md#enabling-custom-components)|6.4.8.1+|6.5.5.0+|Continual|8, 11|29 October 2020|
|[2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0)|This release introduced [AMP support.](/help/developing/amp.md)|6.4.8.1+|6.5.5.0+|Continual|8, 11|20 July 2020|
|[2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0)|This release introduced the [PDF Viewer component.](/help/components/pdf-viewer.md)|6.4.8.1+|6.5.5.0+|Continual|8, 11|17 June 2020|
|[2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0)|This release enabled integration with the [Adobe Client Data Layer](/help/developing/data-layer/overview.md) and introduced the [Progress Bar component.](/help/components/progress-bar.md)|6.4.8.0+|6.5.4.0+|Continual|8, 11|29 May 2020|
|[2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0)|This release focused on fixes with small enhancements.|6.4.4.0+|6.5.0.0+|Continual|8, 11|5 December 2019|
|[2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0)|This release introduced the new [Embed component.](/help/components/embed.md)|6.4.4.0+|6.5.0.0+|Continual|8, 11|25 September 2019|
|[2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0)|This release introduced the new [Experience Fragment component.](/help/components/experience-fragment.md)|6.4.4.0+|6.5.0.0+|Continual|8, 11|6 September 2019|
|[2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0)|This release introduced the new [Accordion,](/help/components/accordion.md) [Button,](/help/components/button.md) [Container,](/help/components/container.md) and [Download components.](/help/components/download.md)|6.4.2.0+|6.5.0.0+|Continual|8, 11|25 June 2019|
|[2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0)|This release introduced the [Content Fragment List Component.](/help/components/content-fragment-list.md)|6.4.2.0+|6.5.0.0+|Continual|8, 11|7 May 2019|
|[2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2)|This release focused on refinements to the [Component Library,](https://aemcomponents.dev) but also contains some feature enhancements for the [Separator Component.](/help/components/separator.md)|6.4.2.0+|6.5.0.0+|Continual|8|14 March 2019|
|[2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0)|This release focused on the [Component Library](https://aemcomponents.dev) as well as introducing the new [Separator Component,](/help/components/separator.md) but also contains some feature enhancements for the [Image Component.](/help/components/image.md)|6.4.2.0+|-|-|8|11 February 2019|
|[2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2)|This release mainly focused on bug fixes, but also contains some feature enhancements for the [Carousel Component.](/help/components/carousel.md)|6.4.2.0+|-|-|8|27 November 2018|
|[2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0)|This release introduced the [Tabs Component](/help/components/tabs.md) and the [Carousel Component](/help/components/carousel.md) as well as improvements to the [Image Component,](/help/components/image.md) [Page Component,](/help/components/page.md) and [Title Component](/help/components/title.md) and enhanced tracking.|6.4.2.0+|-|-|8|16 October 2018|
|[2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0)|This release introduced the [Teaser Component](/help/components/teaser.md) along with improvements to the [Image Component](/help/components/image.md) and numerous bug fixes.|6.4.2.0+|-|-|8|13 July 2018|
|[2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8)|This was a bugfix release.|6.4.0.0+|-|-|8|12 June 2018|
|[2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6)|This release added under-the-hood improvements, bug fixes, and small improvements including support of image flip in the [Image Component.](/help/components/image.md)|6.4.0.0+|-|-|8|11 April 2018|
|[2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4)|This release mostly focussed on under-the-hood improvements, bug fixes, plus some minor improvements to the [Image Component,](/help/components/image.md) [Page Component,](/help/components/page.md) and [Content Fragment Component.](/help/components/content-fragment-component.md)|6.4.0.0+|-|-|8|7 March 2018|
|[2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0)|This release introduced the [Navigation Component,](/help/components/navigation.md) [Language Navigation Component,](/help/components/language-navigation.md) and the [Quick Search Component](/help/components/quick-search.md) and implemented the [Style System](/help/get-started/authoring.md#component-styling) for all components.|6.4.0.0+|-|-|8|16 January 2018|
|[1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0)|This release implements JSON export on all components and introduces the [Content Fragment Component.](/help/components/content-fragment-component.md)|6.4.0.0+|-|-|8|10 October 2017|
|[1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6)|This release adds several fixes for the [Image Component.](/help/components/image.md)|6.4.0.0+|-|-|8|4 August 2017|
|[1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4)|This release adds fixes for the [Page Component,](/help/components/page.md) [Image Component,](/help/components/image.md) and various global fixes and improvements.|6.4.0.0+|-|-|8|26 April 2017|
|[1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2)|This release adds fixes for animated GIF images in [Image Component.](/help/components/image.md)|6.4.0.0+|-|-|7|22 March 2017|
|[1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0)|Initial release of Core Components.|6.4.0.0+|-|-|7|20 March 2017|

>[!TIP]
>
>As with AEM, Adobe recommends that developers use the [latest release and versions of the Core Components](https://github.com/adobe/aem-core-wcm-components/releases/latest) available that is compatible with the version of AEM that they are running in order to benefit from the most up-to-date fixes and features.

### Component Versions & Releases {#component-versions-and-releases}

The following table details which versions of which components are contained in which releases of the Core Components.

||Release 1.0.0 - 1.0.6|Release 1.1.0|Release 2.0.0 - 2.0.8|Release 2.1.0|Release 2.2.0-2.2.0|Release 2.3.0-2.3.2|Release 2.4.0|Release 2.5.0|Release 2.6.0|Release 2.7.0-2.8.0|Release 2.9.0-2.17.14|Release 2.18.0|Release 2.19.0|Release 2.20.0-2.21.2|Release 2.22.0+|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**[Page](components/page.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2, v3|v1, v2, v3|v1, v2, v3|v1, v2, v3|
|**[Title](components/title.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2, v3|v1, v2, v3|v1, v2, v3|v1, v2, v3|
|**[Image](components/image.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2, v3|v1, v2, v3|v1, v2, v3|v1, v2, v3|
|**[List](components/list.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2, v3|v1, v2, v3|v1, v2, v3|v1, v2, v3, v4|
|**[Breadcrumb](components/breadcrumb.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2, v3|v1, v2, v3|v1, v2, v3|v1, v2, v3|
|**[Social Media Sharing](components/sharing.md)**|v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|v1, deprecated|v1, deprecated|v1, deprecated|v1, deprecated|
|**[Form Container](components/forms/form-container.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Text](components/forms/form-text.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Options](components/forms/form-options.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Hidden](components/forms/form-hidden.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Form Button](components/forms/form-button.md)**|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Content Fragment](components/content-fragment-component.md)**||Sandbox|v1|v1|v1|v1|v1|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Navigation](components/navigation.md)**|||v1|v1|v1|v1|v1|v1|v1|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Language Navigation](components/language-navigation.md)**|||v1|v1|v1|v1|v1|v1|v1|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Quick Search](components/quick-search.md)**|||v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|v1, v2|v1, v2|v1, v2|
|**[Teaser](components/teaser.md)**||||v1|v1|v1|v1|v1|v1|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Tabs](components/tabs.md)**|||||v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|
|**[Carousel](components/carousel.md)**|||||v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|
|**[Separator](components/separator.md)**||||||v1|v1|v1|v1|v1|v1|v1|v1|v1|v1|
|**[Content Fragment List](components/content-fragment-list.md)**|||||||v1|v1|v1|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Accordion](components/accordion.md)**||||||||v1|v1|v1|v1|v1|v1|v1|v1|
|**[Button](components/button.md)**||||||||v1|v1|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Container](components/container.md)**||||||||v1|v1|v1|v1|v1|v1|v1|v1|
|**[Download](components/download.md)**||||||||v1|v1|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Experience Fragment](components/experience-fragment.md)**|||||||||v1|v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Embed](components/embed.md)**||||||||||v1|v1|v1, v2|v1, v2|v1, v2|v1, v2|
|**[Progress Bar](components/progress-bar.md)**|||||||||||v1|v1|v1|v1|v1|
|**[PDF Viewer](components/pdf-viewer.md)**|||||||||||v1|v1|v1|v1|v1|
|**[Table of Contents](components/tableofcontents.md)**||||||||||||||v1|v1|

## Versions and Releases {#versions-and-releases}

Core Components are distributed via GitHub. This allows Adobe to more quickly add functionality to the components and also allow for community input outside of the AEM release cycle.

The Core Components are made available with defined AEM versions with which they are compatible. This means that one AEM version may support multiple versions or releases of the Core Components.

### Versions {#versions}

The major iteration of the Core Components are the **versions**. Each component has a version. Versions are denoted with **v** appended with a nonzero, positive integer such as v1 and v2. Versions are incremented only for changes that are not backward-compatible, which is normally the case for the introduction of new features and functionality.

Developers and administrators can recognize versions of the core components by a number in their resource type paths, and in the fully qualified Java class names of their implementations. This version number represents a major version as defined by [semantic versioning guidelines](https://semver.org/).

For more details about core component versions, see the [developer documentation of the Core Components](developing/guidelines.md).

### Releases {#releases}

The core components are made available through **releases** and [represent the actual published artifacts available on GitHu.](https://github.com/adobe/aem-core-wcm-components/releases) Releases are denoted with a decimal number of the format `X.Y.Z` and collect all core components together as a deliverable package.

* **Major releases** introduce entirely new components, improvements to existing version of components, as well as standard bug fixes. This is represented by an increment in the `X` component of the release number.  
* **Minor releases** introduce new components, new functionality to existing versions of components, as well as bug fixes. This is represented by an increment in the `Y` component of the release number.  
* **Patch releases** contain only bug fixes. This is represented by an increment in the `Z` component of the release number.

>[!NOTE]
>
>Releases can contain multiple versions of the same component.
>
>The same version of a component can appear in multiple releases.

## Core Components Support {#core-components-support}

Core Components are an integral part of AEM and are supported under the same terms and conditions as if they were delivered as part of the Quickstart.

Like other product features, the general rule of end-of-life is:

* Components are first announced to be deprecated before being removed
* At the earliest they are then removed from the AEM release following the announcement.

This gives customers at least one release cycle to move to the new version of the component, before support ends.

The version of each component clearly states the AEM versions that it supports. When support ceases for a version of AEM, then so does the support of the Core Components for that version of AEM.

For details about the support of component customizations, see the [Customizing Core Components](developing/customizing.md) page of the relevant Core Components Version.

## Foundation Component Support {#foundation-component-support}

Adobe's development emphasis has shifted to the Core Components and new features will continue to be added.

[Nearly all Foundation Components have been deprecated with AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html) and only major bug fixes will be considered for the Foundation Components going forward.
