---
title: Adaptive Forms Core Component - Switch component
description: Using or customizing the Adaptive Forms Switch Core Component.
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
---
<span class="preview"> This article contains content about the **Allow Rich Text for Title** and **Allow Rich Text for Options**  features, pre-release features. The pre-release feature is accessible only through our [pre-release channel](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

# Switch Component{#switch-adaptive-forms-core-component}

 The switch component is a graphical user interface used in forms that allows users to select between two options. It is usually a two-state toggle that enables users to choose between two states, enabling or disabling a feature, setting, or functionality. The switch component is designed to visually represent the current state and display whether a particular feature is turned on or off.

The switch component is a boolean control element that sets the value to true or false. For example, it is used to toggle a feature ON or OFF, such as muting or unmuting sound, or enabling or disabling Bluetooth or WiFi.

![Switch component example](/help/adaptive-forms/assets/switch-example.png)

## Usage {#reasons-to-use-switch}

The common reasons to use switch in an Adaptive Form are:

- **User interaction**: Users can interact with the switch component by clicking or tapping on it.

- **States**: The switch component has two states: ON and OFF. The initial state of the switch component depends on the default setting or the current status of the feature that it controls.

- **Visual representation**: The switch component visually reflects its current state by changing color or position.

- **Control functionality**: The switch component is used to enable or disable specific functionality in an AEM Form. For example, it allows users to turn a feature on or off.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Switch Core Component was released as part of the Core Components 2.0.64. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|||
|---|---|
|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.64](/help/adaptive-forms/version.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Switch Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your Switch component experience for visitors with the Configure Dialog. You can also define Switch component options with ease for a seamless user experience.

### Basic Tab

![Basic tab](/help/adaptive-forms/assets/switch-basic.png)

- **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

- **Title** - With its Title, you can easily identify a component in a form and by default, the title appears at the beside of the component. If you do not add a title, the component is not displayed.
- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)

- **Hide Title** - Select the option to hide the component's Title.

- **Preserve Uncheck state value** - Selecting this option allows you to specify the value to be returned when the switch component is not selected. 
- **Options** - Specify the data value and display text for each option.
    - **On Data Value** - Specify the value to be submitted when the switch is enabled in an Adaptive Form.
    - **On Display Text** - Specify the text to be displayed as label when the switch is enabled in an Adaptive Form.
    - **Off Data Value** - Specify the value to be submitted when the switch is not enabled in an Adaptive Form. This option is visible only if the **Preserve Uncheck state value** switch is enabled.
    - **Off Display Text** - Specify the text to be displayed as label when the switch is not enabled in an Adaptive Form. This option is visible only if the **Preserve Uncheck state value** switch is enabled.

    You can also format the options for switch component using **Allow Rich Text for Options**. 
  
     ![Rich text support for options](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

    Once you select the checkbox for **Allow Rich Text for options** formatting options become visible to style the component's options. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
    
    ![Rich text support for options](/help/adaptive-forms/assets/switch-richtext-for-display.png)
      
- **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enable you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.
- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.

- **Data type of submitted value**:  This option specifies the data type of the value sent when any option is selected. If the **data type of submitted value** is set to `Number` and you add string data to **Data Value** ​​on the **Options** tab, the screen displays a `Value type mismatch` error message.
- **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

- **Disable Component** - Select the option to disable or lock the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

- **Default Value**: This option allows you to add a default value in a form field. If **Disabled Component** or **Read-Only Component** is selected, the default value is displayed on the screen. If no value is entered by user in the form field, this value is submitted at the time of form submission.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/switch-validation.png)

- **Required** - Select this option, if you want to display the component in an Adaptive Form. After selecting the option, you must make a selection before proceeding with a form submission. You cannot select the **Hide Component** or **Disable Component**  in the **Basic** tab when this option is selected.

- **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the form field is left blank.

- **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

### Help Content Tab {#helpcontent-tab}

![Help Content tab](/help/adaptive-forms/assets/switch-help.png)

- **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

- **Always show short description** - Enable the option to display the Short description below the component.

- **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}

![Accessibility tab](/help/adaptive-forms/assets/switch-accessibility.png)

**Text for screen readers** - Text for screen readers refers to additional text that is intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

### Styles Tab {#styles-tab}

![Styles tab](/help/adaptive-forms/assets/switch-styles.png)

- **Hide Labels** - Select this option to hide the labels of the switch component.

- **Show Labels** - Select this option to show the labels of the switch component.

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Switch component.

### Styles Tab {#styles-design-tab}

The Adaptive Forms Switch Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/checkbox-style.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Switch Group Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties 

![Custom Properties Dialog](/help/adaptive-forms/assets/checkbox-customproperties.png)

Custom properties allow you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.

- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the custom property name and custom property value.

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}
