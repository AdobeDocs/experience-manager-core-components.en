---
title: Adaptive Forms Core Component - Checkbox
description: Using or customizing the Adaptive Forms Checkbox Core Component.
role: Architect, Developer, Admin, User
exl-id: c6ca4800-bd10-4aeb-957a-fb1780cf94f3
---

<span class="preview"> This article contains content about the **Allow Rich Text for Title** feature, a pre-release feature. The pre-release feature is accessible only through our [pre-release channel](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

# Checkbox Component{#checkbox-component}

A checkbox is a graphical user interface element commonly used in software applications and forms to allow users to make a binary choice between two options: checked (selected) or unchecked (deselected). 

A checkbox is usually represented as a small square that can be toggled on or off by clicking or tapping it. When a checkbox is checked, it displays a checkmark to show that the associated option or feature is active or enabled.

>[!NOTE]
>
> For AEM 6.5 Forms, this component was introduced with AEM 6.5 Forms Service Pack 19 (6.5.19.0). To enable this component, ensure that the necessary versions of both Forms Core Components and WCM Core Components are installed. For detailed information on the releases of Adaptive Forms Core Components, please refer to [Adaptive Forms Core Components releases](/help/adaptive-forms/version.md)

**Example**

![checkbox group](/help/adaptive-forms/assets/checkbox-example.png)

## Usage {#reasons-to-use-checkbox}

The common reasons to use checkbox in an Adaptive Form are:

- **Ease of Use**: Checkboxes are visually clear and provide a straightforward way to make binary choices. They are intuitive and easy to understand, making them user-friendly.

- **Consent and Agreement**: Checkboxes are used to obtain user consent for various purposes, for example accepting terms and conditions, subscribing to newsletters, or confirming age verification. They make it clear that the user is actively agreeing to something.

- **Visual Confirmation**: Checked checkboxes provide a visual confirmation to users that their selection has been recorded. This feedback helps prevent user errors and ensures they know their choices have been registered.

- **Error Prevention**: Checkboxes reduce the errors probability by allowing users to review and confirm the choices before form submission.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Checkbox Core Component was released as part of the Core Components 2.0.52. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|||
|---|---|
|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.52](/help/adaptive-forms/version.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Checkbox Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkbox/v1/checkbox). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your Checkbox experience for visitors with the Configure Dialog. You can also define Checkbox options with ease for a seamless user experience.

![Basic tab](/help/adaptive-forms/assets/checkbox-basic.png)

- **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

- **Title** - With its Title, you can easily identify a component in a form and by default, the title appears at the beside of the component. If you do not add a title, the component is not displayed.

- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)

- **Hide Title** - Select the option to hide the component's Title.

- **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enable you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.

- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.

- **Data type of submitted value**:  This option specifies the data type of the value sent when any option is selected. If the **data type of submitted value** is set to `Number` and you add string data to **Data Value** ​​on the **Options** tab, the screen displays a `Value type mismatch` error message.

- **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

- **Disable Component** - Select the option to disable or lock the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
<!-- - **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.-->
- **When Checked, return value** -Select this option to specify what value should be associated with the checkbox when it is checked or selected. It is the action that occurs when a you mark or tick the checkbox.
-  **Preserve Uncheck state value**- Select this option to specify the value to be returned when the checkbox component is not selected. If **Preserve Uncheck state value** is enabled or set to true, **When Unchecked, return value** option appears.
- **When Unchecked, return value** - The option allows you to specify what value should be associated with the checkbox when it is in an unchecked or deselected state.

- **Default Value**: This option allows you to add a default value in a form field. If **Disabled Component** or **Read-Only Component** is selected, the default value is displayed on the screen. If no value is entered by user in the form field, this value is submitted at the time of form submission.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/checkbox-validation.png)

- **Required** - Select this option, if you want to display the component in an Adaptive Form. After selecting the option, you must make a selection before proceeding with a form submission. You cannot select the **Hide Component** or **Disable Component**  in the **Basic** tab when this option is selected.

- **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.
- **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

### Help Content Tab {#helpcontent-tab}

![Help Content tab](/help/adaptive-forms/assets/checkbox-help.png)

- **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

- **Always show short description** - Enable the option to display the Short description below the component.

- **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/checkbox-accessibility.png)

**Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Check-box component.

### Styles Tab {#styles-tab}

The Adaptive Forms Checkbox Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/checkbox-style.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Checkbox Core Component. 

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
