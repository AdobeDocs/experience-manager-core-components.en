---
title: Web-Optimized Image Delivery
description: Learn how the Core Components can leverage AEM as a Cloud Service's web-optimized image delivery features to deliver images more efficiently.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
---
# Web-Optimized Image Delivery {#web-optimized-image-delivery}

Learn how the Core Components can leverage AEM as a Cloud Service's web-optimized image delivery features to deliver images more efficiently.

>[!NOTE]
>
>The web-optimized image delivery service is a prerelease feature feature with the June 2022 release of AEM as a Cloud Service with GA expected in July.
>
>For more information about AEMaaCS's prerelease features, see the document [Adobe Experience Manager as a Cloud Service Prerelease Channel](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html)

## Overview {#overview}

The web-optimized image delivery feature of AEM as a Cloud service delivers image assets from the DAM in [WebP format.](https://developers.google.com/speed/webp) WebP can reduce the download size of an image by about 25% on average, which results in faster page loading.

Activating web-optimized image delivery in Core Components is simple, and because all common browsers support WebP, the experience is transparent to the end user. The only difference they will notice is that content loads faster!

## Activating Web-Optimized Image Delivery for Core Components {#activating}

To enable web-optimized image delivery, edit a page template and simply activate the option **Enable Web Optimized Images** within the design dialog of the [Image Component.](/help/components/image.md#design-dialog) This option is available for v1, v2, and v3 of the Image Component.

If you are not familiar with design dialogs and AEM's page templates, [please review this document.](/help/get-started/authoring.md#pre-configuring-core-components)

![Enabling web-optimized image delivery in the design dialog](/help/assets/web-optimized-image-delivery.png)

That's it! Images are now delivered by the Image Component in WebP format.

Once you activate web-optimized imaged delivery, you may want to also check your dispatcher configuration to verify that it does not block request to the image service. URLs of this service take the following form.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

This can be generalized with this regular expression.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Verifying WebP Delivery {#verifying}

Web-optimized image delivery is transparent to the consumer of the content and does not affect the markup. The only thing that an end user will notice is faster load time.

Therefore to observe the actual change of behavior, you must view the page source.

1. In AEM, edit a page that is based off of the template where you [activated web-optimized image delivery](#activating) for the Image Component.
1. Within the page editor, select the **Page Information** button at the top-left and then **View as Published**.
1. Using your browsers developer tools, view the source of the page and see how the rendered markup stays the same, but that the image in the `src` attribute points to [the URL of the new image service.](#activating)

## When Web-Optimized Image Delivery is Unavailable {#fallback}

Web-optimized image delivery is only available in AEM as a Cloud Service. In cases where it is unavailable such as running AEM 6.5 on premise or on a local development instance, image delivery will fall back to using [the Adaptive Image Servlet.](/help/developing/adaptive-image-servlet.md)

Just as enabling web-optimized image delivery does not affect the markup, falling back to the Adaptive Image Servlet likewise has no effect on the markup since only the URL in the `src` attribute of the `img` element is changed.

## Frequently-Asked Questions {#faq}

### Why is there no such option to enable web-optimized images in my environment? {#missing-option}

The feature is only available on AEM as a Cloud Service. Running AEM locally or on premise, the Image Component [falls back](#fallback) to using the Adaptive Image Servlet.

### Why doesn't the service work with the local SDK? {#local-sdk}

When using the AEM SDK on `localhost`, the image service isn't available, and the image rendering [falls back](#fallback) to using the Adaptive Image Servlet.

To use the web-optimized image delivery service, deploy the project to a AEMaaCS development environment to be able to test precisely how the image service behaves with the image service.

### Why doesn't the service work for some images on my page? {#some-images}

The image service only works for assets located under `/content/dam` and it won't work for images uploaded directly to the page and stored under a `cq:Page` object. Such assets will still be delivered with the Adaptive Image Servlet as a [fallback.](#fallback)

### Why does the service display a worse quality image or limits the size of images? {#quality}

The web-optimized image service considers all image renditions that are 2048px and smaller and picks the largest of those as the base on which it will apply the requested settings (width, crop, format, quality, etc). 

The image service will never upscale images. These renditions therefore define the best size and quality that the image service will be able to deliver. Therefore make sure that your assets all have the 2048px zoom rendition, and if they don't, reprocess them.

### The URL of my images still end with .JPG or .PNG, not .WEBP, and there's no SRCSET attribute or PICTURE element. Is this really using optimized web formats? {#content-negotiation}

To deliver WebP formats, the web-optimized image delivery service uses a technique called "content negotiation". This consists in returning a WebP file format, even when requesting a JPG or PNG file extension, but only when the browser making the request provided an `image/webp` HTTP accept header. Browsers supporting this technique can then provide this header, and older browsers will still get the JPG or PNG file format.

The advantage of this technique is that the `img` element and its attributes can remain the same, which will lead to an optimal compatibility for existing sites, and guarantee the smoothest possible path to transition towards web optimized image delivery.

### Can I use web-optimized image delivery with my own component?

Yes, the web-optimized image delivery service can be used by custom components. Adobe recommends [extending the Image Component](/help/developing/customizing.md) in this case.

The following is a service interface that can be used to help generating the asset URL.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

This service takes an asset resource as mandatory first parameter and can take an optional map of desired image transformations that are to be applied which can contain the following parameters.

* `path` – Asset ID that is to be delivered, must be of pattern `([^:\[\]\|\*\/]+)` (e.g.: `unicorn–1234`)
* `seoname` – User-defined, SEO-centric name to be appended to the image URL, may contain hyphens, must be of pattern `([\w-]+)` (e.g.: `my-friend-the-unicorn`)
* `format` – The desired image format, can be `gif`, `png`, `png8`, `jpg`, `pjpg`, `bjpg`, `webp`, `webpll`, `webply` (e.g.: `webp`)
* `preferwebp` – If possible, deliver WebP output, ignoring the `format` parameter ([see FAQ about content negotiation](#content-negotiation)), boolean (e.g.: `true`)
* `width` – The desired image resolution in pixels, must be greater than 1 (e.g.: `400`)
* `quality` – The desired compression, between `1` and `100` (e.g.: `75`)
* `c` – The desired image cropping coordinates, comma-separated pixel values (e.g.: `100,100,400,200`)
* `r` – The desired image rotation, can be `90`, `180`, `270` (e.g.: `90`)
* `flip` – The desired image flipping, can be `h`, `v`, `hv` (e.g.: `h`)

### What is the URL of an image delivered by the new image service? {#url}

See the previous section [Activating Web-Optimized Image Delivery for Core Components](#activating) for an example URL and regular expression.

### Can images fail to display after enabling web optimized images?

No, this should never happen.

* In the HTML, the markup doesn't change when enabling web optimized images, only the value of the SCR attribute on the image element changes.
* Whenever the new image service isn't available or cannot process the desired image, the URL generated will [fallback to the Adaptive Image Servlet.](#fallback)
* Dispatcher rules may block the web-optimized image service and [should be checked when activating the feature.](#activating)
