---
title: Container Component
description: The Core Component Container component allows for the creation of a container for multiple additional components on a page.
feature: Core Components
role: "Architect, Developer, Administrator, Business Practitioner"
---

# Container Component{#container-component}

The Core Component Container component allows for the creation of a container for multiple additional components on a page.

## Usage {#usage}

The Core Component Container component allows for the creation of a container for multiple additional components on a page and can be used to group other components and apply a common style or layout.

* The container's properties can be selected in the [configure dialog](#configure-dialog).
* Defaults for the Container Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

The current version of the Container Component is v1, which was introduced with release 2.5.0 of the Core Components in June 2019, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Container Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_container).

## Technical Details {#technical-details}

The latest technical documentation about the Container Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_container_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the container item and how it will behave and appear for a visitor to the page.

![Edit dialog of Container Component](/help/assets/container-edit.png)

* **Layout** - This option defines the behavior or the layout behavior of the Container Component.
  * **Simple** - Defines a container as a simple collection of components
  * **Responsive Grid** - Defines a container as an [AEM Responsive Layout](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)
* **Background Color** - Definable either as free-form RGB values or by using the color picker, [depending on configuration](#background-tab)
* **Background Image** - Defines a background color for the container,  [depending on configuration](#background-tab)
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Container Component.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to the Container Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Default Components Tab {#default-components-tab}

The Default Components tab is used to define which component is added to the component when a particular asset type is dropped on the container, similar to [how default components are defined on the page template](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Responsive Settings Tab {#responsive-settings-tab}

![Responsive settings tab of the design dialog of the Container Component](/help/assets/container-design-responsive.png)

* **Columns** - Defines the number of columns in the grid of the resulting container.

### Background Tab {#background-tab}

![Background tab of the design dialog of the Container Component](/help/assets/container-design-background.png)

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
  * **Rearrange** - Tap or click and drag to rearrange the order of the swatches.

### Styles Tab {#styles-tab}

The Container Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
