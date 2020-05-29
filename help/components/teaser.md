---
title: Teaser Component
description: The teaser component can show an image, a title, rich-text, and optionally link to further content.
---

# Teaser Component {#teaser-component}

The Core Component Teaser Component can show an image, a title, rich-text, and optionally link to further content.

## Usage {#usage}

The Teaser Component allows the content author to easily create a teaser to further content using an image, title, or rich text and linking to further content or other actions.

The template author can use the [design dialog](#design-dialog) to define if the options to create call-to-actions and add links are available as well as disabling various display options. The content author can use the [configure dialog](#configure-dialog) to set an image, define CTAs, set titles and descriptions, and configure links to the individual teaser. The [edit dialog](image.md#edit-dialog) of the [Image Component](image.md) can be accessed to modify the teaser image.

## Version and Compatibility {#version-and-compatibility}

The current version of the Teaser Component is v1, which was introduced with release 2.1.0 of the Core Components in July 2018, and is described in this document.  
  
The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

| Component Version |AEM 6.4 |AEM 6.5 |AEM as a Cloud Service|
|---|---|---|---|
| v1 |Compatible |Compatible | Compatible|

## Sample Component Output {#sample-component-output}

To experience the Teaser Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_teaser).

### Technical Details {#technical-details}

The latest technical documentation about the Teaser Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The content author can use the configure dialog to define the properties of the individual teaser. There is also an [edit dialog](#edit-dialog) to modify the teaser image if one is selected.

### Image {#image}

![Teaser Component's edit dialog image tab](/help/assets/teaser-edit-image.png)

* **Image asset**
  * Drop an asset from the [asset browser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) or tap the **browse** option to upload from a local file system.
  * Tap or click **Clear** to de-select the currently selected image.
  * Tap or click **Edit** to [mange the renditions of the asset](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in the asset editor.

### Text {#text}

![Teaser Component's edit dialog text tab](/help/assets/teaser-edit-text.png)

* **Pretitle** - The pretitle will be displayed before the teaser's title.
* **Title** - Defines a title to display as the headline for the teaser.
  * **Get title from linked page** -  When checked, the title will be populated with the linked page's title.
* **Description** - Defines a description to display as the subheading of the teaser.
  * **Get description from linked page** - When checked, the description will be populated with the linked page's description.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

### Links & Actions {#links-actions}

![Teaser Component's edit dialog link tab](/help/assets/teaser-edit-link.png)

* **Link** - Link applied to the teaser. Use the path browser to select the link target.
* **Enable Call-To-Actions** -  When checked, enables definition of Call-To-Actions. The first Call-To-Action link in the list is used as the link for other teaser elements.

## Edit Dialog {#edit-dialog}

The Teaser Component delegates image rendering to the [Image Component](image.md). Therefore the [edit dialog](image.md#edit-dialog of the Image Component is available to the content author to manipulate the teaser image.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the teaser options that the content author has when using this component.

### Teaser Tab {#teaser-tab}

![Teaser Component's design dialog](/help/assets/teaser-design.png)

* **Call-To-Actions**
  * **Disable Call-To-Actions** - Hide the **Call-To-Actions** option for content authors
* **Elements**
  * **Hide pretitle** - Hides the **Pretitle** option for content authors
  * **Hide title** - Hides the **Title** option for content authors
    * When selected the **Title Type** is hidden
  * **Hide description** - Hide the **Description** option for content authors
* **Title Type** - Defines the H tag to be used by the title of the teaser.  
* **Links**
  * **Don't link the image** -  When selected, the teaser image is not linked  
  * **Don't link the title** -  When selected, the teaser title is not linked
* **Image Delegate** - Informational display indicating to which component the Teaser delegates image handling.

### Styles Tab {#styles-tab}

The Teaser Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
