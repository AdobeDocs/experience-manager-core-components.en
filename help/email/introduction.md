---
title: Email Core Components Introduction
description: Create compelling email content using the flexibility of the Email Core Components and deliver it with the power of Adobe Campaign.
role: Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
index: false
TQID: https://experienceleague.adobe.com/PLDfeItW57FUgvSUO7kHgeNP8KogBwVA2AeEd-srbwg
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: ae478996-b206-4712-9b0c-dc78a2644453
    internal-label: Integrations
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
    internal-label: Integrations
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
    internal-label: Personalization
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
    internal-label: Editable templates
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Email Core Components Introduction {#email-core-components-introduction}

Create compelling email content using the flexibility of the Email Core Components and deliver it with the power of Adobe Campaign.

## Overview {#overview}

The Email Core Components are built on the same powerful foundation of the Core Components. They enable simple and flexible drag-and-drop authoring of email content which can then be delivered to your audience using the power of Adobe Campaign.

## Benefits {#benefits}

Emails are part of the brand experience and customer journey. With the Email Core Components, your authors can craft email content from within AEM, offering a consistently-branded experience and thereby increasing content velocity.

* Just like authoring pages with the Core Components, the Email Core Components allow authors to assemble email without technical knowledge while ensuring that they follow branding guidelines.
* The capability to reuse assets and content also encourages authors to follow branding guidelines and optimize the content creation process.

## Features {#features}

* The Core Email Components are based on the [Core Components,](/help/introduction.md) and therefore also support [Editable Templates](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) and the [Style System.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html)
* There are [ten email-optimized production-ready components](#components) to author email content.
* The Core Email Components provide advanced personalization thanks to the insertion of [Adobe Campaign variables](campaign-variables.md) on most dialog fields.
* The flexible [Segmentation component](/help/email/components/segmentation.md) allows for advanced segmentation of your content.
* The Core Email Components provide optimal email-friendly HTML output thanks to the [CSS styles inliner,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation) [the HTML attribute inliner,](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) and [the HTML sanitizer.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* You can create email content anywhere below `/content`.
* The Email Core Components are [open source.](https://github.com/adobe/aem-core-email-components)

## Requirements {#requirements}

The Email Core Components have the following requirements.

|AEM|Adobe Campaign|Core Components|
|---|---|---|
|AEM 6.5.14.0+<br>On-premises or AMS|Adobe Campaign Classic<br>Adobe Campaign Standard|[Release 2.21.2](/help/versions.md)+|

>[!NOTE]
>
>Because the Adobe Campaign integrations are not supported in AEM as a Cloud Service, the Email Core Components are likewise not supports in AEM as a Cloud Service.

## The Email Components {#components}

The current version of the Email Core Components features the following components.

* [Page](components/page.md)
* [Container](components/container.md)
* [Title](components/title.md)
* [Text](components/text.md)
* [Image](components/image.md)
* [Button](components/button.md)
* [Teaser](components/teaser.md)
* [Experience Fragment](components/experience-fragment.md)
* [Content Fragment](components/content-fragment.md)
* [Segmentation](components/segmentation.md)

## Installation and Usage {#installation-usage}

See the [Using the Email Core Components](using.md) document for details on installing the Email Core Components.
