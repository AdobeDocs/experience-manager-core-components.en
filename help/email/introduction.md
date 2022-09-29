---
title: Email Core Components Introduction
description: Author compelling email content using the flexibility of the Email Core Components and deliver it with the power of Adobe Campaign. 
role: Architect, Developer, Admin, User
---

# Email Core Components Introduction {#email-core-components-introduction}

Author compelling email content using the flexibility of the Email Core Components and deliver it with the power of Adobe Campaign.

## Overview {#overview}

The Email Core Components are built on the same powerful foundation of the Core Components. They enable simple and flexible drag-and-drop authoring of email content which can then be delivered to your audience using the power of Adobe Campaign.

## Benefits {#benefits}

Emails are part of the brand experience and customer journey. With the Email Core Components, your authors can craft email content from within AEM, offering a consistently-branded experience and thereby increasing content velocity.

* Just like authoring pages with the Core Components, the Email Core Components allow authors to assemble email without technical knowledge while ensuring that they follow branding guidelines.
* The capability to reuse assets and content also encourages authors to follow branding guidelines and optimize the content creation process.

## Features {#features}

* The Core Email Components are based on the [Core Components,](/help/introduction.md) and therefore also support [Editable Templates](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) and the [Style System.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html)
* There are [10 email-optimized production-ready components](#components) to author email content.
* The Core Email Components provide advanced personalization thanks to the insertion of Adobe Campaign variables on most dialog fields.
* The flexible Segmentation component allows for advanced segmentation of your content.
* The Core Email Components provide optimal email-friendly HTML output thanks to the CSS styles inliner, the HTML attribute inliner, and the HTML sanitizer.
* You can create email content anywhere below `/content`.
* The Email Core Components are [open source.](https://github.com/adobe/aem-core-email-components)

## Requirements {#requirements}

The Email Core Components have the following requirements.

|AEM|Adobe Campaign|Core Components|
|---|---|---|
|AEMaaCS<br>or<br>AEM 6.5.x.y (on premise or AMS)|Adobe Campaign Classic vX<br>or<br>Adobe Campaign Standard*|[Release x](/help/versions.md) or higher|

*See limitations section.

## Limitations {#limitations}

The personalization and segmentation features of the Email Core Components are not supported by Adobe Campaign Standard.

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
