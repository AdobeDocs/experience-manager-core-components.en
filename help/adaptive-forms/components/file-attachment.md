---
title: Adaptive Forms Core Component - File attachment
description: Using or customizing the Adaptive Forms file attachment Core Component.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
---
# File attachment component {#file-attachment-adaptive-forms-core-component}

<span class="preview"> The **Data type of submitted value** feature is available under early adopter program. You can write to aem-forms-ea@adobe.com from your official email id to join the early adopter program and request access to the capability. </span>

A file attachment component in an Adaptive Form allows users to select and upload files from their local computer or device. The file attachment component can be configured to allow specific file types, size limits and multiple attachments.

**Example**

![example](/help/adaptive-forms/assets/upload-image.png)


## Usage {#reasons-to-use-file-attachment}

There are several reasons why it is beneficial to include a file attachment component in an Adaptive form, including:

-   **Collecting additional information**: A file attachment component allows users to upload documents, images, videos, or other types of files as part of the form submission. This can be useful for collecting additional information such as resumes, portfolios, or supporting documentation.

-   **Easy sharing of large files**: File attachment component enables users to share large files easily, without having to rely on external file-sharing services.

-   **Convenience**: File attachment component allows users to upload files from their local computer, without having to navigate away from the form or use other tools.

-   **Data analysis**: File attachment component can be used to collect data from various sources and analyze it, or use it as input for further processing.

-   **User experience**: File attachment component can be used to make the form more user-friendly by providing a clear and intuitive way for users to upload files.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms file attachment Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms File Attachment Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your file attachment experience for visitors with the Configure Dialog. You can also define file attachment options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic tab](/help/adaptive-forms/assets/fileattachement_basictab1.png)

-   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

-   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.
- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)

-   **Hide Title** -  Select the option to hide the component's Title.

-   **Button title** - This option is used to set the label of the button  displayed on an Adaptive Form.
-   **Bind Reference** - A bind reference is a reference to a data element that is stored in an external data source and used in a form. The bind reference allows you to dynamically bind data to form fields, so that the form can display the most up-to-date data from the data source. For example, a bind reference can be used to display a customer's name and address in a form, based on the customer's ID entered into the form. The bind reference can also be used to update the data source with data entered into the form. In this way, AEM Forms enables you to create forms that interact with external data sources, providing a seamless user experience for collecting and managing data.
- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.
- **Data type of submitted value**: Select the option to determine how the attached file is submitted to the server. To send the attachment as binary data, choose the `File` option. To send the attachment as a Base64-encoded string, choose the `String` option. If `String` is selected, the file in the binary format is submitted to the server as a data URL. The server automatically converts the data URL back to binary format, ensuring compatibility with existing actions, such as sending emails and generating the Document of Record, without requiring any changes from users. By default, the `File` option is selected.
-   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 
-   **Disable Component** - Select the option to disable the component. The disabled component is not active or editable by the end user. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-   **Allow multiple attachments** - Select this option to upload multiple attachments using the **File Attachment** button.
-   **Drag Drop Text** - It is the text shown at the top of the **Attach** button to prompt users to either attach or drag and drop files. You have the option to customize the text displayed at the top of the **Attach** button. Additionally, you can format the text using the rich text menu.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/fileattachment_validationtab.png)

-   **Required** - Select this option, if you want to display the component in an Adaptive Form. After selecting the option, you must attach attachments before proceeding with a form submission. You cannot select the **Hide Component** or **Disable Component**  in the **Basic** tab when this option is selected.
-   **Error Message** - This option allows you to enter a message that is displayed if the **Required** checkbox is checked and the field is left blank.

-   **Script Validation Message** - This option allows you to enter a message to be displayed if the script validation fails.

<!--   **Minimum files error message** - This option is used to enter an error message that is displayed if you upload files lesser than the specified minimum number of files.-->

-   **Maximum file size (MB)** - This option allows to specify a maximum file size. File sizes are specified in MB.
<!--   **Maximum files error message** - This option is used to enter an error message that is displayed if you upload files greater than the specified maximum number of files.-->

