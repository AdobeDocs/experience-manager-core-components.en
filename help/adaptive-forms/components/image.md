---
title: Adaptive Forms Core Component - Image
description: Using or customizing the Adaptive Forms Image Core Component.
role: Architect, Developer, Admin, User
---

# Image {#image-adaptive-forms-core-component}

An Image component in an Adaptive Form is a way to include images in a form. These images can be used to enhance the overall design of the form, provide additional information, or serve as a visual aid to help users understand the form's purpose. The image component can be used to add a logo, a photo, or a graphic in the form.

For accessibility, it is important to specify **Alternate text** to the image to provide a short, descriptive text alternative for the image, that describes the image to users who cannot see it.


**Example**

![](/help/adaptive-forms/assets/image.png)


## Usage {#reasons-to-use-image-in-a-form}

There are several reasons why it is beneficial to include an Image component in an Adaptive Form, including:

*   **Branding**: An image can be used to display the logo or name of the organization that created the form, helping to establish brand recognition and credibility.

*   **Visual Aids**: An image can help to provide an additional level of information to users, by serving as a visual aid to help users understand the form's purpose.

*   **Decoration**: An image can be used to enhance the overall design of the form and make it more visually appealing.

*   **User Experience**: An image can be used to make the form more user-friendly by providing a clear and intuitive way for users to access and fill in form fields.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Image Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Image Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your image experience for visitors with the Configure Dialog. You can also define image options with ease for a seamless user experience.

![Properties tab](/help/adaptive-forms/assets/image_properties.png)

* **Name** - The name uniquely identifies the component in the rule editor.Special characters and spaces are not allowed in the name strings.

* **Title** - Title is a string that appears at the top of a component in an Adaptive Form. Title uniquely identifies the component in the tree structure of an Adaptive Form. If you do not add a title, the name of the component is displayed instead of the title text.

* **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record.

* **Description** - This option is used  The entered text appears as a tool tip when the user hovers the mouse pointer over the component type. 

* **Drop an asset here or browse for a file to upload** - This option drop assets with mouse drag and drop. You can also upload a file using the Browse button.
After adding an image, three buttons appear at the bottom of the image:
    * **Edit** - Use this option to edit the  image.
    * **Clear** - Use this option to remove the image.
    * **Pick** - Use this option to select the image from Assets.

* **Alternate text** - This option is used to enter the text to be displayed when the image is not rendered on the Sites.

* **Hide Component** - Select this option if you do not want to make the component type visible in an Adaptive Form. The component remains active in edit mode. 

* **Read-only** - Select this option if you want to make the component type immutable in an Adaptive Form. The component remains active in edit mode.



## Design Dialog {#design-dialog}

