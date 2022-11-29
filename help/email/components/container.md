---
title: Email Container Component
description: The Email Container Component allows for the creation of a container for multiple additional components in your email content.
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
---

# Email Container Component {#email-container-component}

The Email Container Component allows for the creation of a container for multiple additional components in your email content.

## Usage {#usage}

The Email Container component allows for the creation of a container for multiple additional components in your email content and can be used to group other components and apply a common style or layout.

* The container's properties can be selected in the [configure dialog.](#configure-dialog)
* Defaults for the Email Container Component when adding it to a page can be defined in the [design dialog.](#design-dialog)

Once an Email Container component is added to a page, a content author can drag-and-drop additional components into it.

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Container Component is v1, which was introduced with release X of the Email Core Components in October 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM as a Cloud Service|
|---|---|---|
|v1|Compatible|Compatible|

For more information about Email Core Component versions and releases, see the document [Email Core Components Versions.](/help/email/versions.md)

## Sample Component Output {#sample-component-output}

To experience the Email Container Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library.](https://adobe.com/go/aem_cmp_library_email_container)

## Technical Details {#technical-details}

The latest technical documentation about the Container Component [can be found on GitHub.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

Further details about developing Core Components can be found in the [Core Components developer documentation.](/help/developing/overview.md)

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the container item and how it behaves and appears in your content.

![Edit dialog of Email Container Component](/help/email/assets/email-container-configure.png)

* **Layout** - This option defines the behavior or the layout behavior of the Email Container Component.
  * **full-width**
  * **half|half**
  * **one-third|two-third**
  * **two-third|one-third**
  * **third|third|third**
* **Background Color** - Definable either as free-form RGB values or by using the color picker, [depending on configuration](#container-settings-tab)
* **Background Image** - Defines a background image for the container, [depending on configuration](#container-settings-tab)
* **ID** - This option allows controlling the unique identifier of the component in the HTML.
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting content.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS.

### Styles Tab {#styles-tab-edit}

The Email Container Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the tab to be available.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Email Container Component.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to the Email Container Component by the content author.

The **Allowed Components** tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Default Components Tab {#default-components-tab}

The **Default Components** tab is used to define which component is added to the component when a particular asset type is dropped on the container, similar to [how default components are defined on the page template.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Container Settings Tab {#container-settings-tab}

The **Container Settings** tab defines if the author can define a background image or color.

![Container Settings tab of the design dialog of the Email Container Component](/help/email/assets/email-container-design-container-settings.png)

* **Background Image**
  * **Enable background image** - Select this option to enable the content author to define a background image for the container.
* **Background Color**
  * **Enable background color** - Select this option to enable the content author to define a background color for the container.
  * **Swatches only** - Select this option to only allow the content author to select from pre-defined color swatches for the container background color.
    * Only available when **Enable background color** is selected
* **Allowed Swatches** - Define pre-defined colors from which the content author can select the container background color
  * Use the **Add** button to add a pre-defined color swatch. Once added, an entry is added to the list, which contains the following columns:
  * **Value** - Define the color manually via RGB values
    * Tap or click the color picker to more easily select a color by adjusting individual RGB values or defining a hex value.
  * **Delete** - Tap or click to delete a swatch.
  * **Rearrange** - Tap or click and drag to reorder swatches.

### Styles Tab {#styles-tab}

The Email Container Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)
