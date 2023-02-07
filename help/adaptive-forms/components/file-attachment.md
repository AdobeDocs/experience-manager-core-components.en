---
title: Adaptive Forms Core Component - File attachment
description: Using or customizing the Adaptive Forms file attachment Core Component.
role: Architect, Developer, Admin, User
---

# File attachment {#file-attachment-adaptive-forms-core-component}

A file attachment component in an Adaptive Form allows users to select and upload files from their local computer or device. The file attachment component can be configured to allow specific file types, size limits and multiple attachments.

**Example**

![](/help/adaptive-forms/assets/upload-image.png)


## Usage {#reasons-to-use-file-attachment}

There are several reasons why it is beneficial to include a file attachment component in an Adaptive form, including:

*   **Collecting additional information**: A file attachment component allows users to upload documents, images, videos, or other types of files as part of the form submission. This can be useful for collecting additional information such as resumes, portfolios, or supporting documentation.

*   **Easy sharing of large files**: File attachment component enables users to share large files easily, without having to rely on external file-sharing services.

*   **Convenience**: File attachment component allows users to upload files from their local computer, without having to navigate away from the form or use other tools.

*   **Validation**: File attachment component can be configured to validate the type, size, and number of files that are allowed to be uploaded.

*   **Security**: File attachments can be encrypted and secured to protect sensitive information.

*   **Data analysis**: File attachment component can be used to collect data from various sources and analyze it, or use it as input for further processing.

*   **Customization**: File attachment component can be customized to suit the specific needs of the form, such as adding an image preview, renaming the file before uploading, or adding a progress bar to show the upload progress.

*   **User experience**: File attachment component can be used to make the form more user-friendly by providing a clear and intuitive way for users to upload files.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms File Attachment Core Component was released in Feb 2023 as part of the Core Components 2.0.4. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|
|--- |--- |---|---|
|v1|Compatible with<br>[release 2.0.4](/help/versions.md) and later|Compatible|Compatible|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms File Attachment Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your file attachment experience for visitors with the Configure Dialog. You can also define file attachment options with ease for a seamless user experience.

### Basic Tab {#basic-tab} 

![Basic tab](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Name** - The name uniquely identifies the component in the rule editor.Special characters and spaces are not allowed in the name strings.

* **Title** - Title is a string that appears at the top of a component in an Adaptive Form. Title uniquely identifies the component in the tree structure of an Adaptive Form. If you do not add a title, the name of the component is displayed instead of the title text.

* **Hide Title** - Select this option to hide title of the component type in an Adaptive Form.

* **Button title** - This option is used to set the label of the button  displayed on the Adaptive Form.

* **Bind Reference** - This option allows you to link an Adaptive Form field to the schema. When user enters any value in a linked field of an Adaptive Form that value also appears in the associated schema.

* **Hide Component** - Select this option if you do not want to make the component type visible in an Adaptive Form. The component remains active in edit mode. 
* **Disable Component** - Select this option if you want to disable the component in an Adaptive Form. The component remains active in edit mode. 
* **Read-only** - Select this option if you want to make the component type immutable in an Adaptive Form. The component remains active in edit mode.
* **Allow multiple attachments** - Select this option to include multiple attachments.

### Validation Tab {#validation-tab}

![Validation tab](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Required** - When this option is selected, the component type is displayed in an Adaptive Form. In the **Basic** tab, the **Hide Component** and **Disable Component** become non-clickable when this option is selected.

* **Error Message** -The option allows to enter a message to be displayed if the required fields are left blank.

* **Script Validation Message** - This option allows to enter a message to be displayed if the script validation fails on an Adaptive Form submission.

* **Minimum files error message** - This option is used to enter an error message if you upload files lesser than the specified minimum number of files.

* **Maximum files error message** - This option is used to enter an error message if you upload files greater than the specified maximum number of files.

* **Maximum file size (MB)** -

 This option allows to specify a maximum file size. File sizes are specified in MB. 

* **Maximum file size error message** - This option is used to display the error message, when more than maximum size files are uploaded. 

* **Allowed file types** - Various types of files that can be uploaded using the **File Attachment** button are added here. It also allows to add a new file format by clicking the **Add** button. Supported file formats are:
    * **audio/*** - Supports all  formats of audio files such as mp3, wav.
    * **video/*** - Supports all  formats of video files such as mp4, avi, wmv.
    * **image/*** - Supports all  formats of image files such as png, jpg, jpeg.
    * **text/*** - Supports all  formats of text files such as doc, docx, txt.
    * **application/pdf** - Supports PDF format for document files.

    * **Delete** - Tap or click to remove specific file types.
    * **Rearrange** - Tap or click and drag to rearrange the order of allowed file types. 

* **File type error message** - This option allows to enter a error message that is displayed if a different file is uploaded than what is listed in the **Allowed file types** options.

### Help Content Tab {#help-content-tab}

![Help Content tab](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Short Description** - A short description provides enough context for the user to understand what the checkbox options convey. The entered text appears as a tool tip when the user hovers the mouse pointer over the component type. You can also format the text that appears in the short description.

* **Always show short description** - Select this option to display a short description even if the user does not hover over a component type.

* **Help Text** - Help text consists of information or error messages about the component type. Help text is available by clicking the icon that appears above the component type. Click the icon to display help text above the component type.You can also format the text that appears in the help section.

![Accessibility tab](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

On the **Accessibility** tab, values are set for [ARIA accessibility](https://www.w3.org/WAI/standards-guidelines/aria/) labels for the component. Various options are available for using the text for screen reader:
* **Custom text**: Select this option to use the custom text for ARIA accessibility labels. Selecting this option displays the Custom Text dialog box. You can add relevant information in the Custom Text dialog box.
* **Description**: Select this option to use the description for ARIA accessibility labels.
* **Title**: Select this option to use the title for ARIA accessibility labels.
* **Name**: Select this option to use the name for ARIA accessibility labels.
* **None**: Select this option if you do not want to add for ARIA accessibility labels.


## Design Dialog {#design-dialog}

