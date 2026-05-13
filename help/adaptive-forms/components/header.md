---
title: Adaptive Forms Core Component - Header
description: Using or customizing the Adaptive Forms Header Core Component.
role: Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
TQID: https://experienceleague.adobe.com/uwm7dFay8faGjpkIoygSbw7vUexD-82yPjjzjwtabjE
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
    internal-label: Accessibility
---
# Header {#header-adaptive-forms-core-component}

A Header component in an Adaptive Form is a section at the top of the form that typically includes the title, logo, or name of the form. The header can also include other information such as a brief description of the form's purpose, the name of the organization that created the form, or contact information for help with the form. The header is used to give users an overview of the form and provide context for the information they are about to fill out. It is used to help users understand the purpose of the form and how to fill it out correctly.

{{traditional-aem}}

**Example**

![example](/help/adaptive-forms/assets/header.png)

## Usage {#reasons-to-use-header}

-   **Branding**: A header can be used to display the logo or name of the organization that created the form, helping to establish brand recognition and credibility.

-   **Context**: A header can provide a brief description of the form's purpose, helping users understand the context in which the form is being used.

-   **Navigation**: A header can include links or buttons that allow users to navigate to other parts of the website or application.

-   **Information**: A header can include contact information or links to help resources, making it easier for users to get assistance if they need it.

-   **User experience**: A header can be used to make the form more user-friendly by providing a clear and intuitive way for users to access and fill in form fields.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms header Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.


<!--
## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). 
-->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Header Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your header experience for visitors with the Configure Dialog. You can also define header options with ease for a seamless user experience.

### Image Tab {#image-tab}

This part of the header contains the header title and image.

![Imagetab](/help/adaptive-forms/assets/header_image.png)

-   **Image Asset** - This option allows to drop an asset such as image with mouse drag and drop. You can also upload a file from a local file system using the **Browse** button. After adding an image, three buttons appear at the bottom of the image. After adding an image, three buttons appear at the bottom of the image:
    - **Edit** - Tap or click **Edit** to manage the renditions of the asset in the Assets Editor.
    - **Clear** - Tap or click **Clear** to de-select the currently selected image.
    - **Pick** - Tap or click **Pick**  option to select another image from Assets folder.

-   **Title** - This option is used to add the heading to the header. The predefined text is included in the dialog box, and it can be modified by the user.
-   **Link to** - You can link the heading to the folder using the **Browse** icon. 
-   **Description** - A description is a brief text explanation that provides additional information or clarification about the purpose of a specific image. 
-   **Size (px)** - It helps in adjusting the length and width of the image by increasing or decreasing the pixels. 

![accessibilitytab](/help/adaptive-forms/assets/header_accessibility.png)

-   **Alternative Text** - This option is used to enter the text that provides a short and descriptive text alternative for the image, that describes the image to visually impaired users.

-   **Image is decorative** - Check if the image should be ignored by assistive technology and therefore does not require an alternative text. This applies to decorative images only.

### Text tab {#text-tab}

This section allows to enter the text to be included in the header.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}
