---
title: Adaptive Forms Core Component - Checkbox Group
description: Using or customizing the Adaptive Forms Checkbox Group Core Component.
role: Architect, Developer, Admin, User
---

# Checkbox Group {#button-component-adaptive-forms-core-component}

A checkbox group in an Adaptive Form is a set of related checkboxes that allow users to select one or more options from a list. Each checkbox is represented by a Data Value (value used to process items of a checkbox group) and Display value (label for each checkbox item that describes its purpose)

**Example**

![](/help/adaptive-forms/assets/checkbox-group.png)

**Properties Dialog**

![](/help/adaptive-forms/assets/checkbox-group-properties.png)

In this example, Options element is used to group the checkboxes together. The **Display text** element is used to provide a label for an item and **Data Value** is used to specify the value that is sent to the server when the form is submitted. 

Each checkbox option/item has a unique Data value and Display Text attribute. If a user selects the "Son" and "Daughter" checkboxes, the corresponding Data Value is sent to the server when the form is submitted. This data can then be processed by a server-side script to determine which options were selected by the user, and can be used to perform various actions, such as updating other fields in the form or submitting the form data to a server-side script for further processing.

Additionally, The checkbox group can be configured to have different processing values for each option, and this can be set by using Adaptive Forms Rule Editor.

## Usage {#reasons-to-use-check-box-group}

There are several reasons why it is beneficial to include a checkbox group in an Adaptive Form, including:

*   **Multiple selections**: A checkbox group allows users to select multiple options from a list, which can be useful in situations where multiple selections are allowed or required.

*   **Data validation**: A checkbox group can be configured to validate the data entered by the user, ensuring that only valid options are selected.

*   **Customization**: Checkbox group can be customized to suit the specific needs of the form, such as adding a search box, or displaying the options in a hierarchical structure.

*   **Accessibility**: Checkbox group can be made accessible by providing a clear label, and making sure that the options are clearly visible and readable.

*   **User experience**: Checkbox group can be used to make the form more user-friendly by providing a clear and intuitive way for users to select multiple options.

*   **Data analysis**: Checkbox group can be used to collect data from various sources and analyze it, or use it as input for further processing.

*   **Surveys**: Checkbox group can be used in surveys to select multiple options for a question.

*   **User preferences**: Checkbox group can be used to collect user preferences for different options.

*   **Conditional logic**: Checkbox group can be used to show or hide other form fields based on the user selection

*   **Data Value**: Checkbox group can also be used to process items of a checkbox group.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Checkbox Group Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Checkbox Group Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your checkbox experience for visitors with the Configure Dialog. You can also define checkbox options with ease for a seamless user experience.

### Basic Tab {#basic-tab}

![Basic tab](/help/adaptive-forms/assets/checkbox_basictab.png)

* **Name** - The name is a short string that uniquely identifies a component type.

* **Title** - Title is a string that appears at the top of a component type in an Adaptive Form.

* **Hide Title** - When this option is selected,the title of a component type is not displayed.

    In the **Options** tab, you can add data values and display text pairs using the **Add** button. Once new option is added, the following actions are performed:
    
    * **Data Value** - This option allows to enter the content to submit when an option is selected.
    * **Display Text** - This option allows to enter the content to display in an Adaptive Form.
    * **Delete** - Tap or click to delete the option of a checkbox .
    * **Rearrange** - Tap or click and drag to rearrange the order of the panels. 

* **Bind Reference** - This option allows you to get the list items from the local schema.

* **Data type of submitted value** - This option specifies the data type of the value sent when any option is selected.

* **Display options** -  This option is used to set the visual alignment of checkboxes in an Adaptive Form. The two placement types  supported are::
    * **Horizontal** - When this option is selected, check boxes are displayed left to right in an Adaptive Form.
    * **Vertical** - When this option is selected, check boxes are displayed top to bottom in an Adaptive Form.
* **Default options** - 
* **Hide Component** - When this option is selected, a component type is not displayed. 
* **Disable Component** - When this option is selected, a component type is not selected.
* **Read-only** - When this option is selected, the properties of a component type is not modified.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/checkbox_validationtab.png)

* **Required** - When this option is selected, the checkbox is displayed in an Adaptive Form. In the **Basic** tab, the **Hide Component** and **Disable Component** become non-clickable when this option is selected.

* **Error Message** -The option allows you to enter a message to be displayed if the required fields are left blank.

* **Script Validation Message** - This option allows you to enter a message to be displayed if the script fails validation.

### Help Content tab {helpcontent-tab}

![Help Content tab](/help/adaptive-forms/assets/checkbox_helptab.png)

* **Short Description** - A short description provides enough context for the user to understand what the checkbox options convey . You can also format the text that appears in the short description.

* **Always show short description** - Select this option to display a short description even if the user does not hover over a component type.

* **Help Text** - Help text consists of information or error messages about the component type. Help text is available by clicking the icon that appears above the component type. Click the icon to display help text above the component type in edit mode.You can also format the text that appears in the help section.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/checkbox_accessibility.png)

Text for Screen Readers uses a Text-To-Speech (TTS) engine to convert information into speech. You can listen to information  through headphones or speakers. Various options are available for using the text for screen reader:

* **Custom text**: Select this option to use the custom text as a audio text. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box using **Add** button. Tap or click the delete option to remove the checkbox option.

* **Title**: Select this option to use the title as a audio text.
