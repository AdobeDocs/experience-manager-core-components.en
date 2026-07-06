---
title: AMP Support for the Core Components
description: The Core Components support AMP - Accelerated Mobile Pages
role: Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
TQID: https://experienceleague.adobe.com/5v1tXLzHNRvAxy6-aJipN-ZYzsPJ1xFNc1hKmz73wic
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
    internal-label: Mobile experience
---

# AMP Support for the Core Components {#amp-support}

As of [release 2.11.0](/help/versions.md) of the Core Components, [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) - are fully supported.

This document gives an overview of how AMP is supported as well as how to enable it for your sites. However for full technical details, please see the [GitHub developer documentation.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## What is AMP? {#what-is-amp}

Accelerated Mobile Pages or AMP is an open-source framework originally designed by Google to optimize pages for mobile browsing. AMP pages typically load much more quickly than standard web pages, offering better mobile experiences.

## AMP in the Core Components {#amp-in-core-components}

Support for AMP in the Core Components is [fully configurable.](#enabling-amp) AMP versions of pages can be served exclusively, alongside the standard HTML versions, or not at all.

The Core Components use `amp` as a Sling selector to render an AMP page. For example `example.html` would render the normal page and `example.amp.html` would be the AMP version.

Individual projects can decide whether or not to leverage AMP. In fact, because AMP and standard HTML pages can be delivered in parallel, a project can choose to use AMP on only certain pages of the project.

## Getting Started with AMP Support in Your Project {#getting-started}

Although AMP support offers a great deal of flexibility, to get started with it quickly requires only a few simple steps:

1. [Install the Core Components](/help/get-started/using.md#download-and-install)
   * For AEM as a Cloud Service projects, the Core Components are available by default and no additional installation is necessary.
   * For on-premise and AMS projects, you can [download the latest content package for the Core Components from GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) and to install it in your AEM environments.
   * If your on-premise or AMS project uses a Core Components release before 2.14.0, you also must install the AMP extension available as part of the release on GitHub. 
1. Point your component `resourceSuperType`s to `core/wcm/extensions/amp/components/page/v1/page`.
   * If you used [the AEM Project Archetype](/help/developing/archetype/using.md) for your project as recommended best practice and chose [the option to enable AMP support,](https://github.com/adobe/aem-project-archetype/tree/develop) this was done for you automatically.
1. [Enable AMP support](#enabling-amp) on the template level or on your individual pages.
1. [Deploy inlined CSS](#css-requirements) as required.

### Enabling AMP for Pages {#enabling-amp}

To enable AMP for a page, the **AMP Mode** must be selected in the [Page Policy.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![AMP Page Policy options](/help/assets/amp-policy.png)

* **No AMP** - The page is delivered as standard HTML only.
* **Paired AMP** - The page is delivered as AMP as well as HTML.
* **AMP Only** - The page is delivered as AMP only.

The AMP settings for a page can also be overridden in the [Page Properties](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) for an individual page.

![AMP Page Properties](/help/assets/amp-page-properties.png)

* **Inherit from Page Template** - This is the default value, which allows the setting to be taken from the page template's policy.
* **No AMP** - The page is delivered as standard HTML only.
* **Paired AMP** - The page is delivered as AMP as well as HTML.
* **AMP Only** - The page is delivered as AMP only.

These options appear in the UI only if the `resourceSuperType` is properly set for AMP support. The default WKND sample content does not have the `resourceSuperType` set and the options for AMP are therefore not visible in the UI.

### CSS Requirements {#css-requirements}

When using AMP with the Core Components, the main difference is that AMP requires all [CSS to be inlined](including-clientlibs.md#inlining) in the `<head>` element as well as optimized.

To support this, a customized page component is used, which loads just the AMP-specific CSS for components present on the page.

>[!NOTE]
>
>Due to AMP design limitations Adobe does not support the use of the Responsive Grid with the AMP version of your page.

For further requirements and technical details, please see the [GitHub developer documentation.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
