---
title: Adaptive Forms Core Component - Terms and Conditions
description: Using or customizing the Adaptive Forms Terms and Conditions Core Component.
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
---
# Terms and Conditions component

A **Terms and Conditions** component refers to a section within a form that outlines the terms, rules, and conditions that users must agree to or comply with when using a service or accessing content. 

The **Terms and Conditions** component is a composite component which comprises of Text, Checkbox, and Link components. The text component contains a title along with a brief overview of the purpose and scope of the terms and conditions. It also includes a checkbox used to obtain explicit consent from the user. You can also replace a consent text with links. 

>[!NOTE]
>
> For AEM 6.5 Forms, this component was introduced with AEM 6.5 Forms Service Pack 19 (6.5.19.0). To enable this component, ensure that the necessary versions of both Forms Core Components and WCM Core Components are installed. For detailed information on the releases of Adaptive Forms Core Components, please refer to [Adaptive Forms Core Components releases](/help/adaptive-forms/version.md)

**Example**

![terms and conditions](/help/adaptive-forms/assets/terms-and-conditions.png)

See [Sub-components of Terms and Conditions component](#sub-component) section, to learn more about different components of Terms and Conditions component.

## Usage {#reasons-to-use-termsandconditions}

- **User Agreement**: The component serves as an agreement between the service provider and the user. Users are required to acknowledge and agree to the terms before accessing the service or content.

- **Legal Compliance**: It ensures legal compliance and protection for the service provider by outlining the rights, responsibilities, and liabilities of both parties.

- **Registration Processes**: The registration or sign-up forms include the **Terms and Conditions** component, requiring users to explicitly agree to the terms before creating an account or using a service.

- **E-commerce Transactions**: Online websites include the **Terms and Conditions** component so that users are prompted to agree to the terms and conditions as part of the checkout process before making purchases online.

- **Security and Privacy Agreements**: The **Terms and Conditions** component includes details on how the user data is collected, stored, and used, often complemented by a separate privacy policy

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.62 for Cloud Service and Core Components 1.1.28 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.62](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.28](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Terms and Conditions Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your terms and conditions component experience for visitors with the Configure Dialog. You can also define terms and conditions options with ease for a seamless user experience.

### Basic Tab

![Basic tab](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Name** - The name uniquely identifies the component in the rule editor. Special characters and spaces are not allowed in the name strings.

- **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.
- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)
- **Show Approval Option** - Select the option to show the consent checkbox used to obtain explicit consent from the user.

- **Show as a pop-up** - Select the option to display the terms and conditions component in a pop-up window.

- **Replace Consent text with weblink(s)**: Select the option to replace a consent text with a web link.  If the option is unchecked the consent text is displayed by default.

-   **Hide Title** - Select the option to hide the component's Title.

- **Group child components' data on form submission(Wrap data in object)** - When the option is selected, the data from its child components is nested within the parent component's JSON object. However, if the option is not selected, the submitted JSON data has a flat structure, with no object for the parent component. For example: 

    - When the option is selected, the data from the child components (for example, Street, City, and Zip Code) is nested within the parent component (Address) as a JSON object. This creates a hierarchical structure, and the data is organized under the parent component.
    
        Structure of submitted data:

         ```JSON 
    
         { "Address":

         { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }

         }
    
         ```

    - When the option is not selected, the submitted JSON data has a flat structure with no object for the parent component (Address). All data is at the same level, without any hierarchical organization.

        Structure of submitted data:

         ```JSON 
    
            { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
    
         ```

-   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

-   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
-   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/terms-and-conditions-help-tab.png)

-   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

-   **Always show short description** - Enable the option to display the Short description below the component.

-   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab

![Accessibility tab](/help/adaptive-forms/assets/terms-and-conditions-accessibility-tab.png)

**Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Terms and Conditions component.


### Styles Tab {#styles-tab}

The tab is used to define and manage CSS styles for a component. The Adaptive Forms Terms and Conditions Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/checkbox-style.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Terms and Conditions Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties 

![Custom Properties Dialog](/help/adaptive-forms/assets/checkbox-customproperties.png)

Custom properties allows you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.

- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the order of the custom property name and custom property value.

## Sub-components of Terms and Conditions component {#sub-component}

**Terms and Conditions** component is a composite component which comprises the following sub-components:
- [Link component](#link)
- [Text component](#text)
- [Checkbox component](#checkbox)

### Link component{#link}

This component replaces a consent text with a web link or links. It is used in a scenario, where user aims to offer references to particular sections, additional information, or external documents. You can easily customize the **Link** component individually for visitors with the Configure Dialog.

#### Basic Tab 

![Basic tab](/help/adaptive-forms/assets/link-basic-tab.png)

-   **Name** - The name uniquely identifies the component in the rule editor. Special characters and spaces are not allowed in the name strings.

-   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.
- **Allow Rich Text for Title** - This feature enables users to format titles using options like bold, italic, font styles, colors, and alignment, enhancing visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)

-   **Hide Title** - Select the option to hide the component's Title.

- **Links** - Specify the link and the corresponding display text that is used in place of the consent text. You can add multiple links by clicking the **Add** button. You can also format the options for checkbox group using **Allow Rich Text for Options**. Once you select the checkbox for **Allow Rich Text for Options** formatting options become visible to style the component's options. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
    
    ![Rich text support for options](/help/adaptive-forms/assets/link-options.png)
    
    After a new option is added, the following actions can be performed:

    - **Link** - This option allows to enter the URL to redirect when an option is selected.
    - **Display Text** - This option allows to enter the content to display in an Adaptive Form.
    - **Delete** - Tap or click to delete the option of a radio button .
    - **Rearrange** - Tap or click and drag to rearrange the order of the options. 

- **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enable you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.

- **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

- **Disable Component** - Select the option to disable or lock the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
- **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

#### Validation Tab

![Validation tab](/help/adaptive-forms/assets/link-validation-tab.png)

- **Required** - Select this option, if you want to display the component in an Adaptive Form. After selecting the option, you must make a selection before proceeding with a form submission. You cannot select the **Hide Component** or **Disable Component**  in the **Basic** tab when this option is selected.

- **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.

- **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

### Help Content Tab {#helpcontent-tab}

![Help Content tab](/help/adaptive-forms/assets/link-help-tab.png)

- **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

- **Always show short description** - Enable the option to display the Short description below the component.

- **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab

![Accessibility tab](/help/adaptive-forms/assets/link-accessibilty-tab.png)

**Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

### Text component {#text}

**Text** component displays the textual content that provides information to users. This component includes the actual terms and conditions, legal language, or any other relevant textual information. 

You can easily customize the [Text component](/help/adaptive-forms/components/text.md) individually for visitors with the Configure Dialog. To define text options with ease for a seamless user experience, use the [configure dialog of the text component](/help/adaptive-forms/components/text.md#configure-dialog).


### Checkbox component {#checkbox}

A checkbox is used to obtain user consent or acknowledgment. It serves as a visual indicator that the user has read and agreed to the terms outlined. It is mandatory to select the checkbox to indicate the consent of the user. 

You can easily customize the [Checkbox component](/help/adaptive-forms/components/checkbox.md) individually for visitors with the Configure Dialog. To define the properties of checkbox for a seamless user experience, use the [configure dialog of the checkbox component](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}
