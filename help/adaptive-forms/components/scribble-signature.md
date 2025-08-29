---
title: Adaptive Forms Core Component - Scribble Signature
description: Using or customizing the Adaptive Forms Scribble Signature Core Component.
role: Architect, Developer, Admin, User
---

# Scribble Signature Component

<span>Scribble Signature component is under Early Adopter Program. You can write to `aem-forms-ea@adobe.com` from your official email id to join the early adopter program and request access to the capability.</span>

A Scribble Signature component in an Adaptive Form is a user interface element that allows users to draw their **signature** directly within the form using a mouse, stylus, or touchscreen. It ensures accurate capture of handwritten consent, approvals, or verification in digital workflows.

**Example**

![example](/help/adaptive-forms/assets/scribble-signature.png){width=50%,align-center}

**Various Options available in Signature Window**

- **A:** Click the **Draw** icon to draw your signature on canvas.
- **B:** Click the **Clear** icon to clear the signature on canvas.
- **C:** Click the **Geolocation** icon to add geolocation along with the signature.
- **D:** Click the **Keyboard** icon to type your name on canvas. 

 Once you select the **Save** icon in Scribble signature window, you cannot edit the signature. In case, if you want to edit the signature, you have to disregard the current signature and re-sign using the above Paint Brush/Keyboard option.

>[!NOTE]
>
> Signatures are always saved in a PNG format.

## Usage {#reasons-to-use-scribble-signature}

There are several reasons why it is beneficial to include a Scribble Signature field in a form, including:

- **Digital consent**: Allows users to provide legally valid signatures electronically.
- **Improved user experience**: Provides a natural way to sign directly on devices without scanning or uploading.
- **Paperless workflows**: Eliminates the need for printing, signing, and rescanning documents.
- **Authentication**: Acts as an additional layer of confirmation and approval.
- **Data accuracy**: Ensures correct capture of the signer's handwritten input in digital form.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Scribble Signature Core Component was released in **August 2025** as part of **Core Components 2.24.6** for Cloud Service and later.  

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.24.6](/help/adaptive-forms/version.md) and later| |

For details on versions, see [Core Components Versions](/help/adaptive-forms/version.md).

## Technical Details {#technical-details}

Get the latest technical details on the Adaptive Forms Scribble Signature Core Component on [GitHub](https://github.com/adobe/aem-core-forms-components). For more on developing Core Components, see [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The Configure Dialog allows customization of the Scribble Signature component.  

### Basic Tab {#basic-tab}

![Basic tab](/help/adaptive-forms/assets/scribble-signature-basictab.png)

- **Name** - The name uniquely identifies the component in the rule editor. Special characters and spaces are not allowed in the name strings.

-   **Title** - Title is a string that appears at the top of a component in an Adaptive Form. Title uniquely identifies the component in the tree structure of an Adaptive Form. If you do not add a title, the name of the component is displayed instead of the title text.
- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)

-   **Hide Title** - Select this option to hide title of the component type in an Adaptive Form.
- **Placeholder text** - Placeholder text in a form component refers to a short label or prompt that appears within an input field as a hint to the user on what type of information is expected to be entered in that field. Placeholder text disappears when the user starts typing into the field and reappears if the field is left empty. It provides a visual cue to the user, but does not act as a permanent label or value for the field.

- **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enable you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.

- **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
- **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

- **Signature Dialog Title**: Signature Dialog Title defines the text displayed at the top of the signature capture dialog. It serves as a prompt or instruction for the user when they are required to provide a signature. The text helps guide the user through the signing process, making the interaction clear and intuitive.

### Validation Tab

![validation tab](/help/adaptive-forms/assets/scribble-signature-validation.png)

-   **Required** - Select this option, if you want to display the component in an Adaptive Form. After selecting the option, you must make a selection before proceeding with a form submission. You cannot select the **Hide Component** or **Disable Component** in the **Basic** tab when this option is selected.

-   **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.

-   **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/scribble-signature-helptab.png)

-   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

-   **Always show short description**- Enable the option to display the Short description below the component.

-   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/scribble-signature-accessibilitytab.png)

- **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 
  - **Custom text**: Select this option to use the custom text for ARIA accessibility labels. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
  - **Description**: Select this option to use the description for ARIA accessibility labels.
  - **Title**: Select this option to use the title for ARIA accessibility labels.
  - **Name**: Select this option to use the name for ARIA accessibility labels.
  - **None**: Select this option if you do not want to add for ARIA accessibility labels.

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Scribble Signature component.

### Styles Tab {#styles-tab}

The tab is used to define and manage CSS styles for a component. The Adaptive Forms Scribble Signature Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/checkbox-style.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Scribble Signature Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties 

![Custom Properties Dialog](/help/adaptive-forms/assets/checkbox-customproperties.png)

Custom properties allows you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.

- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the order of the custom property name and custom property value.

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}
