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

*   **Long list of options**: Drop-down lists are useful for situations where there is a long list of options are available for a field. They take up less space on the form than a list of radio buttons or checkboxes, and can be less overwhelming for users.

*   **Consistency**: Drop-down lists provide consistency in the design and layout of the form, making it more intuitive and easy for users to navigate.

*   **Clarity**: Drop-down lists can make the form more clear and easy to understand by providing a clear and concise list of options.

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

* **Name** -  You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

* **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

* **Hide Title** -  Select the option to hide the component's Title.

* **Allow multiple selection** - Select this option to select multiple options from a drop-down list.

* **Save value as** - 
This option specifies the data type of the value sent when any option is selected. If the **Save value as** is set to `Number` and you add string data to **Data Value** ​​on the **Options** tab, the screen displays a `Value type mismatch` error message.

    In the **Options** tab, you can add data values and display text pairs using the **Add** button. Once a new option is added, the following actions are performed:
    
    * **Data Value** - This option allows to enter the content to submit when an option is selected.
    * **Display Text** - This option allows to enter the content to display in an Adaptive Form.
    * **Delete** - Tap or click to delete the option of a drop-down menu .
    * **Rearrange** - Tap or click and drag to rearrange the order for option of a drop-down menu. 

* **Default options** - This option allows you to add default values. Use the delete icon to remove the added option. If the **Save value as** is set to `Number` and you add string data to **Default options**, the screen displays a `Value type mismatch` error message.

* **Placeholder text** - Placeholder text in a form component refers to a short label or prompt that appears within an input field as a hint to the user on what type of information is expected to be entered in that field. Placeholder text disappears when the user starts typing into the field and reappears if the field is left empty. It provides a visual cue to the user, but does not act as a permanent label or value for the field.

* **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

*   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
*   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
*   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/dropdown_validationtab.png)

* **Required** - Select this option, if you want to display the component in an Adaptive Form. You cannot select the **Hide Component** and **Disable Component**  in the **Basic** tab when this option is selected.

* **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.

* **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/dropdown_helptab.png)

*   **Short description**: A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

*   **Always show short description**: Enable the option to display the Short description below the component.

*   **Help text**:  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)

*   **Text for screen readers**: Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

## Design Dialog {#design-dialog}

