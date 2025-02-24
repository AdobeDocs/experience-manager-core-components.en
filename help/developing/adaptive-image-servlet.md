---
title: Adaptive Image Servlet
description: Learn how the Core Components uses the Adaptive Image Servlet for image delivery and how you can optimize its use.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
---
# Adaptive Image Servlet {#adaptive-image-servlet}

Learn how the Core Components uses the Adaptive Image Servlet for image delivery and how you can optimize its use.

>[!WARNING]
>
>For performance reasons it is highly recommend to store images in DAM and use web-optimized image delivery.
>
>Storing images directly under the component node is intended for occasional usage. It does not leverage the DAM renditions to reduce processing in the Adaptive Image Servlet and does not permit the performance benefits of web-optimized image delivery, resulting in possible performance issues.

## Adaptive Image Servlet or Web-Optimized Image Delivery? {#options}

The Image Core Component can use two methods to deliver images.

* The Adaptive Image Servlet is the default.
* [Web-optimized image delivery](/help/developing/web-optimized-image-delivery.md) is available to AEMaaCS and reduces download size by 25% on average.

This document describes the default Adaptive Image Servlet.

## Overview {#overview}

By default, the Image Component uses the Core Component's Adaptive Image Servlet to deliver images. [The Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) is responsible for image processing and streaming and can be leveraged by developers in their [customizations of the Core Components](/help/developing/customizing.md).

## Rendition Selection {#rendition-selection}

The Adaptive Image Servlet will automatically select the most appropriate rendition to display based on the size of the container in which it is displayed. The rendition selection process is as follows.

1.  The Adaptive Image Servlet reviews at all available renditions of the image asset.
1.  It selects only those with the same mime/type of the original referenced asset.
    * E.g. if the original asset was a PNG, it will only consider PNG renditions.
1.  Of those renditions it considers the dimensions, and comparing them to the size of the container in which the image should be displayed.
1.  If the rendition is &gt;= the container size, it is added to a list of candidate renditions. 
1.  If the rendition is &lt; the container size, it is disregarded.
1.  These criteria ensure that the rendition will not be upscaled, which would impact image quality.
1.  The Adaptive Image Servlet then picks the rendition with the smallest file size from the candidate list.

## Optimizing Rendition Selection {#optimizing-rendition-selection}

The Adaptive Image Servlet will try to pick the best rendition for the requested image size and type. It's recommended that DAM renditions and Image component allowed widths are defined in sync so that the Adaptive Image Servlet does as little processing as possible.

This will improve performance and avoid some images not being correctly processed by the underlying image processing library.

## Using Last-Modified Headers {#last-modified}

Conditional requests via the `Last-Modified` header are supported by the Adaptive Image Servlet, but the caching of the `Last-Modified` header [needs to be enabled in the Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers).

[The AEM Project Archetype's](/help/developing/archetype/overview.md) sample Dispatcher configuration already contains this configuration.
