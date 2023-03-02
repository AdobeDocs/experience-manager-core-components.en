---
title: Adaptive Forms Core Component - Telephone input
description: Using or customizing the Adaptive Forms Telephone input Core Component.
role: Architect, Developer, Admin, User
exl-id: d06179ac-04bd-4af4-b6ac-c4c78086058c
---
# Telephone input {#telephone-input-adaptive-forms-core-component}

The Adaptive Form telephone input Core Component allows users to input a telephone number. The telephone input field displays keyboards in mobile devices that are relevant to telephone numbers. It can be customized with additional attributes such as "pattern" and "placeholder" to specify the format and description of the telephone number. 

The telephone input field is commonly used in contact forms, registration forms, and other forms where a telephone number is required as a means of contact. The telephone input field can also be used to ensure that the user inputs a valid telephone number, as the browser can enforce certain constraints, such as the length and format of the telephone number, based on the "pattern" attribute.

## Usage {#reasons-to-use-telephone-input}

The common reasons to use a telephone input field in an Adaptive Form are:

*   **Contact Information**: A telephone input field is commonly used to collect a user's telephone number as a means of contact.

*   **Improved Data Accuracy**: By using a telephone input field, the form can enforce certain constraints on the format of the telephone number, which can help ensure that the data entered is accurate and complete.

*   **Better User Experience**: A telephone input field provides a clear and intuitive way for users to input their telephone number, and can improve the user experience by allowing users to quickly and easily enter their contact information.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Telephone input Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/telephoneinput/v1/telephoneinput). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your Telephone input experience for visitors with the Configure Dialog. You can also define Telephone input options with ease for a seamless user experience.

![Basic Tab](/help/adaptive-forms/assets/telephoneinput_basictab.png)

*   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

*   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

*   **Hide Title** - Select the option to hide the component's Title.

*   **Placeholder Text** - Placeholder text in a form component refers to a short label or prompt that appears within an input field as a hint to the user on what type of information is expected to be entered in that field. Placeholder text disappears when the user starts typing into the field and reappears if the field is left empty. It provides a visual cue to the user, but does not act as a permanent label or value for the field.

*   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

*   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

*   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

*   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

*   **Default Value** - This option allows you to add a default value in a form field. If **Disabled Component** or **Read-Only Component** is selected, the default value is displayed on the screen. If no value is entered by user in the form field, this value is submitted at the time of form submission

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/telephoneinput_validationtab.png)

*   **Required** - Select this option, if you want to display the component in an Adaptive Form. You cannot select the **Hide Component** or **Disable Component**  in the **Basic** tab when this option is selected.

*   **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the field is left blank.

*   **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

*   **Maximum Number of characters** - This option allows you to specify the maximum number of characters allowed  in the component. If you enter characters greater than the value specified in **Maximum Number of characters**, an error message appears on the screen. The **Maximum characters error message** dialog box allows you to add a custom error message.
 
*   **Maximum characters error message** - The **Maximum characters error message** dialog box allows you to add a custom error message if you enter characters greater than the value specified in the **Maximum Number of characters** option.

*   **Minimum Number of characters** - This option allows you to specify the minimum number of characters allowed in the field. If you enter characters less than the value specified in **Minimum Number of characters**, an error message appears on the screen. The **Minimum characters error message** dialog box allows you to add a custom error message.
 
*   *Minimum characters error message** - The **Minimum characters error message** dialog box allows you to add a custom error message if you enter characters less than the value specified in the **Minimum Number of characters** option.

The **Validation Pattern** option allows you to enter a pattern to validate the entered telephone number. The entered telephone number is validated against the value entered in the **Pattern** option. In case the telephone number fails to validate with the value entered in **Pattern** option , the error message appears on screen.
    
*   **Pattern** - This option allows you to enter the allowed verification patterns for telephone number. Regular expressions are also allowed.

*   **Error Message** - This option allows you to enter a message that is displayed on the screen if the entered telephone number fails to validate with the value entered in the **Pattern** option

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/telephoneinput_helptab.png)

*   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

*   **Always show short description** - Enable the option to display the Short description below the component.

*   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/telephoneinput_accessibilitytab.png)

**Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Telephone input component.

### Styles Tab {#styles-tab}

The tab is used to define and manage CSS styles for a component. The Adaptive Forms Telephone input Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

* **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Telephone input Core Component. 

* **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Formats Tab {#format-tab}

The formats tab allows you to specify default and custom number formats.

![Format Tab](/help/adaptive-forms/assets/telephoneinput_format.png)

