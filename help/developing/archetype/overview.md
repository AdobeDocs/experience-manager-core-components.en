---
title: AEM Project Archetype
description: Learn about the AEM Project Archetype which serves as a template for AEM-based applications.
feature: Core Components, AEM Project Archetype
role: Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
TQID: https://experienceleague.adobe.com/snvIzunCCWegShAzgcg9Zpof00Wq-tAYkaoGvq4RwEk
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
    internal-label: Editable templates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: ce44533e-8ec8-4e11-a9e9-78b0fe561832
    internal-label: Content structure
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
---
# AEM Project Archetype {#aem-project-archetype}

The AEM Project Archetype is a Maven template that creates a minimal, best-practices-based Adobe Experience Manager (AEM) project as a starting point for your website. This documentation provides an overview of the benefits of the archetype and general usage. Detailed technical instructions and documentation can be found in the archetype GitHub repository.

>[!TIP]
>
>The latest AEM Project Archetype and associated technical documentation [can be found on GitHub.](https://github.com/adobe/aem-project-archetype)

{{traditional-aem}}

## Why Use the Archetype {#why-use-the-archetype}

Using the AEM Project Archetype sets you on the path towards building a best-practices-based AEM project with just a few keystrokes. By using the archetype, all of the pieces will already in place so that while the resulting project is minimal, it already implements all of the [key features](/help/developing/archetype/using.md#what-you-get) of AEM so that all you have to do is build on top and extend.

Of course there are many elements that go into [a successful AEM project,](/help/developing/success.md) but using the AEM Project Archetype is a sound foundation and is strongly recommended for any AEM project.

## Features {#features}

* **Best Practice:** Bootstrap your site with all of Adobe's latest recommended practices.
* **Low-Code:** Edit your templates, create content, deploy your CSS, and your site is ready for go-live.
* **Cloud-Ready:** If desired, use [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html) to go-live in few days and ease scalability and maintenance.
* **Dispatcher:** A project is complete only with a [Dispatcher configuration](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html) that ensures speed and security.
* **Multi-Site:** If needed, the archetype generates the content structure for a [multi-language and multi-region setup](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html).
* **Core Components:** Authors can create nearly any layout with our versatile [set of standardized components](/help/introduction.md).
* **Editable Templates:** Assemble virtually any [template without code](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html), and define what the authors are allowed to edit.
* **Responsive Layout:** On templates or individual pages, [define how the elements reflow](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html) for the defined breakpoints.
* **Header and Footer:** Assemble and localize them without code, using the [localization features of the components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html).
* **Style System:** Avoid building custom components by allowing authors to [apply different styles](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html) to them.
* **Front-End Build:** Front-end developers can [mock AEM pages and build client libraries](front-end.md) with Webpack, TypeScript, and SASS.
* **WebApp-Ready:** For sites using React or Angular, use the [SPA SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html) to retain [in-context authoring of the app](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Commerce Enabled:** For projects that want to integrate [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html) with commerce solutions like [Magento](https://magento.com/) using the [Commerce Core Components](https://github.com/adobe/aem-core-cif-components).
* **Example Code:** Checkout the HelloWorld component, and the sample models, servlets, filters, and schedulers.
* **Open Sourced:** If something is not as it should, [contribute](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) your improvements!

## Further Reading {#further-reading}

* **[AEM Project Archetype GitHub](https://github.com/adobe/aem-project-archetype)** - For full usage and technical details of the archetype
* **[Using the Archetype](using.md)** - An overview of how to use the archetype in your project and the resulting modules generated
* **[Front-End Development with the AEM Project Archetype](front-end.md)** - How to use the front-end module of the archetype
* **The following tutorials are based off the archetype:**
  * **[WKND Site](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** - Learn how to start a fresh new website.
  * **[WKND Single Page App](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** - Learn how to build a React or Angular webapp that is fully authorable in AEM.
