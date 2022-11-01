---
title: Email Segmentation Component
description: The Email Segmentation component
role: Architect, Developer, Admin, User
hidefromtoc: yes
index: no
---

# Email Segmentation Component {#email-segmentation-component}

The Email Segmentation Component uses variables from Adobe Campaign to show and hide content based on the recipient of the content.

## Usage {#usage}

The Email Segmentation Component allows the content author to hide and show content based on conditions met by variables about the recipient provided by Adobe Campaign. In this way, the recipients of the content sees content based on their segmentation.

* The template author can use the [design dialog](#design-dialog) to define which components can be added as segment.
* The content author can use the [configure dialog](#configure-dialog) to add components as segments and configure which segments are shown based on Adobe Campaign variables.

As an alternative to using the configure dialog, once the content author has added the Email Segmentation Component to a content page, the content author can then drag-and-drop additional components onto the Email Segmentation Components to create new segments.

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Segmentation Component is v1, which was introduced with release x of the Email Core Components in October 2022, and is described in this document.  
  
The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version |AEM 6.5 |AEM as a Cloud Service|
|---|---|---|
|v1 |Compatible | Compatible|

## Sample Component Output {#sample-component-output}

To experience the Email Segmentation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library.](https://adobe.com/go/aem_cmp_library_email_segmentation)

### Technical Details {#technical-details}

The latest technical documentation about the Email Teaser Component [can be found on GitHub.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

Further details about developing Core Components can be found in the [Core Components developer documentation.](/help/developing/overview.md)

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to create, rename, and rearrange segments as well as define the active segment. In the Email Segmentation Component, a segment is simply another component that is hidden or shown based on conditions met by the recipient of the content. You can compare it to the [Core Components Tab Component,](/help/components/tabs.md) but in the Segmentation Component, only the content of the tab whose conditions are met are shown.

### Items Tab {#items-tab}

![Email Segmentation Component's configure dialog items tab](/help/email/assets/email-segmentation-configure-items.png)

Use the **Add Segment** button to open the component selector to choose which component to add as a segment. Once added, an entry is added to the list, which contains the following elements:

* **Icon** - The icon of the component type of the segment for easy identification in the list. Mouse over to see the full component name as a tooltip.
* **Condition** - The condition that must be met for this segment to be shown to the recipient of the content.
  * The conditions available are defined in the [design dialog.](#design-dialog)
  * **Default** - Defines the default segment to show if no other conditions are met
  * **Custom** - Allows the author to define a condition
    * The conditions are based on Adobe Campaign personalization variables
    * [See here for Adobe Campaign Standard personalization resources.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
    * [See here for Adobe Campaign Classic personalization resources.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html)
* **Delete** - Tap or click to delete the segment from the Email Segmentation Component.
* **Rearrange** - Tap or click and drag to rearrange the segments.

>[!TIP]
>
>If the viewport of the content is reduced so that the edit dialog becomes full screen, the **Add** button will be hidden. Components can still be added to the Email Segmentation Component by [dragging from the components browser and dropping on the Email Segmentation Component in the content editor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component)

### Properties Tab {#properties-tab}

![Email Segmentation Component's configure dialog properties tab](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - This option allows controlling the unique identifier of the component in the HTML.
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting content.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS.

### Accessibility Tab {#accessibility-tab}

![Email Segmentation Component's configure dialog accessibility tab](/help/email/assets/email-segmentation-configure-accessibility.png)

On the **Accessibility** tab, values can be set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component.

* **Label** - Value of an ARIA label attribute for the component

### Styles Tab {#styles-tab-edit}

The Email Segmentation Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)

Use the drop-down to select the styles that you want to apply to the component. Selections made in the edit dialog have the same effect as those chosen from the component toolbar.

Styles must be configured for this component in the [design dialog](#design-dialog) in order for the tab to be available.

## Select Panel {#select-panel}

The content author can use the **Select Panel** option on the component toolbar to change to a different segment for editing as well as to easily rearrange the segments.

![Select panel icon](/help/email/assets/select-panel-icon.png)

Once selecting the **Select Panel** option in the component toolbar, the configured segments are displayed as a drop-down.

* The list is ordered by the assigned arrangement of the segments and is reflected in the numbering.
* The component type of the segment is displayed first, followed by the description of the segment in lighter font.

![Select panel popover](/help/email/assets/select-panel-popover.png)

* Tapping or clicking an entry in the dropdown, switches the view in the editor to that segment.
* The segments can be rearranged in-place by using the drag handles.

>[!NOTE]
>
>Segments are rendered as tabs within the page editor to show that there are multiple options for the final content. These tabs are not selectable by the author within the page editor. Use the select panel to switch between displayed segments.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define which components can be added as segments to the Email Segmentation Component as well as define which custom styles are available to the content author.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as segments to the Email Segmentation Component by the content author.

The **Allowed Components** tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Styles Tab {#styles-tab}

The Email Segmentation Component supports the AEM [Style System.](/help/get-started/authoring.md#component-styling)

### Defined Conditions Tab {#defined-conditions}

Using the **Defined Conditions** tab, the template editor can define which conditions are available to the content author to select when creating segments.

![Design dialog Defined Conditions tab](/help/email/assets/email-segmentation-design-defined-conditions.png)

Tap or click the **Add** button to create new conditions.

* **Segment Condition Name** - A description of the condition
* **Segment Condition** - The actual condition that must be met, based on Adobe Campaign personalization variables
  * [See here for Adobe Campaign Standard personalization resources.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
  * [See here for Adobe Campaign Classic personalization resources.](https://experienceleague.adobe.com/docs/
* **Remove** - Tap to click to remove the condition
* **Rearrange** - Tap or click and drag to rearrange the order of the conditions
