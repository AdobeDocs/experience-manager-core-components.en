---
title: Adaptive Forms Core Component - Button
description: Using or customizing the Adaptive Forms button Core Component.
role: Architect, Developer, Admin, User
exl-id: cb75929b-8c86-49d1-b51a-368f5b80b1a9
---
# Button Component {#button-component-adaptive-forms-core-component}

A button in an Adaptive Form is a UI element that allows users to initiate an action when clicked. The button element can be used to submit a form, reset a form, or perform other actions such as navigating to a different page or triggering custom code. The button can be created using the Button Core Component.

The Adaptive Forms Rule Editor allows users to set various actions for the button component. These actions include opening a website, showing or hiding form components, adding an instance of a panel or component, submitting or resetting a form, and more.

Adaptive Forms feature separate components for the [Submit button](/help/adaptive-forms/components/submit-button.md) and [Reset button](/help/adaptive-forms/components/reset-button.md), allowing users to conveniently submit or reset a form. The Button component can be flexibly configured to execute these actions based on specific needs.

Users can access the complete list of actions supported for the button component by using the Adaptive Forms Rule Editor. The Rule Editor allows users to create rules that are triggered by various events, such as when a button is clicked, when a form is loaded, or when a field value changes. These rules can then be used to perform various actions, such as showing or hiding components, setting field values, or submitting the form. 

## Usage {#reasons-to-use-button}

There are several reasons why it is beneficial to include a button in an Adaptive Form, including:

*   **Form submission**: A button is typically used to submit a form, allowing users to send the data they have entered to the server for processing.

*   **Form reset**: Buttons can also be used to reset a form, clearing all the data entered by the user.

*   **Navigation**: Buttons can be used to navigate between different sections of a form or different pages on a website.

*   **Event Handling**: Buttons can be used to trigger different events like opening a website, show/hide components, add an instance of a panel or component to the button.

*   **Interactivity**: Buttons can be used to create interactive forms. For example, a button can be used to open a modal dialog or to toggle a section of the form.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Button Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your button experience for visitors with the Configure Dialog. You can also define button properties with ease for a seamless user experience.

### Basic Tab {#basic-tab}

![Basic Tab](/help/adaptive-forms/assets/button_basictab.png)

*   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

*   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

*   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

*   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enables you to generate Document of Record and offers a seamless user experience for collecting and managing data.

*   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
*   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
*   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Help Content Tab {#help-content}

![Help Content tab](/help/adaptive-forms/assets/button_helptab.png)

*   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

*   **Always show short description** - Enable the option to display the Short description below the component.

*   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility {#accessibility}

![Accessibility tab](/help/adaptive-forms/assets/button_accessibilitytab.png)


*   **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

## Design Dialog {#design-dialog} 

Design Dialog is used to define and manage CSS styles for the button component.

### Styles Tab {#styles-tab}

The Adaptive Forms Button Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![design Dialog](/help/adaptive-forms/assets/button_designdialog.png)

* **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Button Core Component. 

* **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

## Related article {#related-article}

* [Create an Adaptive Form in AEM Sites Page or Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

## See Also {#see-also}

* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down.md)
* [Email-input](/help/adaptive-forms/components/email-input.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Number Input](/help/adaptive-forms/components/number-input.md)
* [Panel Container](/help/adaptive-forms/components/panel-container.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Telephone input](/help/adaptive-forms/components/telephone-input.md)
* [Text Input](/help/adaptive-forms/components/text-input.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Title](/help/adaptive-forms/components/title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

