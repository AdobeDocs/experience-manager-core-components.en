---
title: Email Teaser Component
description: The Email Teaser Component can show an image, a title, rich-text, and optionally link to further content.
role: Architect, Developer, Admin, User
---

# Email Teaser Component{#email-teaser-component}

The Email Teaser Component can show an image, a title, rich-text, and optionally link to further content.

## Usage {#usage}

The Email Teaser Component allows the content author to easily create a teaser to further content using an image, title, or rich text and linking to further content or other actions.

The template author can use the [design dialog](#design-dialog) to define if the options to create call-to-actions and add links are available as well as disabling various display options. The content author can use the [configure dialog](#configure-dialog) to set an image, define CTAs, set titles and descriptions, and configure links to the individual teaser. The [edit dialog](image.md#edit-dialog) of the [Email Image Component](image.md) can be accessed to modify the teaser image.

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Teaser Component is v1, which was introduced with release x of the Email Core Components in October 2022, and is described in this document.  
  
The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version |AEM 6.5 |AEM as a Cloud Service|
|---|---|---|
|v1 |Compatible | Compatible|

## Sample Component Output {#sample-component-output}

To experience the Email Teaser Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library.](https://adobe.com/go/aem_cmp_library_email_teaser)

### Technical Details {#technical-details}

The latest technical documentation about the Email Teaser Component [can be found on GitHub.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

Further details about developing Core Components can be found in the [Core Components developer documentation.](/help/developing/overview.md)

## Configure Dialog {#configure-dialog}

The content author can use the configure dialog to define the properties of the individual teaser. There is also an [edit dialog](#edit-dialog) to modify the teaser image if one is selected.

### Links Tab {#links-tab}

![Email Teaser Component's edit dialog links tab](/help/email/assets/email-teaser-edit-links.png)

The teaser title, description, and image can be inherited from the linked content, or from the content linked in the first call to action. If neither a link nor a call to action is specified, then the title, description, and image will be inherited from the current content.

* **Link** - This file links to content, external URL, or anchor.
  * Click the Campaign icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
* **Call-to-actions** - This option allows linking to multiple destinations.
  * The page linked in the first call-to-action is used when inheriting the teaser title, description, or image.
  * Click the Campaign icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.

### Text Tab {#text-tab}

![Email Teaser Component's edit dialog text tab](/help/email/assets/email-teaser-edit-text.png)

* **Pretitle** - The pretitle will be displayed before the teaser's title.
* **Title** - Defines a title to display as the headline for the teaser.
  * Click the Campaign icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
  * **Get title from linked page** -  When checked, the title will be populated with the linked page's title.
* **Description** - Defines a description to display as the subheading of the teaser.
  * Click the **Select Adobe Campaign Variable** icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
  * **Get description from linked page** - When checked, the description will be populated with the linked page's description.
* **ID** - This option allows to control the unique identifier of the component in the HTML.
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting content.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS.

### Asset Tab {#asset-tab}

![Email Teaser Component's edit dialog image tab](/help/email/assets/email-teaser-edit-image.png)

* **Inherit featured image from page** - Use the image defined in the page properties of the linked page or the current page if none is found.
* **Image asset** - Drop an asset from the [asset browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) or tap the **browse** option to upload from a local file system.
  * Tap or click **Clear** to de-select the currently selected image.
  * Tap or click **Edit** to [mange the renditions of the asset](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in the asset editor.
* **Alternative text for accessibility** - This field allows you to define a description of the image for visually impaired users.
  * **Inherit alternative text from page** - This option uses the alternative description of the linked asset value of the `dc:description` metadata in DAM or of the current page if no asset is linked.
* **Don't provide an alternative text** - This option marks the image to be ignored by assistive technologies like screen readers for cases where the image is purely decorative or otherwise conveys no additional information to the page.

>[!NOTE]
>
>[Dynamic Media features](image.md#dynamic-media) are not currently available in the Teaser Component.

### Styles Tab {#styles-tab-edit}

The Email Teaser Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the tab to be available.

## Edit Dialog {#edit-dialog}

The Email Teaser Component delegates image rendering to the [Image Component](image.md). Therefore the [edit dialog](image.md#edit-dialog) of the Image Component is available to the content author to manipulate the teaser image.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the teaser options that the content author has when using this component.

### Teaser Tab {#teaser-tab}

![Email Teaser Component's design dialog](/help/email/assets/email-teaser-design.png)

* **Allowed Heading Elements** - Use the drop-down to define which heading HTML elements that are allowed to be selected by an author for the teaser's title type.
* **Default Heading Element of the Title** - The default heading HTML element used for the teaser's title type
* **Call-To-Actions**
  * **Disable Call-To-Actions** - Hide the **Call-To-Actions** option for content authors
* **Elements**
  * **Hide pretitle** - Hides the **Pretitle** option for content authors
  * **Hide title** - Hides the **Title** option for content authors
    * When selected the **Title Type** is hidden
  * **Show title type**
  * **Hide description** - Hide the **Description** option for content authors
* **Image Delegate** - Informational display indicating to which component the Email Teaser delegates image handling.

### Styles Tab {#styles-tab}

The Email Teaser Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)
