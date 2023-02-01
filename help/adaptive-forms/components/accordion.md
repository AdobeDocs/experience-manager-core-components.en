---
title: Adaptive Forms Core Accordion
description: Use accordion to organize and simplify a long or complex form by breaking it into smaller, more manageable sections.
role: Architect, Developer, Admin, User

---
# Accordion Component {#accordion-component-adaptive-forms-core-component}

Accordion Core Component allows users to create expandable and collapsable sections in an Adaptive Form. It is often used to organize and simplify long or complex forms by breaking them up into smaller, more manageable sections. Each section of an accordion is typically represented by a header, which the user can click to expand or collapse the corresponding content. The content can be any Core Component. 

## Usage {#usage}

There are several reasons why it is beneficial to include an accordion in an Adaptive Form, including:

*   **Space saving**: An accordion allows users to expand and collapse sections of a form, reducing the amount of space needed to display all the form fields at once.

*   **Navigation**: An accordion can be used to create a hierarchical navigation structure, making it easier for users to find the form fields they need.

*   **Customization**: Accordion can be customized to suit the specific needs of the form, such as adding icons or changing the color of the accordion.

*   **Accessibility**: Accordion can be made accessible by providing a clear label, and making sure that the options are clearly visible and readable.

*   **User experience**: Accordion can be used to make the form more user-friendly by providing a clear and intuitive way for users to access and fill in form fields.

*   **Conditional logic**: Accordion can be used to show or hide other form fields based on the user selection

*   **Long Forms**: Accordion is an ideal component to handle long forms, as it allows users to focus on one section at a time, rather than trying to process a lot of information all at once.

*   **Rule based actions**: Accordion can also be used to trigger different rule based actions like submitting form, opening a website, show/hide components, add an instance of a panel or component to the button.

You can use:

*   The [configure dialog](#configure-dialog) to specify properties of the accordion component. 

*   The [Select panel popover](#select-panel-popover)  to define the order of the panels of the accordion. This allows the author to arrange the panels in the order the panels should appear.

*   Options for a forms author to enable or disable certain features in the [design dialog](#design-dialog). For example, an author may choose to disable certain fields or sections of a form. These options allow the author to have greater control over the form's design and functionality, making it easier to create forms that are tailored to the specific needs of the organization.

The configure dialog, and select panel popover and the design dialog are all part of the core components that are built to make the authoring of the forms easy and provide an efficient way to create complex forms.

## Version and Compatibility {#version-and-compatibility}


The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Accordion Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your accordion experience for visitors with the Configure Dialog. You can also define accordion items, panels, behavior, and appearance with ease for a seamless user experience.

### Basic Tab {#basic-tab}
![Basic tab](/help/adaptive-forms/assets/accordion_basictab.png)

* **Name** - The name is a short string that uniquely identifies a component type.

* **Title** - Title is a string that appears at the top of a component type in an Adaptive Form.

* **Hide Title** - When this option is selected,the title of a component type is not displayed.

* **Wrap data in a object** - This option specifies whether the content of a component type is automatically wrapped at the end of lines. 

* **Layout** - A layout is a menu style that displays collapsible headings on top of each other. Click a header to see related content. Different  layout formats are:
    * **Simple** - This menu style stacks headers vertically. 
    * **Responsive Grid** - This style of menu is responsive and adapts to the size of the device on which it is displayed.
* **Bind Reference** - This option allows you to get the accordion list items from the local schema.
* **Hide Component** - If you select this option, a component types is not displayed. You can also hide individual accordion list items.
* **Disable Component** - If you select this option, you cannot select a component type. You can also disable individual accordion list items. 

### Items Tab {#items-tab}

![Items tab](/help/adaptive-forms/assets/accordion_itemstab.png)

The Add button allows you to select a component to add as a panel from the component selection window. After adding the component, you can see the following options:
* **Icon** - The icon of the component type of the panel for easy identification in the list. Hover mouse over the icon to see the full component name as a tooltip.
* **Description** - The description used as the text of the panel, defaulting to the name of the component selected for the panel.
* **Delete** - Tap or click to delete the panel from the accordion component.
* **Rearrange** - Tap or click and drag to rearrange the order of the panels.

>[!NOTE]
>
>If the viewport of the page is reduced so that the edit dialog becomes full screen, the **Add** button is hidden. Components can still be added to the Accordion Component by [dragging from the components browser and dropping on the Accordion Component in the page editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Help Content {help-content}

![Help Content tab](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **Short Description** - The short description provides enough context to user to understand what the accordion menu conveys. You can also format the text that appears in the short description.

* **Always show short description** - Select this option to display a short description even if the user does not hover over a component type.

* **Help Text** - Help text consists of information or error messages about the component type. Help text is available by clicking the icon that appears above the component type. Click the icon to display help text above the component type in edit mode.You can also format the text that appears in the help text.

### Accessibility {#accessibility}

![Accessibility tab](/help/adaptive-forms/assets/accordion_accessibility.png)

Text for Screen Readers uses a Text-To-Speech (TTS) engine to convert information into speech. You can listen to information  through headphones or speakers. Various options are available for using the text for screen reader:
* **Custom text**: Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
* **Description**: Select this option to use the description as a audio text.
* **Title**: Select this option to use the title as a audio text.
* **Name**: Select this option to use the name as a audio text.
* **None**: Select this option if you do not want to add audio text.

<!--

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Accordion Component](/help/assets/accordion-edit-properties.png)

*   **Single item expansion** - When selected, this option forces a single accordion item to be expanded at a time. Expanding one item will then collapse all others.
*   **Expanded items** - This option defines the items that are expanded by default when the page is loaded.
    * When **Single item expansion** is selected, one panel must be selected. By default the first panel is selected.
    * When **Single item expansion** is not selected, this option is a multi-select and is optional.
*   **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
    * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
    * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Select Panel Popover {#select-panel-popover}

The **Select Panel** option (![Select panel icon](/help/assets/select-panel-icon.png)) on the component toolbar enables content authors to modify the panels in an accordion with ease. By selecting this option, the author can switch to a different panel for editing and rearrange the order of the panels in the accordion. The configured panels will be displayed in a drop-down menu for the author to choose from. This feature optimizes the editing process and makes it user-friendly for content authors.

![Select panel popover](/help/assets/select-panel-popover.png)


* The panels are displayed in a numbered list, reflecting the assigned arrangement.
* Each panel is listed with its component type in bold, followed by a brief description in lighter font.
* By clicking or tapping on a panel in the drop-down, you can easily switch the view in the editor to that specific panel.
* To rearrange the panels, simply use the drag handles to move them into the desired order. -->

## Design Dialog {#design-dialog} 

<!-- 

The design dialog allows the template author to define the options available to the content author who uses the Accordion Component and the defaults set when placing the Accordion Component.


### Properties Tab {#properties-tab-design}

![Design dialog properties tab](/help/assets/accordion-design-properties.png)

* **Allowed Heading Elements** - This multi-select drop-down defines the accordion item heading HTML elements that are allowed to be selected by an author.
* **Default Heading Element** - This drop-down defines the default accordion item heading HTML element.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Styles Tab {#styles-tab}

The Accordion Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Accordion Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)

-->




