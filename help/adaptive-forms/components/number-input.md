---
title: Adaptive Forms Core Component - Number input
description: Using or customizing the Adaptive Forms Number input Core Component.
role: Architect, Developer, Admin, User
---

# Number input {#number-input-adaptive-forms-core-component}

A Number Input component in an Adaptive form is a type of form field that allows users to input numerical values. The component is typically represented by a text field with a up and down arrow for incrementing and decrementing the number.

It can also be used with attributes like min, max, step, value, and more. These attributes can be used to set the minimum and maximum values allowed in the field, the step interval for incrementing or decrementing the number, and the default value of the field.

This component can be used to gather numerical data like age, quantity, and more. and can also be used to perform mathematical operations like addition and  subtraction. This component can also be used to validate the numerical data entered by the user.

For accessibility, it is important to specify 'label' that describes the purpose of the number input field, and what kind of input is expected.

**Example**

![](/help/adaptive-forms/assets/numeric-stepper.png)

## Usage {#reasons-to-use-number-input-numeric-stepper}

There are several reasons why it is beneficial to include a numeric input component in an Adaptive Form, including:

*   **Data Collection**: Numeric fields are used to collect numerical data such as age, quantity, weight, etc.

*   **Mathematical Operations**: Numeric fields can be used to perform mathematical operations such as addition, subtraction, multiplication and division.

*   **Validation**: Numeric fields can be used to validate data entered by the user and ensure that only valid numerical values are accepted.

*   **Data Range**: Numeric fields can be used to set a range of valid values through the use of min, max, and step attributes.

*   **User Experience**: Numeric fields can be used to make the form more user-friendly by providing a clear and intuitive way for users to input numerical data.

*   **Rule based actions**: A numeric component can also be used to trigger different rule based actions like submitting form, opening a website, show/hide components, add an instance of a panel or component to the button.

*   **Adaptive forms**: A numeric component is a core component that allows users to add a number input field to an Adaptive Form.

*   **Dynamic Content**: Numeric component can be used to display dynamic data based on the form fields.

*   **Accessibility**: Numeric fields can be made accessible by including an appropriate label and providing clear instructions on what kind of input is expected.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Number input Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Number input Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your number input experience for visitors with the Configure Dialog. You can also define number input options with ease for a seamless user experience.

### Basic Tab {#basic-tab}

![Basic Tab](/help/adaptive-forms/assets/numberinput_basictab.png)

* **Name** - The name uniquely identifies the component in the rule editor.Special characters and spaces are not allowed in the name strings.

* **Title** - Title is a string that appears at the top of a component in an Adaptive Form. Title uniquely identifies the component in the tree structure of an Adaptive Form. If you do not add a title, the name of the component is displayed instead of the title text.

* **Placeholder Text** - 
* **Bind Reference** - 
* **Hide Component** -
* **Disable Component** -
* **Number Typr** - 
* **Default Value** -

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/numberinput_validationtab.png)

* **Required** - When this option is selected, the component type is displayed in an Adaptive Form. In the **Basic** tab, the **Hide Component** and **Disable Component** become non-clickable when this option is selected.

* **Error Message** -The option allows you to enter a message to be displayed if the required fields are left blank.

* **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails on an adaptive Form submission.

* **Lowest number / Smallest number** - Use this option to select the minimum allowed number to be entered. If the number than the number specified in **Lowest number / Smallest number** option is entered, the error message appears. 

* **Exclude Minimum Value**

### Help Content Tab {#help-content}

![Help Content tab](/help/adaptive-forms/assets/button_helptab.png)

* **Short Description** - The short description provides enough context to user to understand the functionality of the component. The entered text appears as a tool tip when the user hovers the mouse pointer over the component type. You can also format the text that appears in the short description.

* **Always show short description** - Select this option to display a short description even if the user does not hover over a component type.

* **Help Text** - Help text consists of information or error messages about the component type. Help text is available by clicking the icon that appears above the component type. Click the icon to display help text above the component type.You can also format the text that appears in the help section.

### Accessibility {#accessibility}

![Accessibility tab](/help/adaptive-forms/assets/button_accessibilitytab.png)

On the **Accessibility** tab, values are set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component. Various options are available for using the text for screen reader:
* **Custom text**: Select this option to use the custom text for ARIA accessibility labels. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
* **Description**: Select this option to use the description for ARIA accessibility labels.
* **Title**: Select this option to use the title for ARIA accessibility labels.
* **Name**: Select this option to use the name for ARIA accessibility labels.
* **None**: Select this option if you do not want to add for ARIA accessibility labels.


## Design Dialog {#design-dialog}