-   **Maximum file size error message** - This option is used to enter an error message that is displayed if you upload files of size more than the file size specified in **Maximum file size (MB)** option. 

-   **Allowed file types** - Various types of files that can be uploaded using the **File Attachment** button are added here. It also allows to add a new file format by clicking the **Add** button. Supported file formats are: audio, video, image, text or PDF. You can also delete or rearrange allowed file types using:
    - **Delete** - Tap or click to remove specific file types.
    - **Rearrange** - Tap or click and drag to rearrange the order of allowed file types. 

-   **File type error message** - This option allows you to enter an error message that is displayed when you upload the file formats other than those listed in the **Allowed file types** option.

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

-   **Short description** - A short description is a brief text explanation that provides additional information or clarification about the purpose of a specific form field. It helps the user understand what type of data should be entered into the field and can provide guidelines or examples to help ensure that the information entered is valid and meets the desired criteria. By default, short descriptions remain hidden. Enable the **Always show short description** option to display it below the component.

-   **Always show short description** - Enable the option to display the Short description below the component.

-   **Help text** - Help text refers to additional information or guidance that is provided to the user to assist them in filling out a form field correctly. It appears when the user clicks the help icon (i) placed next to the component. Help text provides more detailed information than a form field's label or placeholder text, and is designed to help the user understand the requirements or constraints of the field. It can also offer suggestions or examples to make filling out the form easier and more accurate.

### Accessibility Tab {#accessibility-tab}


![Accessibility tab](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

- **Text for screen readers** - Text for screen readers refers to additional text that is specifically intended to be read by assistive technologies, such as screen readers, used by visually impaired individuals. This text provides an audio description of the form field's purpose, and can include information about the field's title, description, name, and any relevant messages (Custom text). The screen reader text helps ensure that the form is accessible to all users, including those with visual impairments, and provides them with a complete understanding of the form field and its requirements. 

  - **Custom text**: Select this option to use the custom text for ARIA accessibility labels. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
  - **Description**: Select this option to use the description for ARIA accessibility labels.
  - **Title**: Select this option to use the title for ARIA accessibility labels.
  - **Name**: Select this option to use the name for ARIA accessibility labels.
  - **None**: Select this option if you do not want to add for ARIA accessibility labels.

## Design Dialog {#design-dialog} 

Design Dialog is used to define and manage CSS styles for the File attachment component.

### Styles Tab {#styles-tab}

The Adaptive Forms File Attachment Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/checkbox-style.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms File Attachment Core Component. 

- **Allowed Styles**: You can define styles by providing a name and the CSS class that represents the style. For example, you can create a style named "bold text" and provide the CSS class "font-weight: bold". You can use or apply these styles to an Adaptive Form in Adaptive Forms editor. To apply a style, in Adaptive Forms editor, select the component you want to apply the style to, navigate to the properties dialog, and select the desired style from the **Styles** drop-down list. If you need to update or modify the styles, simply return to the Design Dialog, update the styles in the styles tab, and save the changes.

### Custom Properties 

![Custom Properties Dialog](/help/adaptive-forms/assets/checkbox-customproperties.png)

Custom properties allows you to associate custom attributes (key-value pairs) to an Adaptive Form core component using the form template. The custom properties are reflected in the properties section of the headless rendition of the component. It allows creating dynamic form behavior that adapts based on the custom attributes values. For example, developers can design various renditions of a Headless Forms component for mobile, desktop, or web platforms, significantly enhancing the user experience across a wide array of devices.

- **Group Name**: You can provide a name to identify the custom property group. You can add, delete, or rearrange multiple custom property groups. After adding the custom property group, you can see the following options:

    - **Key-Value Pairs**: You can add multiple custom property names and custom property values by clicking the **Add** button for each custom property group.

    - **Delete**: Tap or click to delete the custom property name and custom property value.

    - **Rearrange**: Tap or click and drag to rearrange the order of the custom property name and custom property value.
<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}
