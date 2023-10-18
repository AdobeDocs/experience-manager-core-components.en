---
title: Adaptive Form Accordion
description: Use accordion to organize and simplify a long or complex form by breaking it into smaller, more manageable sections.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
---
# Accordion Component {#accordion-component-adaptive-forms-core-component}

Accordion Core Component allows users to create expandable and collapsible sections in an Adaptive Form. It is often used to organize and simplify long or complex forms by breaking them up into smaller, more manageable sections. Each section of an accordion is typically represented by a header, which the user can click to expand or collapse the corresponding content. The content can be any Core Component. 

## Usage {#usage}

There are several reasons why it is beneficial to include an accordion in an Adaptive Form, including:

* **Space saving**: An accordion allows users to expand and collapse sections of a form, reducing the amount of space needed to display all the form fields at once.

* **Navigation**: An accordion can be used to create a hierarchical navigation structure, making it easier for users to find the form fields they need.

* **User experience**: Accordion can be used to make the form more user-friendly by providing a clear and intuitive way for users to access and fill in form fields.

* **Long Forms**: Accordion is an ideal component to handle long forms, as it allows users to focus on one section at a time, rather than trying to process a lot of information all at once.

You can use:

* The [configure dialog](#configure-dialog) to specify properties of the accordion component. 

* The [Select panel popover](#select-panel-popover)  to define the order of the panels of the accordion. This allows the author to arrange the panels in the order the panels should appear.

* Options for a forms author to enable or disable certain features in the [design dialog](#design-dialog). For example, an author may choose to disable certain fields or sections of a form. These options allow the author to have greater control over the form's design and functionality, making it easier to create forms that are tailored to the specific needs of the organization.

The configure dialog, and select panel popover and the design dialog are all part of the core components that are built to make the authoring of the forms easy and provide an efficient way to create complex forms.

## Version and Compatibility {#version-and-compatibility}


The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|||
|---|---|
|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Accordion Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your accordion experience for visitors with the Configure Dialog. You can also define accordion items, panels, behavior, and appearance with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic tab](/help/adaptive-forms/assets/acc-basic.png)

* **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

* **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

* **Hide Title** - Select the option to hide the component's Title.

* **Group child components' data on form submission(Wrap data in object)** - When the option is selected, the data from its child components is nested within the parent component's JSON object. However, if the option is not selected, the submitted JSON data has a flat structure, with no object for the parent component. For example: 

    * When the option is selected, the data from the child components (for example, Street, City, and Zip Code) is nested within the parent component (Address) as a JSON object. This creates a hierarchical structure, and the data is organized under the parent component.
    
        Structure of submitted data:

         ```JSON 
    
         { "Address":

         { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }

         }
    
         ```

    * When the option is not selected, the submitted JSON data has a flat structure with no object for the parent component (Address). All data is at the same level, without any hierarchical organization.

        
        Structure of submitted data:

         ```JSON 
    
            { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
    
         ```

* **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row. 

* **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

* **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

* **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Repeat Accordion {#repeat-accordion}

![repeat-accordion](/help/adaptive-forms/assets/repeat-accordion.png)

You can use the repeatibility options to duplicate accordion panels and its child components, define a minimum and maximum repetition count, and facilitates the replication of similar sections within a form. When interacting with the accordion component and accessing its settings, the following options are presented:

* **Make accordion repeatable**: A toggle feature that allows users to enable or disable the repeatability functionality.
* **Minimum repetitions**: Establishes the minimum number of times the accordion panel can be repeated. A value of zero indicates that the accordion panel is not repeated; the default value is zero.
* **Maximum repetitions**: Sets the maximum number of times the accordion panel can be repeated. By default, this value is unlimited.

To effectively manage repeatable sections within the accordion, follow the steps provided in the [Creating forms with repeatable sections](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) article.

### Items Tab {#items-tab}

![Items tab](/help/adaptive-forms/assets/acc-items.png)

The Add button allows you to select a component to add as a panel from the component selection window. After adding the component, you can see the following options:

* **Icon** - The icon identifies the component of the panel in the list. You can hover mouse over the icon to see the full component name as a tooltip.
* **Description** - The description used as the text of the panel. By default, the name of the component is selected for the panel.
* **Delete** - Tap or click to delete the panel from the accordion component.
* **Rearrange** - Tap or click and drag to rearrange the order of the panels.

### Help Content Tab {#help-content}

![Help Content tab](/help/adaptive-forms/assets/acc-helpcontent.png)

* **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

* **Always show short description** - Enable the option to display the Short description below the component.

* **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility}

![Accessibility tab](/help/adaptive-forms/assets/acc-accessisbilty.png)

On the **Accessibility** tab, values are set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component. Various options are available for using the text for screen reader:

* **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 


    * **Custom text**: Select this option to use the custom text for ARIA accessibility labels. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
    * **Description**: Select this option to use the description for ARIA accessibility labels.
    * **Title**: Select this option to use the title for ARIA accessibility labels.
    * **Name**: Select this option to use the name for ARIA accessibility labels.
    * **None**: Select this option if you do not want to add for ARIA accessibility labels.

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

The Design Dialog lets template creators control how things are displayed by default. For the Adaptive Forms Accordion component, you can set the following:

* The type of HTML heading elements that are allowed and set as the default (such as H1, H2, H3, etc.)
* The core components that a form creator can add to the accordion in the Adaptive Forms editor
* Simple names for styles (CSS classes) which can be applied in the properties dialog  of accordion component in the Adaptive Forms editor.

This helps make the process of creating and customizing forms more straightforward and efficient.

### Properties Tab {#properties-tab-design}

The Properties Tab allows template authors to set default and allowed HTML heading elements for form authors: 

![Design dialog properties tab](/help/assets/accordion-design-properties.png)

* **Allowed Heading Elements**: A drop-down list with multiple options that lets the template author choose which headings elements can form author can use for accordion.

* **Default Heading Element**: A drop-down list sets the default Heading element for accordion component.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab allows template editor to set the components that can be added as items to the panels in the Accordion component in the Adaptive Forms editor.

### Styles Tab {#styles-tab}

The Design Dialog is used to define and manage CSS styles for a component. The Adaptive Forms Accordion Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

**Default CSS Classes**: You can provide a default CSS class for the accordion component. 

**Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.


<!--- 

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


<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

-->


>[!MORELIKETHIS]
>
>* [Button](/help/adaptive-forms/components/button.md)
>* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
>* [Date Picker](/help/adaptive-forms/components/date-picker.md)
>* [Drop-down list](/help/adaptive-forms/components/drop-down.md)
>* [Email-input](/help/adaptive-forms/components/email-input.md)
>* [Form Container](/help/adaptive-forms/components/form-container.md)
>* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
>* [Footer](/help/adaptive-forms/components/footer.md)
>* [Header](/help/adaptive-forms/components/header.md)
>* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Image](/help/adaptive-forms/components/image.md)
>* [Number Input](/help/adaptive-forms/components/number-input.md)
>* [Panel Container](/help/adaptive-forms/components/panel-container.md)
>* [Radio Button](/help/adaptive-forms/components/radio-button.md)
>* [Reset Button](/help/adaptive-forms/components/reset-button.md)
>* [Submit Button](/help/adaptive-forms/components/submit-button.md)
>* [Telephone input](/help/adaptive-forms/components/telephone-input.md)
>* [Text Input](/help/adaptive-forms/components/text-input.md)
>* [Text](/help/adaptive-forms/components/text.md)
>* [Title](/help/adaptive-forms/components/title.md)
>* [Wizard](/help/adaptive-forms/components/wizard.md)

## See Also {#see-also}

{{see-also}}