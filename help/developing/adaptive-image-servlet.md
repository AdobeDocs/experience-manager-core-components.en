---
title: Adaptive Image Servlet
description: Learn how the Core Components uses the Adaptive Image Servlet for image delivery and how you can optimize its use.
role: Architect, Developer, Admin, User
---

# Adaptive Image Servlet {#adaptive-image-servlet}

Learn how the Core Components uses the Adaptive Image Servlet for image delivery and how you can optimize its use.

## Adaptive Image Servelt or Web-Optimized Image Delivery? {#options}

The Image Core Component can use two methods to delivery images.

* The Adaptive Image Servlet is the default.
* [Web-optimized image delivery](/help/developing/web-optimized-image-delivery.md) is available to AEMaaCS and reduces download size by 25% on average.

This document describes the default Adaptive Image Servlet.

## Overview {#overview}

By default, the Image Component uses the Core Component's Adaptive Image Servlet to deliver images. [The Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) is responsible for image processing and streaming and can be leveraged by developers in their [customizations of the Core Components](/help/developing/customizing.md).

## Optimizing Rendition Selection {#optimizing-rendition-selection}

The Adaptive Image Servlet will try to pick the best rendition for the requested image size and type. It's recommended that DAM renditions and Image component allowed widths are defined in sync so that the Adaptive Image Servlet does as little processing as possible.

This will improve performance and avoid some images not being correctly processed by the underlying image processing library.

## Using Last-Mofified Headers {#last-modified}

Conditional requests via the `Last-Modified` header are supported by the Adaptive Image Servlet, but the caching of the `Last-Modified` header [needs to be enabled in the Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers).

[The AEM Project Archetype](/help/developing/archetype/overview.md)'s sample Dispatcher configuration already contains this configuration.
