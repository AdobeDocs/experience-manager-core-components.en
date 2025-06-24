---
title: Adaptive Forms Core Component - Footer
description: Using or customizing the Adaptive Forms Footer Core Component.
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
---

# Footer {#footer-adaptive-forms-core-component}

A footer component in an Adaptive Form is an area that typically appears at the bottom of the form and contains information such as a copyright notice, links to related resources, or contact information. A footer can provide additional information, such as the date of the last update, which can be beneficial for users with accessibility needs.

{{traditional-aem}}

**Example**

![example](/help/adaptive-forms/assets/footer.png)

## Usage {#reasons-to-use-footer}

There are several reasons why it is beneficial to include a footer component in a form, including:

-   **Legal requirements**: Some forms may be required to include a disclaimer, copyright notice, or other legal information. A footer is a convenient place to include this information.

-   **Navigation**: A footer can provide links to other important pages on the website, such as a privacy policy, terms of service, or contact page.

-   **Branding**: A footer can be used to include a logo or other branding elements, helping to reinforce the identity of the organization or website.

-   **Consistency**: A footer provides consistency in the design and layout of the form, making it more intuitive and easy for users to navigate.

-   **Additional context**: A footer can provide additional context to the form, such as a text describing the form or a link to related resources, making the form more informative and user-friendly.

## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Footer Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Footer Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).


## Configure Dialog {#configure-dialog}

You can easily customize your footer experience for visitors with the Configure Dialog. You can also define footer options with ease for a seamless user experience.

![Properties tab](/help/adaptive-forms/assets/footer_propertiestab.png)

-   **Edit Dialog box**
The edit dialog provides standard rich text formatting tools that allow the user to create text for the footer.

-   **Bold** - This option applies bold formatting to selected text or boldly   format text entered after the cursor. `Ctrl+B` is a keyboard shortcut.

-   **Italic** - This option applies italicized formatting to selected text or   italicize text entered after the cursor. `Ctrl+I` is a keyboard shortcut.

![Bullet Options](/help/adaptive-forms/assets/footer_bullet.png)


-   **Bullet**

    -   **Bullet icon** - It formats the selected text as a bulleted list or begin the insertion of a bulleted list after the cursor. To end a bulleted list, tap or click the Bullet button again or enter two carriage returns.

    -   **Numbered list icon** - It formats the selected text as a numbered list or begin the insertion of a numbered list after the cursor. To end a numbered list, tap or click the Numbered button again or enter two carriage returns.

    -   **Outdent icon** - It decreases the indentation level of the selected text or text entered after the cursor. Only active if the selected text or position of the cursor is already indented.
    
    -   **Indent icon** - It increases the indentation level of the selected text or text entered after the cursor.

 ![Hyperlink Options](/help/adaptive-forms/assets/footer_link.png)

-   **Hyperlink**

    -   **Path** - Enter the path
        1. Use the Open Selection Dialog to choose a path in AEM.
        1. If the link is not within AEM, enter the absolute URL.
        1. Non-absolute paths are interpreted as relative to AEM.
    
    -   **Alternative text** - Enter alternative descriptive text for the link.

    -   **Target** - Select link behavior
        - Target
        - Same Tab
        - New Tab
        - Parent Frame
        - Top Frame

    -   **Unlink icon** - This option removes a link already applied to the selected text. This option is only active if the link is already selected.

    -   **Paragraph format icon** - This option allows you to apply paragraph formatting to the selected text. It also helps you to format the text inserted after the cursor. It defines the heading level of the title.

-   **ID**: This option allows to control the unique identifier of the component in the HTML and in the Data Layer.

    - If left blank, a unique ID is automatically * generated for you and can be found by inspecting the resulting page.
    - If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    - Changing the ID can have an impact on CSS, JS and Data Layer tracking.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}
