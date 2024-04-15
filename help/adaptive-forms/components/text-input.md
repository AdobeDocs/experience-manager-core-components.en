---
title: Adaptive Forms Core Component - Text input (Text box)
description: Using or customizing the Adaptive Forms Text input Core Component.
role: Architect, Developer, Admin, User
exl-id: 49d9fe69-0578-4489-beaa-a18cdb14add7
---
# Text input (Text box) {#text-input-adaptive-forms-core-component}

<span class="preview"> This article contains content about the **Allow Rich Text for Title** feature, a pre-release feature. The pre-release feature is accessible only through our [pre-release channel](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

A text input (text box) component allows a user to enter and edit a single or multiple lines of text, depending on the type attribute of the input element. The text input component can be placed within a form and is usually labeled with a helpful text that easily identifies its purpose. These are a fundamental element of any form, widely used to collect different types of data from users, these are simple, flexible, and can be configured to validate inputs, improve accuracy of data collection.


**Example**

![example](/help/adaptive-forms/assets/text-input.png)


## Usage {#reasons-to-use-text-input-field}

There are several reasons to use Text input component in an Adaptive Form:

-   **Data collection**: Text input fields are one of the most common form elements used to collect a wide range of information from users, such as names, email addresses, phone numbers, and other types of text data.

-   **User-friendly**: Text input fields are simple and easy to use, making it easy for users to enter and edit text.

-   **Flexibility**: Text input fields can be used to collect a wide range of information, from short, single-line text entries to longer, multi-line text entries.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Tabs on Top Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your text input experience for visitors with the Configure Dialog. You can also define text input options with ease for a seamless user experience.

![Basic Tab](/help/adaptive-forms/assets/textinput_basictab.png)

-   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

-   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.
- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)
     
-   **Hide Title** - Select the option to hide the component's Title.

-   **Placeholder Text** - Placeholder text in a form component refers to a short label or prompt that appears within an input field as a hint to the user on what type of information is expected to be entered in that field. Placeholder text disappears when the user starts typing into the field and reappears if the field is left empty. It provides a visual cue to the user, but does not act as a permanent label or value for the field.
-   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.
- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.

-   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

-   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

-   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

-   **Default Value** - This option allows you to add a default value in a form field. The text disappears when the user starts typing into the field. If **Disabled Component** or **Read-Only Component** is selected, the default value is displayed on the screen. If no value is entered by user in the form field, this value is submitted at the time of form submission.

-   **Allow Multiple Lines** - This option allows user to enter multiple lines in a form field. 

-   **Autofill Attribute** - The option enables users to input a value that is automatically populated within the form field based on the stored information.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/textinput_validationtab.png)

-   **Required** - Select this option, if you want to display the component in an Adaptive Form. After selecting the option, you must enter a value before proceeding with a form submission. You cannot select the **Hide Component** or **Disable Component**  in the **Basic** tab when this option is selected.

-   **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the field is left blank.

-   **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

-   **Maximum Number of characters** - This option allows you to specify the maximum number of characters allowed  in the component. If you enter characters greater than the value specified in **Maximum Number of characters**, an error message appears on the screen. The **Maximum characters error message** dialog box allows you to add a custom error message.
 
-   **Maximum characters error message** - The **Maximum characters error message** dialog box allows you to add a custom error message if you enter characters greater than the value specified in the **Maximum Number of characters** option.

-   **Minimum Number of characters** - This option allows you to specify the minimum number of characters allowed in the field. If you enter characters less than the value specified in **Minimum Number of characters**, an error message appears on the screen. The **Minimum characters error message** dialog box allows you to add a custom error message.
 
-   **Minimum characters error message** - The **Minimum characters error message** dialog box allows you to add a custom error message if you enter characters less than the value specified in the **Minimum Number of characters** option.

The **Validation Pattern** option allows you to enter a pattern to validate the entered text. In case the text fails to validate with the value entered in **Pattern** option , the error message appears on screen.

-   **Pattern** - This option allows you to enter the allowed verification patterns for text. Regular expressions are also allowed.

-   **Error Message** - This option allows you to enter a message that is displayed on the screen if the entered text fails to validate with the value entered in the **Pattern** option

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/textinput_helptab.png)

-   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

-   **Always show short description** - Enable the option to display the Short description below the component.

-   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

**Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Text box component.

### Styles Tab {#styles-tab}

The tab is used to define and manage CSS styles for a component. The Adaptive Forms Text box Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Style tab](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Text Input Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties 

![Custom Properties Dialog](/help/adaptive-forms/assets/datepicker_customproperties.png)

Custom properties allows you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.

- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the order of the custom property name and custom property value.

### Formats Tab {#formats-tab}

The formats tab allows you to specify default and custom date formats.

![Formattab](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}
