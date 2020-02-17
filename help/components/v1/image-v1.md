---
title: Image Component (v1)
description: The Core Component Image Component is an adaptive image component features in-place editing.
index: n
---

# Image Component (v1) {#image-component-v}

The Core Component Image Component is an adaptive image component features in-place editing.

## Usage {#usage}

The Image Component allows easy placement of image assets and offers in-place editing. It features adaptive image selection with lazy loading as well as cropping for the content author.

The allowed image widths as well as cropping and additional settings can be defined by the template author in the [design dialog](#design-dialog). The content editor can upload or select assets in the [configure dialog](#configure-dialog) and crop the image in the [edit dialog](#edit-dialog). For added convenience, simple in-place modification of the image is also available.

## Version and Compatibility {#version-and-compatibility}

This document describes v1 of the Image Component, originally introduced with release 1.0.0 of the Core Components with AEM 6.3.

The following table lists the compatibility of v1 of the Image Component.

|AEM Version|Image Component v1|
|--- |--- |
|6.3|Compatible|
|6.4|Compatible|

>[!CAUTION]
>
>This document describes v1 of the Image Component.
>
>For details of the current version of the Image Component, see the [Image Component](/help/components/image.md) document.

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-7.png) 

### HTML {#html}

```
<div class="cmp cmp-image aem-GridColumn aem-GridColumn--default--12">
 
        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/image.img.jpg" alt="Surfboard"/>
        </noscript>

</div>
```

### JSON {#json}

```
"image": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "smartSizes": [],
              "smartImages": [],
              "lazyEnabled": true,
              "src": "/content/we-retail/us/en/equipment/equipment/jcr%3acontent/root/responsivegrid/image.img.jpeg",
              ":type": "weretail/components/content/image"
            }
```

