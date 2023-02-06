---
title: Adaptive Forms Core Component - Drop-down list
description: Using or customizing the Adaptive Forms Drop-down Core Component.
role: Architect, Developer, Admin, User
---

# Drop-down list {#drop-down-list-adaptive-forms-core-component}

A drop-down list in an Adaptive form allows users to select one or more option from a list of predefined options. The options can be of type String, Number, or Boolean. Additionally, the drop-down list component can be configured to have different validation and default values.

**Example**
![](/help/adaptive-forms/assets/drop-down-list.png)

## Usage {#reasons-to-use-drop-down-list}

There are several reasons why it is beneficial to include a drop-down list in an Adaptive Form, including:

*   **Limited options**: Drop-down lists are useful for situations where there are a limited number of options for a given field. They take up less space on the form than a list of radio buttons or checkboxes, and can be less overwhelming for users.

*   **Consistency**: Drop-down lists provide consistency in the design and layout of the form, making it more intuitive and easy for users to navigate.

*   **Clarity**: Drop-down lists can make the form more clear and easy to understand by providing a clear and concise list of options.

*   **Data validation**: Drop-down lists can be configured to validate the data entered by the user, ensuring that only valid options are selected.

*   **Accessibility**: Drop-down lists can be made accessible by providing a clear label, and making sure that the options are clearly visible and readable.

*   **Customization**: Drop-down lists can be customized to suit the specific needs of the form, such as adding a search box, providing an option to "other" which can be filled by user, or displaying the options in a hierarchical structure.

*   **User experience**: Drop-down lists can be used to make the form more user-friendly by providing a clear and intuitive way for users to select options.

*   **Data analysis**: Drop-down lists can be used to collect data from various sources and analyze it, or use it as input for further processing.


**Properties Dialog**

![](/help/adaptive-forms/assets/drop-down-list-properties.png)

In this example, Options element is used to define the list items. The **Display text** element is used to provide a label for list items and **Data Value** is used to specify the value that is sent to the server when the form is submitted. 

Each drop-down list option has a unique Data value and Display Text attribute. If a user selects the "Red" option, the corresponding Data Value is sent to the server when the form is submitted. This data can then be processed by a server-side script to determine which options were selected by the user, and can be used to perform various actions, such as updating other fields in the form or submitting the form data to a server-side script for further processing.

Additionally, The drop-down list can be configured to have different processing values for each option, and this can be set by using Adaptive Forms Rule Editor.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Drop-down list Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Drop-down list Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your drop-down list experience for visitors with the Configure Dialog. You can also define drop-down list options with ease for a seamless user experience.

![Basic tab](/help/adaptive-forms/assets/dropdown_basictab.png)

* **Name** - The name uniquely identifies the component in the rule editor.Special characters and spaces are not allowed in the name strings.

* **Title** - Title is a string that appears at the top of a component in an Adaptive Form. Title uniquely identifies the component in the tree structure of an Adaptive Form. If you do not add a title, the name of the component is displayed instead of the title text.

* **Hide Title** - Select this option to hide title of the component type in an Adaptive Form.

* **Allow multiple selection** - Select this option to select multiple options from a drop-down list.

* **Save value as** - This option specifies the data type of the value sent when any option is selected. If the **Save value as** is set to `Number` and you add string data to **Data Value** ​​on the **Options** tab, the screen displays a `Value type mismatch` error message.

    In the **Options** tab, you can add data values and display text pairs using the **Add** button. Once new option is added, the following actions are performed:
    
    * **Data Value** - This option allows to enter the content to submit when an option is selected.
    * **Display Text** - This option allows to enter the content to display in an Adaptive Form.
    * **Delete** - Tap or click to delete the option of a checkbox .
    * **Rearrange** - Tap or click and drag to rearrange the order of the panels. 

* **Default options** - This option allows you to add default values. Use the delete icon to remove the added options. If the **Save value as** is set to `Number` and you add string data to **Default options**, the screen displays a `Value type mismatch` error message.

* **Placeholder text** - 

* **Bind Reference** - This option allows you to bind the component to the form schema on form submission.

* **Hide Component** - Select this option if you do not want to make the component type visible in an Adaptive Form. The component remains active in edit mode. 
* **Disable Component** - Select this option if you want to disable the component in an Adaptive Form. The component remains active in edit mode. 
* **Read-only** - Select this option if you want to make the component type immutable in an Adaptive Form. The component remains active in edit mode.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/dropdown_validationtab.png)

* **Required** - When this option is selected, the component type is displayed in an Adaptive Form. In the **Basic** tab, the **Hide Component** and **Disable Component** become non-clickable when this option is selected.

* **Error Message** -The option allows you to enter a message to be displayed if the required fields are left blank.

* **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails on an adaptive Form submission.

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/dropdown_helptab.png)

* **Short Description** - A short description provides enough context for the user to understand what the checkbox options convey . You can also format the text that appears in the short description.

* **Always show short description** - Select this option to display a short description even if the user does not hover over a component type.

* **Help Text** - Help text consists of information or error messages about the component type. Help text is available by clicking the icon that appears above the component type. Click the icon to display help text above the component type in edit mode.You can also format the text that appears in the help section.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)

On the **Accessibility** tab, values are set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component. Various options are available for using the text for screen reader:
* **Custom text**: Select this option to use the custom text for ARIA accessibility labels. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
* **Description**: Select this option to use the description for ARIA accessibility labels.
* **Title**: Select this option to use the title for ARIA accessibility labels.
* **Name**: Select this option to use the name for ARIA accessibility labels.
* **None**: Select this option if you do not want to add for ARIA accessibility labels.


## Design Dialog {#design-dialog}

