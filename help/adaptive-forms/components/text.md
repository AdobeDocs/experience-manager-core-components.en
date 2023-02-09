---
title: Adaptive Forms Core Component - Text 
description: Using or customizing the Adaptive Forms Text Core Component.
role: Architect, Developer, Admin, User
---

# Text {#text-adaptive-forms-core-component}

In an Adaptive Form, text refers to the content that is displayed on the form for the user to read. This can include the text that is used to label a group of form elements, such as text fields, as well as any additional instructions or information that is provided to the user.

This can also help divide a form's structure into logical sections, making it easier for users to understand and complete the form. Additionally, it could be used for accessibility purpose to give a brief description of the element it is associated with. Such text field is typically displayed near the form components, such as before or after it.

**Example**

![](/help/adaptive-forms/assets/text.png)

## Usage {#reasons-to-use-text-label}

There are several reasons to use text in a form:

*   **Provide instructions**: Text can be used to provide instructions on how to fill out the form or what information is required.

*   **Provide context**: Text can be used to provide context for the form, such as explaining the purpose of the form or the organization collecting the information.

*   **Divide the form into logical sections**: Text can be used to divide a form into logical sections, making it easier for users to understand and complete the form.

*   **Branding and identity**: Text can be used for branding and identity purposes, such as including the organization's name in the form.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Text Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Text Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your text experience for visitors with the Configure Dialog. You can also define text options with ease for a seamless user experience.

![Basic tab](/help/adaptive-forms/assets/text_properties.png)

*   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

*   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.
* **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
*   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.


## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Text component.


### Styles Tab {#styles-tab}

The Design Dialog is used to define and manage CSS styles for a component. The Adaptive Forms Text Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

**Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Text Core Component. 

**Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.
