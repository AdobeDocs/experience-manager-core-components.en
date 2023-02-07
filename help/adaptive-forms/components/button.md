---
title: Adaptive Forms Core Component - Button
description: Using or customizing the Adaptive Forms button Core Component.
role: Architect, Developer, Admin, User
---

# Button Component {#button-component-adaptive-forms-core-component}

A button in an Adaptive Form is a UI element that allows users to initiate an action when clicked. The button element can be used to submit a form, reset a form, or perform other actions such as navigating to a different page or triggering custom code. The button can be created using the Button Core Component and can be styled using CSS.

The Adaptive Forms Rule Editor allows users to set various actions for the button component. These actions include opening a website, showing or hiding form components, adding an instance of a panel or component, submitting or resetting a form, and more.

Adaptive Forms also provide separate button components for submitting or resetting a form, but the button component can also be configured to perform these actions if needed.

Users can access the complete list of actions supported for the button component by using the Adaptive Forms Rule Editor. The Rule Editor allows users to create rules that are triggered by various events, such as when a button is clicked, when a form is loaded, or when a field value changes. These rules can then be used to perform various actions, such as showing or hiding components, setting field values, or submitting the form. 

## Usage {#reasons-to-use-button}

There are several reasons why it is beneficial to include a button in an Adaptive Form, including:

*   **Form submission**: A button is typically used to submit a form, allowing users to send the data they have entered to the server for processing.

*   **Form reset**: Buttons can also be used to reset a form, clearing all the data entered by the user.

*   **Navigation**: Buttons can be used to navigate between different sections of a form or different pages on a website.

*   **Event Handling**: Buttons can be used to trigger different events like opening a website, show/hide components, add an instance of a panel or component to the button.

*   **Interactivity**: Buttons can be used to create interactive forms. For example, a button can be used to open a modal dialog or to toggle a section of the form.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Button Core Component v1 was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Button Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your button experience for visitors with the Configure Dialog. You can also define button properties with ease for a seamless user experience.

## Basic Tab {#basic-tab}

![Basic Tab](/help/adaptive-forms/assets/button_basictab.png)

* **Name** - The name uniquely identifies the component in the rule editor.Special characters and spaces are not allowed in the name strings.

* **Title** - Title is a string that appears at the top of a component in an Adaptive Form. Title uniquely identifies the component in the tree structure of an Adaptive Form. If you do not add a title, the name of the component is displayed instead of the title text.

* **Bind Reference** - This option allows you to link an Adaptive Form field to the schema. When user enters any value in a linked field of an Adaptive Form that value also appears in the associated schema.

* **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record.
* **Hide Component** - Select this option if you do not want to make the component type visible in an Adaptive Form. The component remains active in edit mode. 
* **Disable Component** - Select this option if you want to disable the component in an Adaptive Form. The component remains active in edit mode. 
* **Read-only** - Select this option if you want to make the component type immutable in an Adaptive Form. The component remains active in edit mode.

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
