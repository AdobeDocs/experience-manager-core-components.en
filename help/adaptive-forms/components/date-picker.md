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

*   **Data validation**: A date picker component can be configured to validate the date entered by the user, ensuring that only valid dates are selected.

*   **Customization**: Date picker component can be customized to suit the specific needs of the form, such as adding a time picker, or showing the date in different formats like date, month, year.

*   **Accessibility**: Date picker component can be made accessible by providing a clear label, and making sure that the options are clearly visible and readable.

*   **User experience**: Date picker component can be used to make the form more user-friendly by providing a clear and intuitive way for users to select date.

*   **Data analysis**: Date picker component can be used to collect data from various sources and analyze it, or use it as input for further processing.

*   **Event Management**: Date picker component can be used in event management websites to select the event date.

*   **Booking and reservation**: Date picker component can be used in booking and reservation websites to select the check-in and check-out dates.

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

* **Name** - The name uniquely identifies the component in the rule editor.Special characters and spaces are not allowed in the name strings.

* **Title** - Title is a string that appears at the top of a component in an Adaptive Form. Title uniquely identifies the component in the tree structure of an Adaptive Form. If you do not add a title, the name of the component is displayed instead of the title text.

* **Hide Title** - Select this option to hide title of the component type in an Adaptive Form.

* **Placeholder text** - 

* **Hide Component** - Select this option if you do not want to make the component type visible in an Adaptive Form. The component remains active in edit mode. 
* **Disable Component** - Select this option if you want to disable the component in an Adaptive Form. The component remains active in edit mode. 
* **Read-only** - Select this option if you want to make the component type immutable in an Adaptive Form. The component remains active in edit mode.
* **Default Date** - This option allows you to add a date to your component type. The entered date appears by default at the place of the component type. If **Disabled Component** or **Read-Only Component** is selected, the default date is displayed on the screen.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/datepicker_validation.png)

* **Required** - When this option is selected, the component type is displayed in an Adaptive Form. In the **Basic** tab, the **Hide Component** and **Disable Component** become non-clickable when this option is selected.

* **Error Message** -The option allows you to enter a message to be displayed if the required fields are left blank.

* **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails on an adaptive Form submission.

* **Minimum Date** - This option allows you to enter the minimum required date. If you enter a date that is earlier than the date specified in Minimum Date, an error message appears on the screen. The **Minimum Error Message** dialog box allows you to add a custom error message.

* **Minimum Error Message** - The **Minimum Error Message** dialog box allows you to add a custom error message if you enter a date earlier than the date specified in the **Minimum Date** option.

* **Maximum Date** - This option allows you to enter the maximum required date. If you enter a date that is later than the date specified in Maximum Date, an error message appears on the screen. The **Maximum Error Message** dialog box allows you to add a custom error message.

* **Maximum Error Message** - The **Maximum Error Message** dialog box allows you to add a custom error message if you enter a date later than the date specified in the **Maximum Date** option.

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/datepicker_helptab.png)

* **Short Description** - A short description provides enough context for the user to understand what the checkbox options convey. The entered text appears as a tool tip when the user hovers the mouse pointer over the component type. You can also format the text that appears in the short description.

* **Always show short description** - Select this option to display a short description even if the user does not hover over a component type.

* **Help Text** - Help text consists of information or error messages about the component type. Help text is available by clicking the icon that appears above the component type. Click the icon to display help text above the component type.You can also format the text that appears in the help section.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

On the **Accessibility** tab, values are set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component. Various options are available for using the text for screen reader:
* **Custom text**: Select this option to use the custom text for ARIA accessibility labels. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
* **Description**: Select this option to use the description for ARIA accessibility labels.
* **Title**: Select this option to use the title for ARIA accessibility labels.
* **Name**: Select this option to use the name for ARIA accessibility labels.
* **None**: Select this option if you do not want to add for ARIA accessibility labels.

### Formats Tab {#format-tab}

![Formats tab](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Display Format** - It represents the date format that is displayed to the user. The Type option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

* **Edit Format** - It represents a date format in which the user edits the date. The Type option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

## Design Dialog {#design-dialog}