>[!NOTE]
>
>JSON export from the Core Components requires release 1.1.0 of the Core Components. Please see the [compatibility information for Core Components v1](versions.md#main-pars_title_236368006) for more information.

## Configure Dialog {#configure-dialog}

In addition to the standard [edit dialog](#edit-dialog) and [design dialog](#design-dialog), the image component offers a configure dialog where the image itself is defined along with its description and basic properties.

![](/help/assets/chlimage_1-50.png)

* **Image asset**
  * Drop an asset from the [asset browser](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) or tap the **browse** option to upload from a local file system.
  * Tap or click **Clear** to de-select the currently selected image.
  * Tap or click **Edit** to [mange the renditions of the asset](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) in the asset editor.

* **Image is decorative** - Check if the image should be ignored by assistive technology and therefore does not require an alternative text. This applies to decorative images only.
* **Alternative text** - Textual alternative of the meaning or function of the image, for visually impaired readers.
* **Link**
  * Link the image to another resource.
  * Use the selection dialog to link to another AEM resource.
  * If not linking to an AEM resource, enter the absolute URL. Non-solute URLs will be interpreted as relative to AEM.

* **Caption** -  Additional information about the image, displayed below the image be default.
* **Display caption as pop-up** -   When checked, the caption won't be displayed below the image, but as a pop-up displayed by some browsers when hovering over the image.

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to crop, modify the launch map, and zoom the image.

![](/help/assets/chlimage_1-8.png)

* Start Crop

  ![](/help/assets/chlimage_1-9.png)

  Selecting this option opens a drop-down for pre-defined crop proportions.

  * Choose the option **Free Hand** to define your own crop.
  * Choose the option **Remove Crop** to display the original asset.

  Once a crop option is selected, use the blue handles to size the crop on the image.

  ![](/help/assets/chlimage_1-10.png)

* Rotate Right

  ![](/help/assets/chlimage_1-11.png)

  Use this option to rotate the image 90° to the right (clockwise).

* Launch Map

  ![](/help/assets/chlimage_1-12.png)

  Use this option to apply a launch map to the image. Selecting this option opens a new window allowing the user select the shape of the map:

  * **Add Rectangular Map**
  * **Add Circular Map**
  * **Add Polygon Map**

    * By default adds a triangle map. Double-click on a line of the shape to add a new blue resize handle on a new side.

  Once a map shape is selected, it is superimposed on the image allowing for resizing. Drag and drop the blue resize handles to adjust the shape.

  ![](/help/assets/chlimage_1-13.png)

  After sizing the launch map, click on it to open a floating toolbar to define the path of the link.

  * **Path**
    * Use the Path Picker option to select a path in AEM
    * If the path is not in AEM, use the absolute URL. Non-absolute paths will be interpreted relative to AEM.

    * **Alt text**
      Alternative description of the path destination
    * **Target**
      * **Same tab**
      * **New tab**
      * **Parent Frame**
      * **Top Frame**

  Tap or click the blue check mark to save, the black x to cancel, and the red trash can to delete the map.

  ![](/help/assets/chlimage_1-14.png)

* Reset Zoom

  ![](/help/assets/chlimage_1-15.png)

  If the image has already been zoomed, use this option to reset the zoom level.

* Open Zoom Slider

  ![](/help/assets/chlimage_1-16.png)

  Use this option to display a slider to control the zoom level of the image.

  ![](/help/assets/chlimage_1-17.png)

The in-place editor can also be used to modify the image. Due to space limitations, only basic options are available in-line. For full edit options, use the full-screen mode.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>Image edit operations (crop, flip, rotate) are not supported for GIF images. Any such changes made in edit mode to GIFs will not be persisted.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the cropping, upload, and rotation uploads the content author has when using this component.

### Main {#main}

On the **Main** tab you can define a list of allowed widths in pixels for the image to automatically load the most appropriate width from the list.

![](/help/assets/chlimage_1-51.png)

Tap or click the Add button to add another size.

* Use the grab handles to re-arrange the order of the sizes.
* Use the delete icon to remove a width.

By default images loading is deferred until they become visible. Select the option **Disable lazy loading** to load the images upon page load.

### Features {#features}

On the **Features** tab you can define which options are available to the content authors when using the component including upload options, orientation, and cropping options.

* Source

  ![](/help/assets/chlimage_1-19.png)

  Select the option **Allow asset upload from file system** to allow content authors to upload images from his or her local computer. To force content authors to only select assets from AEM, de-select this option.

* Orientation

  ![](/help/assets/chlimage_1-20.png)

  * **Rotate** - Use this option to allow the content author to use the **Rotate Right** option.
  * **Flip**
    Use this option to allow the content author to use the **Flip Horizontally** and **Flip Vertically** options.

  >[!CAUTION]
  >
  >The **Flip** option is disabled by default. Enabling it will display the **Flip Vertically** and **Flip Horizontally** buttons in the edit dialog of the image component, however the feature is not currently supported by AEM and any changes made using these options will not be persisted.

<!-- 
Comment Type: remark
Last Modified By: Chris Bohnert (bohnert)
Last Modified Date: 2017-11-20T05:51:34.378-0500

<p>Added caution based on CQDOC-11457. Hid the flip options in the procedure using the <strong>Draft</strong> option so that when this feature is implemented in CQ-4221539, the <strong>Draft</strong> property can simply be removed along with the caution.</p>
-->

* Cropping

  ![](/help/assets/chlimage_1-21.png)

  Select the option **Allow crop** to allow the content author to crop the image in the component in the edit dialog.
  * Click **Add** to add a pre-defined crop aspect ratio.
  * Enter a descriptive name, which will be shown in the **Start Crop** dropdown.
  * Enter the numerical ratio of the aspect.
  * Use the drag handles to re-arrange the order of the aspect ratios
  * Use the trash can icon to delete an aspect ratio.

  >[!CAUTION]
  >
  >Note that in AEM, crop aspect ratios are defined as **height/width**. This differs from the conventional definition of width/height and is done for legacy compatibility reasons. The content authors will not be aware of any difference as long as you provide a clear name of the ratio since the name is shown in the UI and not the ratio itself.

## Technical Details {#technical-details}

The latest technical documentation about the Image Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).
