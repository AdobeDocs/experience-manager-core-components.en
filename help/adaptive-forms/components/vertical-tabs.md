---
title: Adaptive Forms Core Component - Vertical tabs
description: Using or customizing the Adaptive Forms Vertical tabs Core Component.
role: Architect, Developer, Admin, User
---

# Vertical Tabs {#vertical-tabs-adaptive-forms-core-component}

Vertical tabs in an Adaptive Form refer to a design pattern where multiple sections of a form are grouped together and displayed as separate tabs, aligned vertically. The user can switch between the tabs to access different sections of the form. Each tab acts as a trigger to show and hide the related form content. The vertical tabs help to organize long forms into manageable sections and improve the user experience. Tabs can help to make a form more accessible for users with disabilities, as they can switch between sections using keyboard navigation.

The tabs are usually created as a series of links or buttons, with each link or button corresponding to a section of the form. When a user clicks on a tab, the form content is dynamically updated to show the corresponding section.

## Usage {#reasons-to-use-vertical-tabs}

The common reasons to use vertical tabs in an Adaptive Form are:

- **Improved Usability**: Vertical tabs make it easier for users to navigate through the form, especially if the form has multiple sections or a large number of fields.

- **Space Management**: Vertical tabs help to conserve screen space by grouping related form sections into tabs and displaying only one section at a time.

- **Better Organization**: Tabs provide a clear and organized structure for a form, making it easier for users to understand and complete the form.

- **Increased User Engagement**: Vertical tabs can make a form more visually appealing and engaging for users, which can improve the form completion rate.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Vertical tabs Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|||
|---|---|
|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Vertical tabs Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/verticaltabs/v1/verticaltabs). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).


## Configure Dialog {#configure-dialog}

You can easily customize your Vertical tabs experience for visitors with the Configure Dialog. You can also define Vertical tabs options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic tab](/help/adaptive-forms/assets/vertical-tab-basic.png)

- **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

- **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

- **Hide Title** - Select the option to hide the component's Title.

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

- **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enable you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.
- **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
- **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Repeat Vertical Tab {#repeat-tabs-on-top}

![Repeat tab](/help/adaptive-forms/assets/vertical-tab-repeat-vertical-tab.png)

You can use the repeatibility options to duplicate Vertical-tabs component and its child components, define a minimum and maximum repetition count, and facilitates the replication of similar sections within a form. When interacting with the Vertical-tabs  component and accessing its settings, the following options are presented:

- **Make Vertical-tabs repeatable**: A toggle feature that allows users to enable or disable the repeatability functionality.
- **Minimum repetitions**: Establishes the minimum number of times the Vertical-tabs component can be repeated. A value of zero indicates that the Vertical-tabs component is not repeated; the default value is zero.
- **Maximum repetitions**: Sets the maximum number of times the Vertical-tabs component can be repeated. By default, this value is unlimited.

To effectively manage repeatable sections within the Vertical-tabs, follow the steps provided in the [Creating forms with repeatable sections](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) article.

### Items Tab {#items-tab}

![Items tab](/help/adaptive-forms/assets/vertical-tab-items.png)

The **Add** button allows you to select a component to add as a panel from the component selection window. After adding the component, you can see the following options:

- **Icon** - The icon identifies the component of the panel in the list. You can hover mouse over the icon to see the full component name as a tooltip.
- **Description** - The description used as the text of the panel. By default, the name of the component selected for the panel.
- **Delete** - Tap or click to delete the panel from the Vertical-tabs  component.
- **Rearrange** - Tap or click and drag to rearrange the order of the panels.

### Help Content Tab {#help-content}

![Help Content tab](/help/adaptive-forms/assets/vertical-tab-help.png)

- **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

- **Always show short description** - Enable the option to display the Short description below the component.

- **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility}

![Accessibility tab](/help/adaptive-forms/assets/vertical-tab-accessibility.png)

- **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

- **HTML role for screen reader to announce** - The HTML role is an attribute used to specify the purpose of an HTML element to assistive technologies such as screen readers. The role attribute is used to provide additional context and semantic meaning to an element, making it easier for screen readers to interpret and announce the content to the user. For example, in AEM Forms, a form field's label might have the role of "label," and its input field might have the role of "textbox." This helps the screen reader understand the relationship between the label and input field, and correctly announce them to the user.

## Design Dialog {#design-dialog} 

The Design Dialog lets template creators control how things are displayed by default. For the Adaptive Forms Vertical-tabs  component, you can set the following:

- The core components that a form creator can add to the Vertical-tabs  in the Adaptive Forms editor
- Simple names for styles (CSS classes) which can be applied in the properties dialog  of Vertical-tabs  component in the Adaptive Forms editor.

This helps make the process of creating and customizing forms more straightforward and efficient.

### Allowed Components Tab {#allowed-components-tab}

![Allowed Components tab](/help/adaptive-forms/assets/tabs-allowed-component.png)

The **Allowed Components** tab allows template editor to set the components that can be added as items to the panels in the Vertical tabs component in the Adaptive Forms editor.

### Styles Tab {#styles-tab}

![Styles tab](/help/adaptive-forms/assets/tabs-styles-tab.png)

The Design Dialog is used to define and manage CSS styles for a component. The Adaptive Forms Vertical tabs Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Vertical tabs Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties tab

![Custom Properties tab](/help/adaptive-forms/assets/tabs-custom-properties.png)

Custom properties allows you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.

- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the order of the custom property name and custom property value.

## Related Articles {#related-articles}

- [Accordion](/help/adaptive-forms/components/accordion.md)
- [Button](/help/adaptive-forms/components/button.md)
- [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
- [Date Picker](/help/adaptive-forms/components/date-picker.md)
- [Drop-down list](/help/adaptive-forms/components/drop-down.md)
- [Email-input](/help/adaptive-forms/components/email-input.md)
- [Form Container](/help/adaptive-forms/components/form-container.md)
- [File Attachment](/help/adaptive-forms/components/file-attachment.md)
- [Footer](/help/adaptive-forms/components/footer.md)
- [Header](/help/adaptive-forms/components/header.md)
- [Image](/help/adaptive-forms/components/image.md)
- [Number Input](/help/adaptive-forms/components/number-input.md)
- [Panel Container](/help/adaptive-forms/components/panel-container.md)
- [Radio Button](/help/adaptive-forms/components/radio-button.md)
- [Reset Button](/help/adaptive-forms/components/reset-button.md)
- [Submit Button](/help/adaptive-forms/components/submit-button.md)
- [Telephone input](/help/adaptive-forms/components/telephone-input.md)
- [Text Input](/help/adaptive-forms/components/text-input.md)
- [Text](/help/adaptive-forms/components/text.md)
- [Title](/help/adaptive-forms/components/title.md)
- [Wizard](/help/adaptive-forms/components/wizard.md)

## See Also {#see-also}

{{see-also}}