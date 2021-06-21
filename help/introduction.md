---
title: Core Components Introduction
description: The Core Components provide robust and extensible base components, built on the latest technology and best practices. 
role: Architect, Developer, Administrator, Business Practitioner
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
---
# Core Components Introduction{#core-components-introduction}

In Adobe Experience Manager, components are the structural elements that constitute the content of the pages being authored. Components have always been a fundamental element of the AEM experience, making page creation simple but powerful for the author and the development of components flexible and extensible for the developer.

The Core Components are a set of standardized Web Content Management (WCM) components for AEM to speed up development time and reduce maintenance cost of your websites.

## Resources {#resources}

* **[Component Library:](https://www.adobe.com/go/aem_cmp_library)** A collection of examples to view the components in their various configurations.
* **Component Documentation (this document):** For developers and authors, with details about each component.
* **[Core Components GitHub Repository:](https://github.com/adobe/aem-core-wcm-components)** For developer details of each component and project download.
* Get Started:
  * **[Success with the Core Components:](/help/developing/success.md)** Guidelines to consider well before the start of any project that will use the Core Components.
  * **[WKND Tutorial:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** A two-day tutorial for building a new site.
  * **[Summit Tutorial:](https://expleague.azureedge.net/labs/L767/index.html)** A two-hour tutorial for building a new site (from a Lab at US Summit 2019).
  * **[Gems Webinar:](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** A guided tour of the Core Components (recorded on Dec 2018).

## Features {#features}

|||
|---|---|
|Production-Ready| The Core Components are 28 robust components that are well tested, widely used, and that perform well.|
|Cloud-Ready| Whether on [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), on [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), or on-premise, they just work.|
|Versatile| The components represent generic concepts with which the authors can assemble nearly any layout.|
|Configurable| Template-level [content policies](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#content-policies) define which features the page authors are allowed to use or not use.|
|Trackable|The [Adobe Client Data Layer integration](/help/developing/data-layer/overview.md) allows tracking of all aspects of the visitor experience.|
|Accessible| They comply [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, and support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)).|
|SEO-Friendly| The HTML output is semantic and provides [schema.org](https://schema.org) microdata annotations.|
|WebApp-Ready| The [streamlined JSON output](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) allows client-side rendering, still with a possibility of [in-context editing](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).|
|AMP Support| The components have built-in [support for the AMP standard,](/help/developing/amp.md) accelerating your mobile experiences.|
|Design Kit| A [UI kit for Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) allows designers to create wireframes that they can then [style as needed](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd).|
|Themeable| The components implement the [Style System](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/).|
|Customizable| Several patterns allow [easy customization](developing/customizing.md), from adjusting the HTML to advanced functionality reuse.|
|Versioning| The [versioning policy](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) ensures that the Core Components won't break your site when improving things that might impact you.|
|Localizable|Smart reference resolution allows certain components to find and [render corresponding localized content automatically](get-started/localization.md).|
|Open Sourced| If something is not as it should, [contribute your improvements!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md)|

## The Components {#the-components}

The current version of the Core Components features the following components.

### Template Components {#template-components}

* [Page](components/page.md)
* [Navigation](components/navigation.md)
* [Language Navigation](components/language-navigation.md)
* [Breadcrumb](components/breadcrumb.md)
* [Quick Search](components/quick-search.md)

### Page Authoring Components {#page-authoring-components}

* [Title](components/title.md)
* [Text](components/text.md)
* [Image](components/image.md)
* [Button](components/button.md)
* [Teaser](components/teaser.md)
* [Download](components/download.md)
* [List](components/list.md)
* [Experience Fragment](components/experience-fragment.md)
* [Content Fragment](components/content-fragment-component.md)
* [Content Fragment List](components/content-fragment-list.md)
* [Embed](components/embed.md)
* [Social Media Sharing](components/sharing.md)
* [Separator](components/separator.md)
* [Progress Bar](components/progress-bar.md)
* [PDF Viewer](components/pdf-viewer.md)

### Container Components {#container-components}

* [Container](components/container.md)
* [Carousel](components/carousel.md)
* [Tabs](components/tabs.md)
* [Accordion](components/accordion.md)

### Form Components {#form-components}

* [Form Container](components/forms/form-container.md)
* [Form Text](components/forms/form-text.md)
* [Form Options](components/forms/form-options.md)
* [Form Hidden](components/forms/form-hidden.md)
* [Form Button](components/forms/form-button.md)

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Some versions of individual Core Components may only be compatible with certain versions of AEM.
>
>See the individual help page (linked to in the previous list) for the specific component for compatibility information or reference the [Core Components Versions](versions.md) document for more information.

## System Requirements {#system-requirements}

|Core Components | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | Maven|
|---------|---------|---------|---------|---------|---------|
|[2.17.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | Continual | 6.5.6.0+ * | 6.4.8.4+ * | 8, 11 | 3.3.9+|

>[!NOTE]
>
>(*) Since version 2.11.0, `org.apache.sling.models.impl` version 1.4.12 or higher is required (due to [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). This will be provided for AEM 6.4 and 6.5 in a future Service Pack. Until then, the Sling Models bundle is included in the `core.wcm.components.all` package.

For the requirements from previous Core Component releases, see [Core Components Versions](versions.md).

The Core Components require the use of [editable templates](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) and do not support Classic UI nor static templates. If needed, check out the [AEM Modernization Tools](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) to update your project with these modern AEM features.

To setup your local development environment, check out [this overview for AEM as a Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) or this document [for older versions of AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

>[!TIP]
>
>The Core Components are automatically part of AEM as a Cloud Service and you always have the latest release of the Core Components.
>
>See the [Using Core Components](/help/get-started/using.md) document for more information on how to get started with the Core Components both in AEMaaCS and on premises.
