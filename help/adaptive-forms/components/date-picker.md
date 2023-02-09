---
title: Adaptive Forms Core Component - Date picker
description: Using or customizing the Adaptive Forms Date picker Core Component.
role: Architect, Developer, Admin, User
---

# Date picker {#date-picker-adaptive-forms-core-component}

A date picker component in an Adaptive form is a user interface element that allows users to select a date from a calendar or by manually entering a date in a specific format. The date picker component can be configured to have different formatting, validation, and default values.

**Example**

![](/help/adaptive-forms/assets/date-picker.png)

## Usage {#reasons-to-use-drop-date-picker}

There are several reasons why it is beneficial to include a date picker in an Adaptive Form, including:

*   **Convenience**: A date picker component allows users to easily select a date from a calendar without having to manually enter the date in a text field. This can save time and reduce errors.

*   **User experience**: Date picker component can be used to make the form more user-friendly by providing a clear and intuitive way for users to select date.

*   **Data analysis**: Date picker component can be used to collect data from various sources and analyze it, or use it as input for further processing.

*   **Event Management**: Date picker component can be used in event management websites to select the event date.

*   **Booking and reservation**: Date picker component can be used in booking and reservation websites to select the check-in and check-out dates.

* **Date format**: Date picker component can be used to fix the format in which the date is displayed and entered. Ensure the date format is consistent across the form to ensure a consistent user experience.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Date picker Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Date picker Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your date picker experience for visitors with the Configure Dialog. You can also define date picker options with ease for a seamless user experience.

### Basic Tab {#basic-tab}

![Basic tab](/help/adaptive-forms/assets/datepicker_basictab.png)

* **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

* **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

* **Hide Title** - Select the option to hide the component's Title.

* **Placeholder text** - Placeholder text in a form component refers to a short label or prompt that appears within an input field as a hint to the user on what type of information is expected to be entered in that field. Placeholder text disappears when the user starts typing into the field and reappears if the field is left empty. It provides a visual cue to the user, but does not act as a permanent label or value for the field.

*   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
*   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
*   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
* **Default Date** - This option allows you to add a date to the form field. The entered date appears by default at the place of the component. If no date is entered by user, this value is submitted at the time of form submission. In case **Disabled Component** or **Read-Only Component** is selected, the default date is displayed on the screen and submitted at the time of form submission.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/datepicker_validation.png)

* **Required** - Select this option, if you want to display the component in an Adaptive Form. You cannot select the **Hide Component** or **Disable Component** in the **Basic** tab when this option is selected.

* **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.

* **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

* **Minimum Date** - This option allows you to enter the minimum required date. If you enter a date earlier than the date specified in Minimum Date, an error message appears on the screen. The **Minimum Error Message** dialog box allows you to add a custom error message.

* **Minimum Error Message** - The **Minimum Error Message** dialog box allows you to add a custom error message to be displayed, if you enter a date earlier than the date specified in the **Minimum Date** option.

* **Maximum Date** - This option allows you to enter the maximum required date. If you enter a date later than the date specified in Maximum Date, an error message appears on the screen. The **Maximum Error Message** dialog box allows you to add a custom error message.

* **Maximum Error Message** - The **Maximum Error Message** dialog box allows you to add a custom error message to be displayed, if you enter a date later than the date specified in the **Maximum Date** option.

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/datepicker_helptab.png)

*   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

*   **Always show short description**- Enable the option to display the Short description below the component.

*   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

*   **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

### Formats Tab {#format-tab}

![Formats tab](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Display Format** - It represents the date format that is displayed to the user. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

* **Edit Format** - It represents a date format in which the user can edit the date. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

## Design Dialog {#design-dialog}

