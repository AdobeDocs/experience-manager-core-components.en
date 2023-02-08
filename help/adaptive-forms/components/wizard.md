---
title: Adaptive Forms Core Component - Wizard 
description: Using or customizing the Adaptive Forms Wizard Core Component.
role: Architect, Developer, Admin, User
---

# Wizard {#wizard-adaptive-forms-core-component}

A Wizard layout in an Adaptive Form refers to a form that is divided into multiple steps or pages, with the user moving through the form one step at a time. This layout is called a "wizard" because it guides the user through the form in a step-by-step process.

Each step of the wizard typically contains a group of related form fields and a navigation mechanism, such as "Next" and "Back" buttons, to move between steps. The user can only proceed to the next step once the current step has been completed and all required fields have been filled out.

Wizard layout is useful for forms that have a lot of fields or information that need to be collected, as it breaks down the form into smaller, more manageable chunks. It also helps users to focus on one set of fields at a time, which can make the form-filling process less overwhelming.

However, it can also increase the complexity of the form, as the user has to go through several pages to complete the form. So it is necessary to evaluate the form requirement and user needs before deciding to use a wizard layout.

You can use the Wizard layout Core Component in an Adaptive Form to create Wizard layout. 


**Example**

![](/help/adaptive-forms/assets/wizard.png)

## Usage {#reasons-to-use-wizard-in-an-adaptive-form}

There are several reasons why it may be beneficial to use a Wizard layout in an Adaptive Form:

*   **Simplicity**: Breaking down a form into multiple steps can make it easier for users to understand and complete, as they can focus on one set of fields at a time.

*   **Organization**: A Wizard layout can help to organize forms by topic or purpose, and it can also group related fields together, which can make the form-filling process more logical and efficient.

*   **Validation**: A Wizard layout allows for step-by-step validation, which can help users identify and correct errors as they go, rather than waiting until the end of the form.

*   **Progress Indicator**: A wizard layout can display the progress of the form, which can help the user understand how much of the form is left to complete.

*   **Long forms**: If the form has a lot of fields, it can be overwhelming for the user to see them all at once, so breaking them down into smaller, more manageable chunks can make it less intimidating.

*   **Avoiding Abandonment**: A wizard layout can also help to reduce form abandonment, as users are more likely to complete a form if they can see progress and understand how much is left to do.

*   **Mobile Experience**: A wizard layout can also be beneficial for forms accessed on mobile devices, as it allows for smaller pages that load faster and are easier to navigate.

Overall, a Wizard layout can make the form-filling process more manageable and efficient for users, but it's important to consider the complexity of the form and the user's needs before deciding to use this type of layout.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Wizard Layout Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Title Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your wizard experience for visitors with the Configure Dialog. You can also define wizard options with ease for a seamless user experience.

### Basic Tab {#basic-tab}

![Basic tab](/help/adaptive-forms/assets/wizard_basictab.png)

*   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

*   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component.

*   **Hide Title** - Select the option to hide the component's Title.

*   **Wrap data in an object** - Choose "Wrap data in an object" to put the field data from the Wizard inside a JSON object. If not chosen, the submit data JSON has a flat structure for the Wizard's fields.

*   **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row.  

*   **Bind reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enable you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

*   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user.

*   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Help Tab {#help-tab}

![Help tab](/help/adaptive-forms/assets/wizard_helptab.png)

*   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

*   **Always show short description** - Enable the option to display the Short description below the component.

*   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.


### Accessibility Tab {#accessibility}

![Basic tab](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

*   **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

*   **HTML role for screen reader to announce** - The HTML role is an attribute used to specify the purpose of an HTML element to assistive technologies such as screen readers. The role attribute is used to provide additional context and semantic meaning to an element, making it easier for screen readers to interpret and announce the content to the user. For example, in AEM Forms, a form field's label might have the role of "label," and its input field might have the role of "textbox." This helps the screen reader understand the relationship between the label and input field, and correctly announce them to the user.


## Design Dialog {#design-dialog}

