---
title: Adaptive Forms Core Component - Panel container
description: Using or customizing the Adaptive Forms Panel container Core Component.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
---
# Panel container {#panel-container-adaptive-forms-core-component}

In an Adaptive Form, a panel is a container element that can be used to group related form elements. It allows you to group and organize different form elements in a logical and meaningful way. This can help to improve the overall structure and readability of the form, making it easier for users to understand and navigate. 

Panels can be used to create collapsible sections, which can be useful for hiding complex or less frequently used form fields, thus keeping the form simple and easy to use. It also allows you to include other components like text, checkbox, button.

It also can be used to set different rule-based actions like submitting form, opening a website, show/hide components, or add an instance of a panel. 

**Example**

![](/help/adaptive-forms/assets/panel-container.png)

## Usage {#reasons-to-use-panel-container}

There are several reasons to use a panel in a form, including:

*   **Organizing form elements**: A panel can be used to group related form elements together, making it easier for users to understand and navigate the form.

*   **Improving form structure**: By grouping form elements into panels, it can improve the overall structure and readability of the form, making it easier to understand.

*   **Creating collapsible sections**: Panels can be used to create collapsible sections, which can be useful for hiding complex or less frequently used form fields, thus keeping the form simple and easy to use.

*   **Enhancing usability**: By using panels to organize form elements, it can make the form more user-friendly and easier to use, which can lead to higher completion rates.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Panel Container Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your panel container experience for visitors with the Configure Dialog. You can also define panel container options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic tab](/help/adaptive-forms/assets/panelcontainer_basictab.png)

*   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

*   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

*   **Hide Title** - Select the option to hide the component's Title.

*   **Wrap data in object** - Choose "Wrap data in an object" to put the field data from the Wizard inside a JSON object. If not chosen, the submit data JSON has a flat structure for the Wizard's fields.

*   **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row. 

*   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enable you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.
*   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
*   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Help Content Tab {#help-content}

![Help Content tab](/help/adaptive-forms/assets/panelcontainer_helptab.png)

*   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

*   **Always show short description** - Enable the option to display the Short description below the component.

*   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility}

![Accessibility tab](/help/adaptive-forms/assets/panelcontainer_accessibilitytab.png)

*   **Text for screen readers** - Text for screen readers refers to additional text that is intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

* **HTML role for screen reader to announce** - The HTML role is an attribute used to specify the purpose of an HTML element to assistive technologies such as screen readers. The role attribute is used to provide additional context and semantic meaning to an element, making it easier for screen readers to interpret and announce the content to the user. For example, in AEM Forms, a form field's label might have the role of "label," and its input field might have the role of "textbox." This helps the screen reader understand the relationship between the label and input field, and correctly announce them to the user.

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Panel container component.

### Allowed Components Tab {#allowed-components-tab}

![Allowed Components tabs](/help/adaptive-forms/assets/panel_allowedcomponent.png)

The **Allowed Components** tab allows template editor to set the components that can be added as items to the panels in the Panel container component in the Adaptive Forms editor.

### Default Components Tab {#default-component-tab}

This tab allows template editor to map the components that can be added as items to the panels in the Panel container component in the Adaptive Forms editor.

![Panel Default Component](/help/adaptive-forms/assets/panel_defaultcomponent.png)

### Responsive settings {#responsive-settings}

 This tab allows template editor to set the number of columns to be displayed in the responsive grid.

 ![Responsive Grid](/help/adaptive-forms/assets/panel_responsivesettings.png) 

### Container Settings Tab {#container-setting-tab}

The container settings tab allows to set the position of components in the Adaptive Forms editor.

![Container Settings](/help/adaptive-forms/assets/panel_settings.png)

* **Layout**: The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to change the position of components to suit your needs. 
* **Disable layout**: You can also disable layout selection in the edit dialog by selecting the **Disable layout** checkbox.  
* **Enable background image**: This tab allows to set the background image and color in the template editor. 
* **Enable background color**: This tab  allows to set the background color in the template editor.

### Styles Tab {#styles-tab}

The tab is used to define and manage CSS styles for a component. The Adaptive Forms panel container Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Style tab](/help/adaptive-forms/assets/panel_style.png)

* **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms  Core Component. 

* **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms . To apply a style, in Adaptive Forms editor, select the component you want to apply editor the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

*   **HTML role for screen reader to announce** - The HTML role is an attribute used to specify the purpose of an HTML element to assistive technologies such as screen readers. The role attribute is used to provide additional context and semantic meaning to an element, making it easier for screen readers to interpret and announce the content to the user. For example, in AEM Forms, a form field's label might have the role of "label," and its input field might have the role of "textbox." This helps the screen reader understand the relationship between the label and input field, and correctly announce them to the user.

