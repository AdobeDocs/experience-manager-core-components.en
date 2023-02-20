---
title: Adaptive Forms Core Component - Horizontal tabs
description: Using or customizing the Adaptive Forms Horizontal tabs Core Component.
role: Architect, Developer, Admin, User
exl-id: fbdf330b-3b85-4f94-9dab-eea8465fba67
---
# Horizontal tabs {#horizontal-tabs-adaptive-forms-core-component}

Horizontal tabs in an Adaptive Form refer to a design pattern where multiple sections of a form are grouped together and displayed as separate tabs, aligned horizontally. The user can switch between the tabs to access different sections of the form. Each tab acts as a trigger to show and hide the related form content. The horizontal tabs help to organize long forms into manageable sections and improve the user experience. Tabs can help to make a form more accessible for users with disabilities, as they can switch between sections using keyboard navigation.

The tabs are usually created as a series of links or buttons, with each link or button corresponding to a section of the form. When a user clicks on a tab, the form content is dynamically updated to show the corresponding section.

## Usage {#reasons-to-use-horizontal-tabs}

The common reasons to use horizontal tabs in an Adaptive Form are:

*   **Improved Usability**: Horizontal tabs make it easier for users to navigate through the form, especially if the form has multiple sections or a large number of fields.

*   **Space Management**: Horizontal tabs help to conserve screen space by grouping related form sections into tabs and displaying only one section at a time.

*   **Better Organization**: Tabs provide a clear and organized structure for a form, making it easier for users to understand and complete the form.

*   **Increased User Engagement**: Horizontal tabs can make a form more visually appealing and engaging for users, which can improve the form completion rate.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Horizontal tabs Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|||
|---|---|
|Component Version|AEM as a Cloud Service|
|--- |--- |
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Horizontal tabs Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal tabs/v1/pageHorizontal tabs). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your Horizontal tabs experience for visitors with the Configure Dialog. You can also define Horizontal tabs options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic tab](/help/adaptive-forms/assets/tabsontop_basictab.png)

*   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

*   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

*   **Hide Title** - Select the option to hide the component's Title.

*   **Wrap data in object** - Choose "Wrap data in an object" to put the field data from the Wizard inside a JSON object. If not chosen, the submit data JSON has a flat structure for the Wizard's fields.

*   **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row. 

*   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.
*   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
*   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.

### Items Tab {#items-tab}

![Items tab](/help/adaptive-forms/assets/tabsontop_itemstab.png)

The **Add** button allows you to select a component to add as a panel from the component selection window. After adding the component, you can see the following options:

* **Icon** - The icon identifies the component of the panel in the list. You can hover mouse over the icon to see the full component name as a tooltip.
* **Description** - The description used as the text of the panel. By default,the name of the component selected for the panel.
* **Delete** - Tap or click to delete the panel from the horizontal tab component.
* **Rearrange** - Tap or click and drag to rearrange the order of the panels.

### Help Content Tab {#help-content}

![Help Content tab](/help/adaptive-forms/assets/tabsontop_helptab.png)

*   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

*   **Always show short description** - Enable the option to display the Short description below the component.

*   **Help text** -  Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility}

![Accessibility tab](/help/adaptive-forms/assets/tabsontop_accessibilitytab.png)

*   **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

*   **HTML role for screen reader to announce** - The HTML role is an attribute used to specify the purpose of an HTML element to assistive technologies such as screen readers. The role attribute is used to provide additional context and semantic meaning to an element, making it easier for screen readers to interpret and announce the content to the user. For example, in AEM Forms, a form field's label might have the role of "label," and its input field might have the role of "textbox." This helps the screen reader understand the relationship between the label and input field, and correctly announce them to the user.

## Design Dialog {#design-dialog}

The Design Dialog lets template creators control how things are displayed by default. For the Adaptive Forms component, you can set the following:

* The core components that a form creator can add to the horizontal tabs in the Adaptive Forms editor
* Simple names for styles (CSS classes) which can be applied in the properties dialog  of horizontal tabs component in the Adaptive Forms editor.

This helps make the process of creating and customizing forms more straightforward and efficient.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab allows template editor to set the components that can be added as items to the panels in the Horizontal tabs component in the Adaptive Forms editor.

![Horizontal tabs](/help/adaptive-forms/assets/horizontaltabs_designdilog.png)

### Styles Tab {#styles-tab}

The tab is used to define and manage CSS styles for a component. The Adaptive Forms Horizontal tabs Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Style tab](/help/adaptive-forms/assets/horizontaltabs_designstyletab.png)

* **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Horizontal tabs Core Component. 

* **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.
