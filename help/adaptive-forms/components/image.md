---
title: Adaptive Forms Core Component - Image
description: Using or customizing the Adaptive Forms Image Core Component.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
---
# Image component{#image-adaptive-forms-core-component}

An Image component in an Adaptive Form is a way to include images in a form. These images can be used to enhance the overall design of the form, provide additional information, or serve as a visual aid to help users understand the form's purpose. The image component can be used to add a logo, a photo, or a graphic in the form.

For accessibility, it is important to specify **Alternate text** to the image to provide a short, descriptive text alternative for the image, that describes the image to users who cannot see it.

**Example**

![example](/help/adaptive-forms/assets/image.png)


## Usage {#reasons-to-use-image-in-a-form}

There are several reasons why it is beneficial to include an Image component in an Adaptive Form, including:

-   **Branding**: An image can be used to display the logo or name of the organization that created the form, helping to establish brand recognition and credibility.

-   **Visual Aids**: An image can help to provide an extra level of information to users, by serving as a visual aid to help users understand the form's purpose.

-   **Decoration**: An image can be used to enhance the overall design of the form and make it more visually appealing.

-   **User Experience**: An image can be used to make the form more user-friendly by providing a clear and intuitive way for users to access and fill in form fields.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Image Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Image Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).


## Configure Dialog {#configure-dialog}

You can easily customize your image experience for visitors with the Configure Dialog. You can also define image options with ease for a seamless user experience.

![Properties tab](/help/adaptive-forms/assets/image_properties.png)

-   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

-   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.

- **Mark as Unbound Form Element**: Select the option to configure a form field not linked to any schema. This option allows you to save data without updating the data source. It also enables you to handle data in a custom way, separate from standard database integration.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enable you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

-   **Description** - A description is a brief text explanation that provides additional information or clarification about the purpose of a specific image. 

-   **Drop an asset here or browse for a file to upload** - This option allows to drop an asset such as image with mouse drag and drop. You can also upload a file from a local file system using the **Browse** button. After adding an image, three buttons appear at the bottom of the image:
    - **Edit** - Tap or click **Edit** to manage the renditions of the asset in the Assets Editor.
    - **Clear** - Tap or click **Clear** to de-select the currently selected image.
    - **Pick** - Tap or click **Pick**  option to select another image from Assets folder.

-   **Alternate text** - This option is used to enter the text that provides a short and descriptive text alternative for the image, that describes the image to visually impaired users.

-   **Hide Component** - Select the option to hide the component from the form. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor. This is useful when you need to store information that doesn't need to be seen or directly changed by the user. 

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-->

## Design Dialog {#design-dialog}

Design Dialog is used to define and manage CSS styles for the Image component.

### Styles Tab {#styles-tab}

The tab is used to define and manage CSS styles for a component. The Adaptive Forms Image Core Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

![Design Dialog](/help/adaptive-forms/assets/checkbox-style.png)

- **Default CSS Classes**: You can provide a default CSS class for the Adaptive Forms Image Core Component. 

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