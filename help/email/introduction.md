---
title: Email Core Components Introduction
description: Create compelling email content using the flexibility of the Email Core Components and deliver it with the power of Adobe Campaign.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
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
|AEM 6.5.14.0+<br>On premise or AMS|Adobe Campaign Classic<br>Adobe Campaign Standard|[Release 2.21.2](/help/versions.md)+|

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
