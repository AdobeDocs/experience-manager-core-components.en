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

*   **Customization**: Buttons can be customized to suit the specific needs of the form, such as adding an icon or changing the color of the button.

*   **Accessibility**: Buttons can be made accessible by providing a clear label and making sure that the button is clearly visible and readable.

*   **User experience**: Buttons can be used to make the form more user-friendly by providing a clear and intuitive way for users to submit or reset the form.

*   **Event Handling**: Buttons can be used to trigger different events like opening a website, show/hide components, add an instance of a panel or component to the button.

*   **Interactivity**: Buttons can be used to create interactive forms. For example, a button can be used to open a modal dialog or to toggle a section of the form.

*   **Rule based actions**: Buttons can also be used to trigger different rule based actions like submitting form, opening a website, show/hide components, add an instance of a panel or component to the button.

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

* **Name** - The name is a short string that uniquely identifies a component type.

* **Title** - Title is a string that appears at the top of a component type in an Adaptive Form.

* **Bind Reference** - This option allows you to get the list items from the local schema.

* **Document of Record bind reference** - 

* **Hide Component** - When this option is selected, a component type is not displayed. 
* **Disable Component** - When this option is selected, a component type is not clicked.
* **Read-only** - When this option is selected, a component type is not modified.

### Help Content {help-content}

![Help Content tab](/help/adaptive-forms/assets/button_helptab.png)

* **Short Description** - A short description provides enough context for the user to understand what action the button performs. You can also format the text that appears in the short description.

* **Always show short description** - Select this option to display a short description even if the user does not hover over a component type.

* **Help Text** - Help text consists of information or error messages about the component type. Help text is available by clicking the icon that appears above the component type. Click the icon to display help text above the component type in edit mode.You can also format the text that appears in the help section.

### Accessibility {#accessibility}

![Accessibility tab](/help/adaptive-forms/assets/button_accessibilitytab.png)

Text for Screen Readers uses a Text-To-Speech (TTS) engine to convert information into speech. You can listen to information  through headphones or speakers. Various options are available for using the text for screen reader:
* **Custom text**: Select this option to use the custom text as an audio text. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
* **Description**: Select this option to use the description as an audio text.
* **Title**: Select this option to use the title as an audio text.
* **Name**: Select this option to use the name as an audio text.
* **None**: Select this option if you do not want to add audio text.

