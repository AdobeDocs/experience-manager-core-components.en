---
title: Web-Optimized Image Delivery
description: Learn how the Core Components can leverage AEM as a Cloud Service's web-optimized image delivery features to deliver images more efficiently.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
---
# Web-Optimized Image Delivery {#web-optimized-image-delivery}

Learn how the Core Components can leverage AEM as a Cloud Service's web-optimized image delivery features to deliver images more efficiently.

## Overview {#overview}

The web-optimized image delivery feature of AEM as a Cloud service delivers image assets from the DAM in [WebP format.](https://developers.google.com/speed/webp) WebP can reduce the download size of an image by about 25% on average, which results in faster page loading.

Activating web-optimized image delivery in Core Components is simple, and because all common browsers support WebP, the experience is transparent to the end user. The only difference they will notice is that content loads faster!

## Activating Web-Optimized Image Delivery for Core Components {#activating}

To enable web-optimized image delivery, edit a page template and simply activate the option **Enable Web Optimized Images** within the design dialog of the [Image Component.](/help/components/image.md#design-dialog) This option is available for v1, v2, and v3 of the Image Component.

If you are not familiar with design dialogs and AEM's page templates, [please review this document.](/help/get-started/authoring.md#pre-configuring-core-components)

![Enabling web-optimized image delivery in the design dialog](/help/assets/web-optimized-image-delivery.png)

That's it! Images are now delivered by the Image Component in WebP format.

Once you activate web-optimized imaged delivery, you may want to check your dispatcher configuration to verify that it does not block request to the image delivery service. Please see [this FAQ entry](#failure-to-deliver) for more information.

## Verifying WebP Delivery {#verifying}

Web-optimized image delivery is transparent to the consumer of the content. The only thing that an end user will notice is faster load time. Therefore to observe any actual change of behavior, you must check the content-type of the rendered images in the browser. All modern browsers support WebP. You can refer to [this site](https://caniuse.com/webp) for details on browser support.

1. In AEM, edit a page that is based off of the template where you [activated web-optimized image delivery](#activating) for the Image Component.
1. Within the page editor, select the **Page Information** button at the top-left and then **View as Published**.
1. Open your browser's developer tools and select the network tab.
1. Reload the page and look for HTTP requests loading the images and check the content-type of the image that the browser received.

## When Web-Optimized Image Delivery is Unavailable {#fallback}

Web-optimized image delivery is only available in AEM as a Cloud Service. In cases where it is unavailable such as running AEM 6.5 on premise or on a local development instance, image delivery will fall back to using [the Adaptive Image Servlet.](/help/developing/adaptive-image-servlet.md)

Falling back to the Adaptive Image Servlet changes the `src` attribute of the `img` elements in the page source.

## Frequently-Asked Questions {#faq}

### Why is there no option to enable web-optimized images in my environment? {#missing-option}

The feature is only available on AEM as a Cloud Service. Running AEM locally or on premise, the Image Component [falls back](#fallback) to using the Adaptive Image Servlet.

### Why doesn't the service work with the local SDK? {#local-sdk}

When using the AEM SDK on `localhost`, the image service isn't available, and the image rendering [falls back](#fallback) to using the Adaptive Image Servlet.

To use the web-optimized image delivery service, deploy the project to a AEMaaCS development environment to be able to test precisely how the image service behaves with the image service.

### Why doesn't the service work for some images on my page? {#some-images}

The image service only works for assets located under `/content/dam` and it won't work for images uploaded directly to the page and stored under a `cq:Page` object. Such assets will still be delivered with the Adaptive Image Servlet as a [fallback.](#fallback)

### Why does the service display a worse quality image or limits the size of images? {#quality}

When image assets under `/content/dam` are processed, AEM as a Cloud Service environments generate optimized renditions of different dimensions. The web-optimized image service analyzes the width requested by the Image Core Component, considers the original image and all renditions that are 2048px and smaller, and picks the largest of those (within the size and dimension limits image service can handle, currently 50 MB and `12k`x`12k`) as the base to which it will apply the requested settings (width, crop, format, quality, etc).

To preserve fidelity of the output, the image service does not upscale images. The aforementioned renditions define the best quality that the image service will be able to deliver. Since you are often not be able to influence the size and/or dimensions of the original image asset, make sure that your image assets all have a 2048px zoom rendition, and if they don't, reprocess them.

### The URL of my images still end with .JPG or .PNG, not .WEBP, and there's no SRCSET attribute or PICTURE element. Is this really using optimized web formats? {#content-negotiation}

To deliver WebP formats, the web-optimized image delivery service performs [server-driven content negotiation.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) This helps selecting the optimal output format for the image based on client-advertized capabilities, allowing the image delivery service to ignore the file extension.

The advantage of leveraging content-negotiation is that the browsers that don't advertize support for WebP will still get the JPG or PNG file format without any change needed in the markup of the page. This offers optimal compatibility for existing sites, and guarantee the smoothest possible path to transition towards web optimized image delivery.

### Can I use web-optimized image delivery with my own component?

Yes, the web-optimized image delivery service can be used by custom components, which are built by [extending the Image Component,](/help/developing/customizing.md) 

The following is a service interface that can be used to help generating the asset URL.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>Direct URL embeds in an experience that is not built through aforementioned SPI (available on AEM as a Cloud Service Sites) are in violation of the [Media Library terms of usage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=en#use-media-library).

### Can images fail to display after enabling web optimized images? {#failure-to-deliver}

No, this should never happen for the following reasons.

* In the HTML, the markup doesn't change when enabling web optimized images, only the value of the `src` attribute on the image element changes.
* Whenever the new image service isn't available or cannot process the desired image, the URL generated will [fallback to the Adaptive Image Servlet.](#fallback)
* Dispatcher rules may block the web-optimized image delivery service. URLs of image delivery service start with `{{/adobe}}`, and examining [dispatcher logs for rejected requests](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html#filter-rejects) should help troubleshoot any failures encountered in delivering the images to browser.
