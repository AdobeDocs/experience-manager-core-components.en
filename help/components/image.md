---
title: Image Component
description: The Core Component Image Component is an adaptive image component.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
---

# Image Component {#image-component}

The Core Component Image Component is an adaptive image component.

## Usage {#usage}

The Image Component features adaptive image selection and responsive behavior with lazy loading for the page visitor and easy image placement for the content author.

The content author can use the [edit dialog](#edit-dialog) to edit the image asset such as applying a crop or rotating the image.

The image widths and additional settings can be defined by the template author in the [design dialog](#design-dialog). The content editor can upload or select assets in the [configure dialog.](#configure-dialog)

## Version and Compatibility {#version-and-compatibility}

The current version of the Image Component is v3, which was introduced with release 2.18.0 of the Core Components in February 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component are compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|--- |--- |--- |---|---|
|v3|-|Compatible|Compatible|Compatible|
|[v2](v2/image.md)|Compatible|Compatible|-|Compatible|
|[v1](v1/image-v1.md )|Compatible|Compatible|-|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Responsive Features {#responsive-features}

The Image Component comes with robust responsive features ready right out of the box. At the page template level, the [design dialog](#design-dialog) can be used to define the default widths of the image asset. The Image Component automatically loads the correct width to display depending on the size of the browser window. As the window is resized, the Image Component dynamically loads the correct image size on the fly. There is no need for component developers to worry about defining custom media queries since the Image Component is already optimized to load your content.

In addition, the Image Component supports lazy loading to defer loading of the actual image asset until it is visible in the browser, increasing the responsiveness of your pages.

>[!TIP]
>
>By default, the Image Component is powered by the Adaptive Image Servlet. See [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md) for details on how it works.

### Differences with v2 {#v2-differences}

Unlike version 2 of the Image Component, version 3 uses browser-native responsiveness. This means that it provides the browser with a set of sources for an image for different widths and the browser will pick the best.

Most of the time, browsers prefer to locally downsize a larger width to fit a smaller viewport instead of fetching the smaller width image from the server. This is expected and why the Image Component should not be used for art direction (different images/crops for different viewports).

[Please see the technical documentation of the Image Component](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/image/v3/image#javascript-data-attribute-bindings) for more information.

## Dynamic Media Support {#dynamic-media}

The Image Component (as of [release 2.13.0](/help/versions.md)) supports [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html) assets. [When enabled,](#design-dialog) these features offer the ability to add Dynamic Media image assets with a simple drag-and-drop or via the assets browser just as you would any other image. In addition, image modifiers, image presets, and smart crops are also supported.

Your web experiences built with Core Components can feature rich, Sensei-powered, robust, high-performance, cross-platform Dynamic Media Image capabilities.

## Remote Assets Support {#remote-assets}

The Image Component (as of [release 2.23.2](/help/versions.md)) supports remote assets. [Once configured,](/help/developing/remote-assets.md) you can select assets from a remote service for your image component.

## SVG Support {#svg-support}

Scalable Vector Graphics (SVG) are supported by the Image Component.

* Drag-and-drop of an SVG asset from DAM and upload of an SVG file uploaded from a local file system are both supported.
* The original SVG file is streamed (transformations are skipped).
* For an SVG image, the "smart images" and the "smart sizes" are set to an empty array in the image model.

### Security {#security}

For security reasons, the original SVG is never called directly by the Image Editor. It is called through `<img src="path-to-component">`. This prevents the browser from executing any scripts embedded in the SVG file.

## Sample Component Output {#sample-component-output}

To experience the Image Component and see examples of its configuration options and HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_image).

### Technical Details {#technical-details}

The latest technical documentation about the Image Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_image_v3).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

The Image Component supports [schema.org microdata](https://schema.org).

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to crop and zoom the image.

Depending on if you have the [Dynamic Media](#dynamic-media) enabled or [Remote Assets Support](#remote-assets) is enabled, the options available for editing images differ.

### Standard Asset Editing {#standard-assets}

If you are editing standard AEM assets, you can click the **Edit** icon in the context menu of the image component.

![Image Component's edit dialog](/help/assets/image-edit.png)

* Start Crop

  ![Start crop icon](/help/assets/image-start-crop.png)

  Selecting this option opens a drop-down for pre-defined crop proportions.

  * Choose the option **Remove Crop** to display the original asset.

  Once a crop option is selected, use the blue handles to size the crop on the image.

  ![Crop options](/help/assets/image-crop-options.png)

* Rotate Right

  ![Rotate right icon](/help/assets/image-rotate-right.png)

  Use this option to rotate the image 90° to the right (clockwise).

* Reset Zoom

  ![Reset zoom icon](/help/assets/image-reset-zoom.png)

  If the image has already been zoomed, use this option to reset the zoom level.

* Open Zoom Slider

  ![Open zoom slider icon](/help/assets/image-zoom.png)

  Use this option to display a slider to control the zoom level of the image.

  ![Zoom slider control](/help/assets/image-zoom-slider.png)

The in-place editor can also be used to modify the image. Due to space limitations, only basic options are available in-line. For full edit options, use the full-screen mode.

![Image in-place edit options](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Image edit operations are not supported for GIF images. Any such changes made in edit mode to GIFs is not persisted.

### Dynamic Media Asset Editing {#dynamic-media-assets}

If you have [Dynamic Media features enabled,](#dynamic-media) editing of the image itself must be performed in the assets console.

## Configure Dialog {#configure-dialog}

The image component offers a configure dialog where the image itself is defined along with its description and basic properties.

### Asset Tab {#asset-tab}

![Asset tab of the Image Component's configure dialog](/help/assets/image-configure-asset.png)

* **Inherit featured image from page** - This option uses the [featured image of the linked page](page.md) or the featured image of the current page if the image is not linked.

* **Image asset** - This is automatically populated if **Inherit featured image from page** is selected. Deselect to manually define the image by setting the following options.

  * Drop an asset from the [asset browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html) or tap the **browse** option so you can upload from a local file system.
  * Tap or click **Clear** to de-select the currently selected image.
  * Tap or click **Pick** to open the [asset browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html) so you can select an image.
    * If [Remote Asserts Support](#remote-assets) is enabled, you have multiple options for picking an asset:
      * **Local** selects from the local AEM asset library.
      * **Remote** selects from a Dynamic Media library outside of your AEM instance.
  * Tap or click **Edit** to [manage the renditions of the asset](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html) in the Asset Editor.

* **Alternative text for accessibility** - This field allows you to define a description of the image for visually impaired users.

  * **Inherit alternative text from page** - This option uses the alternative description of the linked asset value of the `dc:description` metadata in DAM or of the current page if no asset is linked. 
  
* **Don't provide an alternative text** - Marks the image to be ignored by assistive technologies like screen readers for cases where the image is purely decorative or otherwise convey no additional information to the page.

### Metadata Tab {#metadata-tab}

![Metadata tab of the Image Component's configure dialog](/help/assets/image-configure-metadata.png)

* **Preset Type** - This defines the types of image presets available, either **Image Preset** or **Smart Crop**, and is only available when [Dynamic Media features](#dynamic-meida) are enabled.
  * **Image Preset** -  When **Preset Type** of **Image Preset** is selected, the drop-down **Image Preset** is available, allowing selection from the available Dynamic Media presets. This is only available if presets are defined for the selected asset.
  * **Smart Crop** - When **Preset Type** of **Smart Crop** is selected, the drop-down **Rendition** is available, allowing selection from the available renditions of the selected asset. This is only available if renditions are defined for the selected asset.
  * **Image Modifiers** - Additional Dynamic Media image serving commands can be defined here separated by `&`, regardless of which **Preset Type** is selected.
* **Caption** - Additional information about the image, displayed below the image by default.
  * **Get caption from DAM** - When checked the image's caption text is populated with the value of the `dc:title` metadata in DAM.  
  * **Display caption as pop-up** - When checked, the caption is not displayed below the image, but as a pop-up displayed by some browsers when hovering over the image.
* **Link** - Link the image to another resource.
  * Use the selection dialog to link to another AEM resource.
  * If not linking to an AEM resource, enter the absolute URL. Non-solute URLs are interpreted as relative to AEM.
  * **Open link in new tab** - This option opens the link in a new browser window.
* **ID** - This option lets you control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS, and Data Layer tracking.

>[!TIP]
>
>**Smart Crop** and **Image Preset** are mutually exclusive options. If an author must use an image preset along with a Smart Crop rendition, the author must use the **Image Modifiers** to manually add presets.

### Styles Tab {#styles-tab-edit}

![Styles tab of the edit dialog of Image Component](/help/assets/image-configure-styles.png)

The Image Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) for the drop-down menu to be available.

## Design Dialog {#design-dialog}

### Main Tab {#main-tab}

![Image Component's design dialog main tab](/help/assets/image-design-main.png)

* **Enable DM features** - When checked, [Dynamic Media features](#dynamic-media) are available.
  * This option only appears when Dynamic Media is enabled in the environment.
* **Enable Web Optimized Images** - When checked, [the web-optimized image delivery service](/help/developing/web-optimized-image-delivery.md) delivers images in the WebP format, reducing image sizes on average by 25%.
  * This option is only available in AEMaaCS.
  * When unchecked, or the web-optimized image delivery service is unavailable, the [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md) is used.
* **Disable lazy loading** - When checked, the component preloads all images without lazy loading.  
* **Image is decorative** - Define if the decorative image option is automatically enabled when adding the image component to a page.
* **Get alternative text from DAM**-  Define if the option to retrieve the alternate text from the DAM is automatically enabled when adding the image component to a page.
* **Get caption from DAM** - Define if the option to retrieve the caption from the DAM is automatically enabled when adding the image component to a page.
* **Display caption as pop-up** - Define if the option to display the image caption as a pop-up is automatically enabled when adding the image component to a page.
* **Resize width** - This value is used for resizing the width of the base images that are DAM assets.
  * The aspect ratio of the images is preserved.
  * If the value is larger than the actual width of the image, this value has no effect.
  * This value has no effect on SVG images.

You can define a list of widths in pixels for the image, and the component automatically loads the most appropriate width based on browser size. This is an important part of the [responsive features](#responsive-features) of the Image Component.

* **Widths** - Defines a list of widths in pixels for the image and the component automatically loads the most appropriate width based on browser size.
  * Tap or click the **Add** button to add another size.
    * Use the grab handles to rearrange size order.
    * Use the **Delete** icon to remove a width.
  * By default images loading is deferred until they become visible.
    * Select the option **Disable lazy loading** so you can load the images upon page load.
* **JPEG Quality** - The quality factor (in percentage from 0 and 100) for transformed (for example, scaled or cropped) JPEG images.

>[!TIP]
>
>See the document [Adaptive Image Servlet](/help/developing/adaptive-image-servlet.md) for tips for optimizing rendition selection by carefully defining your widths.

### Styles Tab {#styles-tab}

The Image Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Image Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
