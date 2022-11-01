---
title: Email Image Component
description: The Email Image Component is an adaptive image component that features in-place editing.
role: Architect, Developer, Admin, User
hidefromtoc: yes
index: no
---

# Email Image Component {#email-image-component}

The Email Image Component is an adaptive image component that features in-place editing.

## Usage {#usage}

The Email Image Component features adaptive image selection and responsive behavior with lazy loading for the page visitor as well as easy drag-and-drop image placement and configuration for the content author.

* The image widths and additional settings can be defined by the template author in the [design dialog.](#design-dialog)
* The content editor can upload or select assets in the [configure dialog.](#configure-dialog)

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Image Component is v1, which was introduced with release x of the Email Core Components in October 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM as a Cloud Service|
|---|---|---|
|v1|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Email Core Components Versions](/help/email/versions.md).

## Responsive Features {#responsive-features}

The Email Image Component comes with robust responsive features ready right out of the box. At the page template level, the [design dialog](#design-dialog) can be used to define the default widths of the image asset. The Email Image Component will then automatically load the correct width to display depending on the size of the browser window. As the window is resized, the Email Image Component dynamically loads the correct image size on the fly. There is no need for component developers to worry about defining custom media queries since the Email Image Component is already optimized to load your content.

In addition, the Email Image Component supports lazy loading to defer loading of the actual image asset until it is visible in the browser, increasing the responsiveness of your content.

>[!TIP]
>
>By default, the Email Image Component is powered by the Adaptive Image Servlet. Please see the document [Adaptive Image Servlet](#adaptive-image-servlet) for details on how it works.

## Dynamic Media Support {#dynamic-media}

The Email Image Component supports [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html#dynamicmedia) assets. [When enabled,](#design-dialog) these features offer the ability to add Dynamic Media image assets with a simple drag-and-drop or via the assets browser just as you would any other image. In addition, image modifiers, image presets, and smart crops are also supported.

Your email experiences built with the Email Core Components can feature rich, Sensei-powered, robust, high-performance, cross-platform Dynamic Media Image capabilities.

## SVG Support {#svg-support}

Scalable Vector Graphics (SVG) are supported by the Email Image Component.

* Drag-and-drop of an SVG asset from DAM and upload of an SVG file upload from a local file system are both supported.
* The original SVG file is streamed (transformations are skipped).
* For an SVG image, the "smart images" and the "smart sizes" are set to an empty array in the image model.

### Security {#security}

For security reasons, the original SVG is never called directly by the Image Editor. It is called through `<img src=“path-to-component”>`. This prevents the browser from executing any scripts embedded in the SVG file.

## Sample Component Output {#sample-component-output}

To experience the Email Image Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library.](https://adobe.com/go/aem_cmp_library_email_image)

### Technical Details {#technical-details}

The latest technical documentation about the Email Image Component [can be found on GitHub.](https://adobe.com/go/aem_cmp_tech_email_image_v1)

Further details about developing Core Components can be found in the [Core Components developer documentation.](/help/developing/overview.md)

The Image Component supports [schema.org microdata.](https://schema.org)

## Configure Dialog {#configure-dialog}

The Email Image Component offers a configure dialog where the image itself is defined along with its description and basic properties.

### Asset Tab {#asset-tab}

![Asset tab of the Email Image Component's configure dialog](/help/email/assets/email-image-configure-asset.png)

* **Inherit featured image from page** - This option uses the [featured image of the linked page](page.md) or the featured image of the current page if the image is not linked.

* **Alternative text for accessibility** - This field allows you to define a description of the image for visually impaired users.

  * **Inherit alternative text from page** - This option uses the alternative description of the linked asset value of the `dc:description` metadata in DAM or of the current page if no asset is linked. 

* **Image asset**
  * Drop an asset from the [asset browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) or tap the **browse** option to upload from a local file system.
  * Tap or click **Clear** to de-select the currently selected image.
  * Tap or click **Edit** to [manage the renditions of the asset](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in the Asset Editor.

* **Don't provide an alternative text** - This option marks the image to be ignored by assistive technologies like screen readers for cases where the image is purely decorative or otherwise conveys no additional information to the page.

* **Disable lazy loading** - This option preloads all image components without loading as needed.

### Metadata Tab {#metadata-tab}

![Metadata tab of the Image Component's configure dialog](/help/email/assets/email-image-configure-metadata.png)

* **Preset Type** - This defines the types of image presets available, either **Image Preset** or **Smart Crop**, and is only available when [Dynamic Media features](#dynamic-meida) are enabled.
  * **Image Preset** -  When **Preset Type** of **Image Preset** is selected, the drop-down **Image Preset** is available, allowing selection from the available Dynamic Media presets. This is only available if presets are defined for the selected asset.
  * **Smart Crop** - When **Preset Type** of **Smart Crop** is selected the drop-down **Rendition** is available, allowing selection from the available renditions of the selected asset. This is only available if renditions are defined for the selected asset.
  * **Image Modifiers** - Additional Dynamic Media image-serving commands can be defined here separated by `&`, regardless of which **Preset Type** is selected.
* **Caption** - Additional information about the image, displayed below the image by default.
  * **Get caption from DAM** - When checked the image's caption text will be populated with the value of the `dc:title` metadata in DAM. Only available when an asset is chosen from the DAM.
  * **Display caption as pop-up** - When checked, the caption won't be displayed below the image, but as a pop-up displayed by some browsers when hovering over the image.
* **Link** - Link the image to another resource.
  * Use the selection dialog to link to another AEM resource.
  * If not linking to an AEM resource, enter the absolute URL. Non-solute URLs will be interpreted as relative to AEM.
  * **Open link in new tab** - This option opens the link in a new browser window.
* **ID** - This option allows controlling the unique identifier of the component in the HTML.
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS.
* **Fixed with** - This option defines the width in pixels of the image.
* **Scale image to available width** - This option applies `"width":"100%"` to the image style attribute.

>[!TIP]
>
>**Smart Crop** and **Image Preset** are mutually exclusive options. If an author needs to use an image preset along with a Smart Crop rendition, the author will have to use the **Image Modifiers** to manually add presets.

### Styles Tab {#styles-tab-edit}

![Styles tab of the edit dialog of Email Image Component](/help/assets/image-configure-styles.png)

The Email Image Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the tab to be available.

## Design Dialog {#design-dialog}

### Main Tab {#main-tab}

![Image Component's design dialog main tab](/help/email/assets/email-image-design-main.png)

* **Enable DM features** - When checked, [Dynamic Media features](#dynamic-media) are available.
  * This option only appears when Dynamic Media is enabled in the environment.
* **Enable Web Optimized Images** - When checked, [the web-optimized image delivery service](/help/developing/web-optimized-image-delivery.md) will deliver images in the WebP format, reducing image sizes on average by 25%.
  * This option is only available in AEMaaCS.
  * When unchecked or when the web-optimized image delivery service is unavailable the [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md) is used.
* **Image is decorative** - Define if the decorative image option is automatically enabled when adding the image component to a page.
* **Get alternative text from DAM**-  Define if the option to retrieve the alternate text from the DAM is automatically enabled when adding the image component to a page.
* **Get caption from DAM** - Define if the option to retrieve the caption from the DAM is automatically enabled when adding the image component to a page.
* **Display caption as pop-up** - Define if the option to display the image caption as a pop-up is automatically enabled when adding the image component to a page.
* **Resize width** - This value is used for resizing the width of the base images that are DAM assets.
  * The aspect ratio of the images will be preserved.
  * If the value is larger than the actual width of the image, this value will have no effect.
  * This value has no effect on SVG images.

You can define a list of widths in pixels for the image and the component will automatically load the most appropriate width based on browser size. This is an important part of the [responsive features](#responsive-features) of the Email Image Component.

* **Widths** - Defines a list of widths in pixels for the image and the component automatically loads the most appropriate width based on browser size.
  * Tap or click the **Add** button to add another size.
    * Use the grab handles to rearrange the order of the sizes.
    * Use the **Delete** icon to remove a width.
  * By default images loading is deferred until they become visible.
    * Select the option **Disable lazy loading** to load the images upon page load.
* **JPEG Quality** - The quality factor (in percentage from 0 and 100) for transformed (e.g. scaled or cropped) JPEG images.
* **Default width** - The default width of images in pixels that will be used in the design dialog

>[!TIP]
>
>See the document [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md) for tips for optimizing rendition selection by carefully defining your widths.

### Styles Tab {#styles-tab}

The Email Image Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
