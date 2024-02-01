---
title: Carousel Component
description: The Carousel Component allows the content author to present content in a rotating carousel.
role: Architect, Developer, Admin, User
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
---

# Carousel Component{#carousel-component}

The Core Component Carousel Component allows the content author to present content in a navigable carousel.

## Usage {#usage}

Using the Carousel Component, the content author to organize content in a rotating carousel of slides.

The [edit dialog](#edit-dialog) allows the content author to create, name, and order multiple slides as well as enable auto-transition with delay. Using the [design dialog](#design-dialog), the template author can define which components can be added to the carousel, enable or disable automatic transitions, and customize the styles.

## Version and Compatibility {#version-and-compatibility}

The current version of the Carousel Component is v1, which was introduced with release 2.2.0 of the Core Components in October 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v1|Compatible with<br>[release 2.17.4](/help/versions.md) and prior|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Carousel Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_carousel).

### Technical Details {#technical-details}

The latest technical documentation about the Carousel Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Deep Linking to a Panel {#deep-linking}

The Carousel, [Tabs,](tabs.md) and [Accordion Components](accordion.md) support linking directly to a panel within the component.

To do this:

1. View the page with the component using the **[View as Published](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** option in the page editor.
1. Inspect the content of the page and identify the ID of the panel.
   * For example `id="carousel-bfe4fa6647-item-47f1a7ca67-tabpanel"`
1. The ID becomes the anchor you can append to the URL using a hash (`#`).
   * For example `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#carousel-bfe4fa6647-item-47f1a7ca67-tabpanel`

Navigating to the URL with the panel ID as anchor, the browser will scroll directly to the particular component and display the specified panel. If the panel is configured not to be displayed by default, it will be scrolled to automatically.

## Carousel and Responsive Design {#responsive-design}

All Core Components are designed to be fully responsive, ensuring a seamless experience across devices.

Some some advanced components like the Carousel Component may require specific consideration within the context of the implementing project in order to maintain responsiveness in all conditions. Please see the document [Responsive Design of the Core Components](/help/responsive.md) for more information.

## Edit Dialog {#edit-dialog}

The edit dialog allows the content author to add, rename, and rearrange slides as well as define the auto-transition settings.

### Items Tab {#items-tab}

![Items tab of the edit dialog of the Carousel Component](/help/assets/carousel-edit-items.png)

Use the **Add** button to open the component selector to choose which component to add as a tab. Once added, an entry is added to the list, which contains the following columns:

* **Icon** - The icon of the component type of the tab for easy identification in the list. Mouse over to see the full component name as a tooltip.
* **Description** - The description used as the text of the tab, defaulting to the name of the component selected for the tab.
* **Delete** - Tap or click to delete the tab from the tabs component.
* **Reorder** - Tap or click and drag to order the tabs.

>[!TIP]
>
>If the viewport of the page is reduced so that the edit dialog becomes full screen, the **Add** button will be hidden. Components can still be added to the Carousel Component by [dragging from the components browser and dropping on the Carousel Component in the page editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser).

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Carousel Component](/help/assets/carousel-edit-properties.png)

On the **Properties** tab, the content author can set the slides to automatically transition.

* **Active Item** - The content author can define which tab is active when the page is loaded. 
* **Automatically transition slides** - When active, the component will automatically advance to the next slide after a specified delay.
* **Transition Delay** - When Automatically transition slides is selected, this value is used to define the delay between transitions (in milliseconds).
* **Disable automatic pause on hover** - When **Automatically transition slides** is selected, the carousel transition will automatically pause whenever the cursor hovers over the carousel. Select this option so that the transition will not pause.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

>[!NOTE]
>
>The slide advance controls are not enabled when in **Edit** mode. Use [**Preview** mode](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) or the **[View as Published](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** option to interact with the carousel as a reader of the published content would.
>
>The auto-advance feature is not enabled when in **Edit** mode. Use **[View as Published](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** option to see the auto-advance feature as a reader of the published content would.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab of the edit dialog of the Carousel Component](/help/assets/carousel-edit-accessibility.png)

On the **Accessibility** tab, values can be set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component.

* **Label** - Value of an aria-label attribute for the carousel, which describes the carousel's content
* **Previous** - Value of an aria-label attribute for the carousel navigation's previous button label
* **Next** - Value of an aria-label attribute for the carousel navigation's next button label
* **Play** - Value of an aria-label attribute for the carousel navigation's play button label
* **Pause** - Value of an aria-label attribute for the carousel navigation's pause button label
* **Tablist** - Value of an aria-label attribute for the carousel navigation's list of items label
* **Set item's aria label to its title** - If checked, this option automatically sets the carousel items title to its aria-label description.

## Select Panel {#select-panel}

The content author can use the **Select Panel** option on the component toolbar to change to a different slide for editing as well as to easily rearrange the order of the slides.

![Select panel icon](/help/assets/select-panel-icon.png)

Once selecting the **Select Panel** option in the component toolbar, the configured slides are displayed as a drop-down.

* The list is ordered by the assigned arrangement of the slides and is reflected in the numbering.
* The component type of the slide is displayed first, followed by the description of the slide in lighter font.

![Select panel](/help/assets/select-panel-popover.png)

* Tapping or clicking an entry in the dropdown, switches the view in the editor to that slide.
* The slide can be reordered in-place by using the drag handles.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define which components can be added as slides to the carousel component as well as define auto-transition defaults and which custom styles are available to the content author.

### Properties Tab {#properties-tab-1}

The **Properties** tab is used to define the default settings for the slide transitions when a content author adds the carousel component to a page.

![Design dialog of the Carousel Component](/help/assets/carousel-design.png)

* **Automatically transition slides** - Defines if by default the option to automatically advance the carousel to the next slide is enabled when the content author adds the carousel component to a page.
* **Prepend control elements** - When checked, the control elements will be placed in front of the carousel items to improve accessibility.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as slides to the Carousel Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Styles Tab {#styles-tab}

The Carousel Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Carousel Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
