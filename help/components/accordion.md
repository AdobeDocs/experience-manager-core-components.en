---
title: Accordion Component
description: The Core Component Accordion component allows for the creation of a collection of panels arranged in an accordion on a page.
role: Architect, Developer, Administrator, Business Practitioner
---

# Accordion Component{#accordion-component}

The Core Component Accordion component allows for the creation of a collection of panels arranged in an accordion on a page.

## Usage {#usage}

The Core Component Accordion component allows for the creation of a collection of components, composed as panels, and arranged in an accordion on a page, similar to the [Tabs Component](tabs.md), but allows for expanding and collapsing of the panels.

* The accordion's properties can be defined in the [configure dialog](#configure-dialog).
* The order of the panels of the accordion can be defined in the configure dialog as well as the [select panel popover](#select-panel-popover).
* Defaults for the Accordion Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Deep Linking to a Panel {#deep-linking}

The Accordion and [Tabs Components](tabs.md) support linking directly to a panel within the component.

To do this:

1. View the page with the component using the **[View as Published](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** option in the page editor.
1. Inspect the content of the page and identify the ID of the panel.
   * For example `id="accordion-86196c94d3-item-ca319dbb0b"`
1. The ID becomes the anchor you can append to the URL using a hash (`#`).
   * For example `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Navigating to the URL with the panel ID as anchor, the browser will scroll directly to the particular component and display the specified panel. If the panel is configured to not be expanded by default, it will be expanded automatically.

## Version and Compatibility {#version-and-compatibility}

The current version of the Accordion Component is v1, which was introduced with release 2.5.0 of the Core Components in June 2019, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion).

## Technical Details {#technical-details}

The latest technical documentation about the Accordion Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the accordion item, its panels, and how it will behave and appear for a visitor to the page.

### Items Tab {#items-tab}

![Items tab of edit dialog of Accordion Component](/help/assets/accordion-edit-items.png)

Use the **Add** button to open the component selector to choose which component to add as a panel. Once added, an entry is added to the list, which contains the following columns:

* **Icon** - The icon of the component type of the panel for easy identification in the list. Mouse over to see the full component name as a tooltip.
* **Description** - The description used as the text of the panel, defaulting to the name of the component selected for the panel.
* **Delete** - Tap or click to delete the panel from the accordion component.
* **Rearrange** - Tap or click and drag to rearrange the order of the panels.

>[!TIP]
>
>If the viewport of the page is reduced so that the edit dialog becomes full screen, the **Add** button will be hidden. Components can still be added to the Accordion Component by [dragging from the components browser and dropping on the Accordion Component in the page editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Accordion Component](/help/assets/accordion-edit-properties.png)

* **Single item expansion** - When selected, this option forces a single accordion item to be expanded at a time. Expanding one item will then collapse all others.
* **Expanded items** - This option defines the items that are expanded by default when the page is loaded.
  * When **Single item expansion** is selected, one panel must be selected. By default the first panel is selected.
  * When **Single item expansion** is not selected, this option is a multi-select and is optional.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Select Panel Popover {#select-panel-popover}

The content author can use the **Select Panel** option on the component toolbar to change to a different panel for editing as well as to easily rearrange the order of the panels within the accordion.

![Select panel icon](/help/assets/select-panel-icon.png)

Once selecting the **Select Panel** option in the component toolbar, the configured accordion panels are displayed as a drop-down.

![Select panel popover](/help/assets/select-panel-popover.png)

* The list is ordered by the assigned arrangement of the panels and is reflected in the numbering.
* The component type of the panel is displayed first, followed by the description of the panel in lighter font.
* Tapping or clicking an entry in the dropdown, switches the view in the editor to that panel.
* The panels can be rearranged in-place by using the drag handles.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Accordion Component and the defaults set when placing the Accordion Component.

### Properties Tab {#properties-tab-design}

![Design dialog properties tab](/help/assets/accordion-design-properties.png)

* **Allowed Heading Elements** - This multi-select drop-down defines the accordion item heading HTML elements that are allowed to be selected by an author.
* **Default Heading Element** - This drop-down defines the default accordion item heading HTML element.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Styles Tab {#styles-tab}

The Accordion Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Accordion Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
