---
title: Adaptive Forms Core Component - Checkbox Group
description: Using or customizing the Adaptive Forms Checkbox Group Core Component.
role: Architect, Developer, Admin, User
exl-id: 2ced0223-e664-470b-a400-b6865d3a67c9
---
# Checkbox Group Component {#button-component-adaptive-forms-core-component}

<span class="preview"> This article contains content about the  **Allow Rich Text for Title**  and  **Allow Rich Text for Options**  features, pre-release features. The pre-release feature is accessible only through our [pre-release channel](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

A checkbox group in an Adaptive Form is a set of related checkboxes that allow users to select one or more options from a list. Each checkbox is represented by a Data Value (value used to process items of a checkbox group) and Display value (label for each checkbox item that describes its purpose)
**Example**

![checkbox group example](/help/adaptive-forms/assets/checkbox-group.png)

**Properties Dialog**

![checkbox group property dialog](/help/adaptive-forms/assets/checkbox-group-properties.png)

In this example, Options element is used to group the checkboxes together. The **Display text** element is used to provide a label for an item and **Data Value** is used to specify the value that is sent to the server when the form is submitted. 

Each checkbox option/item has a unique Data value and Display Text attribute. If a user selects the "Son" and "Daughter" checkboxes, the corresponding Data Value is sent to the server when the form is submitted. This data can then be processed by a server-side script to determine which options were selected by the user, and can be used to perform various actions, such as updating other fields in the form or submitting the form data to a server-side script for further processing.

Additionally, The checkbox group can be configured to have different processing values for each option, and this can be set by using Adaptive Forms Rule Editor.

## Usage {#reasons-to-use-check-box-group}

There are several reasons why it is beneficial to include a checkbox group in an Adaptive Form, including:

-   **Multiple selections**: A checkbox group allows users to select multiple options from a list, which can be useful in situations where multiple selections are allowed or required.

-   **User experience**: Checkbox group can be used to make the form more user-friendly by providing a clear and intuitive way for users to select multiple options.

-   **Data analysis**: Checkbox group can be used to collect data from various sources and analyze it, or use it as input for further processing.

-   **Surveys**: Checkbox group can be used in surveys to select multiple options for a question.

-   **User preferences**: Checkbox group can be used to collect user preferences for different options.

-   **Data Value**: Checkbox group can also be used to process items of a checkbox group.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Checkbox Group Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your checkbox experience for visitors with the Configure Dialog. You can also define checkbox options with ease for a seamless user experience.


### Basic Tab {#basic-tab}

![Basic tab](/help/adaptive-forms/assets/checkbox_basictab.png)

-   **Name** - The name uniquely identifies the component in the rule editor.Special characters and spaces are not allowed in the name strings.

-   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)

-   **Hide Title** - Select the option to hide the component's Title.

-   **Options** - You can add data values and display text pairs using the **Add** button.  
    After a new option is added, the following actions can be performed:
    - **Data Value** - This option allows to enter the content to submit when an option is selected.
    - **Display Text** - This option allows to enter the content to display in an Adaptive Form.
    - **Delete** - Tap or click to delete the option of a checkbox .
    - **Rearrange** - Tap or click and drag to rearrange the order of the panels. 
   
    You can also format the options for checkbox group using **Allow Rich Text for Options**. 
  
     ![Rich text support for options](/help/adaptive-forms/assets/richtext-for-options.png)

    Once you select the checkbox for **Allow Rich Text for Options** formatting options become visible to style the component's options. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     ![Rich text support for options](/help/adaptive-forms/assets/richtextoptions-support.png)

-   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.

-  **Data type of submitted value** - This option specifies the data type of the value sent when any option is selected. If the **data type of submitted value** is set to `Number` and you add string data to **Data Value** ​​on the **Options** tab, the screen displays a `Value type mismatch` error message.

-   **Display options** -  This option is used to set the visual alignment of checkboxes in an Adaptive Form. The two options supported are:
    - **Horizontal** - When this option is selected, checkboxes are displayed left to right in an Adaptive Form.
    - **Vertical** - When this option is selected, checkboxes are displayed top to bottom in an Adaptive Form.

-   **Default options** - This option allows you to add pre-selected default values when the form loads. Use the delete icon to remove the added options. If the **data type of submitted value** is set to `Number` and you add string data to **Default options**, the screen displays a `Value type mismatch` error message.
-   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
-   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/checkbox_validationtab.png)

-   **Required** - Select this option, if you want to display the component in an Adaptive Form. After selecting the option, you must make a selection before proceeding with a form submission. You cannot select the **Hide Component** or **Disable Component**  in the **Basic** tab when this option is selected.

-   **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.

-   **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

### Help Content Tab {#helpcontent-tab}

![Help Content tab](/help/adaptive-forms/assets/checkbox_helptab.png)

-   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

-   **Always show short description** - Enable the option to display the Short description below the component.

-   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/checkbox_accessibility.png)

**Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Check-box Group component.

### Styles Tab {#styles-tab}

The Adaptive Forms Checkbox Group Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/checkbox-style.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Checkbox Group Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties 

![Custom Properties Dialog](/help/adaptive-forms/assets/checkbox-customproperties.png)

Custom properties allows you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.

- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the order of the custom property name and custom property value.

## Related Articles {#related-articles}

{{more-like-this}})

## See Also {#see-also}

{{see-also}}
