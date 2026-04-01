---
title: Download Component
description: The Core Component Download component allows for the creation of a download option on a page.
role: Developer, Admin, User
exl-id: 48e7ade0-b849-4d1f-b836-51196e5ac507
TQID: https://experienceleague.adobe.com/76bcM5gBp5F-6Va3ChbowPwmDZ-icOkn0biazWgmCbs
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Download Component{#download-component}

The Core Component Download component allows for the creation of a download option on a page.

{{traditional-aem}}

## Usage {#usage}

The Core Component Download component allows for the inclusion of a download option and its associated asset on a page.

* The download option's properties can be selected in the [configure dialog](#configure-dialog).
* Defaults for the download component can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

The current version of the Download Component is v2, which was introduced with release 2.18.0 of the Core Components in February 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|--- |--- |---|---|---|
|v2|-|Compatible|Compatible|Compatible|
|[v1](v1/download.md)|Compatible|Compatible|-|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Download Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_download).

## Technical Details {#technical-details}

The latest technical documentation about the Download Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_download_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the download item and how it will behave and appear for a visitor to the page.

![Asset tab of the Download Component's edit dialog](/help/assets/download-edit-asset.png)

### Asset Tab {#asset-tab}

The selection of a download asset is very similar to the functionality of the [Image Component](image.md) and likewise leverages AEM's DAM.

* **Download Asset**
  * Drop an asset from the [asset browser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) or tap the **browse** option to upload from a local file system.
  * Tap or click **Clear** to de-select the currently selected image.
  * Tap or click **Edit** to [mange the renditions of the asset](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in the asset editor.

### Properties Tab {#properties-tab}

![Properties tab of the Download Component's edit dialog](/help/assets/download-edit-properties.png)

* **Title** - Displays as a headline for the download item
  * **Get title from DAM asset** - When selected, the title is automatically populated with the DAM asset's title.
* **Description** - Displays as a descriptive subheadline of the download item
  * **Get description from DAM asset** - When selected, the description is automatically populated with the DAM asset's description.
* **Action Text** - Displays as action text for the download item
  * This field is required when uploading an asset from the file system.
  * **Display inline** - When selected the provided **Action Text** will display inline.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

### Styles Tab {#styles-tab-edit}

![Styles tab of the edit dialog of Download Component](/help/assets/download-edit-styles.png)

The Download Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling).

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the drop down menu to be available.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Download Component.

### Properties Tab {#properties-tab-design}

![Design dialog of the Download Component](/help/assets/download-design.png)

* **Allow upload from file system** - Allows the content author to upload an asset from his/her local filesystem as the download asset.
  * The default value is unselected.
* **Title Type** - The HTML element used for the Download Component's title.
  * If no value is selected, the default value is H3.
* **Display File Size** - When selected the file size of the asset will be displayed in the download component.
  * The default value is selected.
* **Display File Format** - When selected the file format of the asset will be displayed in the download component.
  * The default value is selected.
* **Display Filename** - When selected the filename of the asset will be displayed in the download component.
  * The default value is selected.

### Styles Tab {#styles-tab}

The Image Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
