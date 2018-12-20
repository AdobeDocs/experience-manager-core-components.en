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

The current release of the Core Components is 2.2.2 and is compatible with AEM 6.3 and up. It was released in October 2018 as an important update to release 2.0.0. Release 2.0.0 introduced new components along with v2 updates of existing components.

See the section [Release History and Compatibility](versions.md#main-pars_title_236368006) of this document for more information.

## Versions and Releases {#versions-and-releases}

Core Components are distributed via GitHub. This allows Adobe to more quickly add functionality to the components and also allow for community input outside of the AEM release cycle.

The Core Components are made available with defined AEM versions with which they are compatible. This means that one AEM version may support multiple versions or releases of the Core Components. This gives more flexibility than the former Foundation Components, which were tied to a specific version of AEM.

### Versions {#versions}

The major iteration of the Core Components are the **versions**. Each component has a version. Versions are denoted with **v** appended with a nonzero, positive integer such as v1 and v2. Versions are incremented only for changes that are not backward-compatible, which is normally the case for the introduction of new features and functionality.

Developers and administrators can recognize versions of the core components by a number in their resource type paths, and in the fully qualified Java class names of their implementations. This version number represents a major version as defined by [semantic versioning guidelines](https://semver.org/).

For more details about core component versions, see the [developer documentation of the Core Components](guidelines.md#main-pars_title_1884592059).

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

<!--
<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <th><strong>Release</strong></th> 
   <th><strong>Description</strong></th> 
   <th><strong>AEM 6.3</strong><br /> </th> 
   <th><strong>AEM 6.4</strong></th> 
   <th><strong>Java</strong></th> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2">2.2.2</a></td> 
   <td>This release is mainly focused on bug fixes, but also contains some feature enhancements for the Carousel component</td> 
   <td>6.3.3.0</td> 
   <td>6.4.2.0</td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0">2.2.0</a></td> 
   <td>Tabs and Carousel components introduced, improvements to the image, page, and title components and enhanced tracking<br /> </td> 
   <td>6.3.3.0</td> 
   <td>6.4.2.0</td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0">2.1.0</a></td> 
   <td>Teaser Component introduced, Image Component improvements, and numerous bug fixes<br /> </td> 
   <td>6.3.3.0</td> 
   <td>6.4.2.0</td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8">2.0.8</a></td> 
   <td>Bugfix release</td> 
   <td>6.3.2.0</td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6">2.0.6</a></td> 
   <td>Additional under-the-hood improvements, bug fixes, and small improvements including support of image flip.</td> 
   <td>6.3.2.0</td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4">2.0.4</a></td> 
   <td>Mostly under-the-hood improvements, bug fixes, plus some minor improvements to the Image, Page, and Content Fragment Components<br /> </td> 
   <td>6.3.2.0<br /> </td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0">2.0.0</a></td> 
   <td>Navigation, Language Navigation, and Quick Search components introduced. Style system implemented for all components.<br /> </td> 
   <td>6.3.2.0<br /> </td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.8<br /> </td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0">1.1.0</a></td> 
   <td>Implementation of JSON export on all components, introduction of the Content Fragment component</td> 
   <td>6.3.1.0<br /> </td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6">1.0.6</a></td> 
   <td>Several fixes for the Image component</td> 
   <td>6.3.0.0<br /> </td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4">1.0.4</a></td> 
   <td>Fixes of Page Component, Image Component, various global fixes and improvements</td> 
   <td>6.3.0.0<br /> </td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.8</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2">1.0.2</a></td> 
   <td>Fixes for animated GIF images in Image component</td> 
   <td>6.3.0.0<br /> </td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.7</td> 
  </tr>
  <tr>
   <td><a href="https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0">1.0.0</a></td> 
   <td>Initial release of Core Components</td> 
   <td>6.3.0.0<br /> </td> 
   <td>6.4.0.0<br /> </td> 
   <td>1.7</td> 
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>As with AEM, Adobe recommends that developers use the [latest release and versions of the Core Components](https://github.com/adobe/aem-core-wcm-components/releases/latest) available that is compatible with the version of AEM that they are running in order to benefit from the most up-to-date fixes and features.

### Component Versions & Releases {#component-versions-releases}

The following table details which versions of which components are contained in which releases of the Core Components.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <th> </th> 
   <th><strong>Release 1.0.0 - 1.0.6</strong><br /> </th> 
   <th><strong>Release 1.1.0</strong><br /> </th> 
   <th><strong>Release 2.0.0 - 2.0.8</strong></th> 
   <th><strong>Release 2.1.0</strong></th> 
   <th><strong>Release 2.2.0+</strong></th> 
  </tr>
  <tr>
   <td><strong><a href="page.md">Page</a></strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="title.md">Title</a></strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="image.md">Image</a></strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="list.md">List</a></strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="breadcrumb.md">Breadcrumb</a></strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="sharing.md">Social Media Sharing</a></strong></td> 
   <td>v1<br /> </td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1</td> 
  </tr>
  <tr>
   <td><strong><a href="form-container.md">Form Container</a></strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="form-text.md">Form Text</a></strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="form-options.md">Form Options</a><br /> </strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="form-hidden.md">Form Hidden</a><br /> </strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="form-button.md">Form Button</a></strong></td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
   <td>v1, v2</td> 
  </tr>
  <tr>
   <td><strong><a href="content-fragment-component.md">Content Fragment</a><br /> </strong></td> 
   <td> </td> 
   <td>Sandbox<br /> </td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1</td> 
  </tr>
  <tr>
   <td><strong><a href="navigation.md">Navigation</a></strong></td> 
   <td> </td> 
   <td> </td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1</td> 
  </tr>
  <tr>
   <td><strong><a href="language-navigation.md">Language Navigation</a></strong></td> 
   <td> </td> 
   <td> </td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1</td> 
  </tr>
  <tr>
   <td><strong><a href="quick-search.md">Quick Search</a><br /> </strong></td> 
   <td> </td> 
   <td> </td> 
   <td>v1</td> 
   <td>v1</td> 
   <td>v1</td> 
  </tr>
  <tr>
   <td><strong><a href="teaser.md">Teaser</a></strong></td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>v1</td> 
   <td>v1</td> 
  </tr>
  <tr>
   <td><a href="tabs.md"><strong>Tabs</strong></a></td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>v1</td> 
  </tr>
  <tr>
   <td><a href="carousel.md"><strong>Carousel</strong></a></td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>v1</td> 
  </tr>
 </tbody>
</table>
-->

## Documentation {#documentation}

[Authoring with Core Components](authoring.md) describes the usage of the core components and the features that are exposed to content authors and template authors. Each component is documented in detail.

[Developing Core Components](developing.md) describes the technical capabilities of the Core Components, how to use them in your projects, how to customize, and best practices.

[Core Components Introduction](introduction.md) gives an overview of Core Components compatibility across versions, use cases, and support.
