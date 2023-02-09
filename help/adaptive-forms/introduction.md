---
title: AEM Adaptive Forms Core Components Introduction
description: Create compelling enrollment experiences (forms) using the flexibility of the Adaptive Forms Core Components and deliver it with the power of Adobe Experience Manager.
role: Architect, Developer, Admin, User
---

# Adaptive Forms Core Components Introduction {#adaptive-forms-core-components-introduction}

Using the Adaptive Forms Core Components in Adobe Experience Manager, you can create compelling enrollment experiences by utilizing the flexibility and customization options available. 

## Core Components  {#overview}

In Adobe Experience Manager (AEM), components are the building blocks used to create pages and forms. They provide a simple and powerful way for authors to create and manage content, while also providing developers with the flexibility and extensibility needed to create custom components.

The are designed to speed up development time and reduce maintenance costs for websites and forms, be flexible and can be easily customized to match the specific needs of a website and form.

The Core Components are also designed to be responsive and support a wide range of devices, including desktops, tablets, and smartphones. They also adhere to the latest web standards and best practices, making them a robust and reliable solution for creating web content.

Overall, the Core Components are an essential tool for creating and managing web content in AEM, providing a powerful and flexible solution that can help to reduce development time and maintenance costs, while also providing a great user experience to the website visitors. 

## Adaptive Forms Core Components

The Adaptive Forms Core Components are a set of 24 open-source, BEM-compliant components that are built on the foundation of the Adobe Experience Manager WCM Core Components. They are specifically designed to be used for creating Adaptive Forms, which are forms that adapt to the device, browser and screen size of the user.

These components can be used to create exceptional data capture and enrollment experiences by providing a wide range of form field options, including text fields, checkboxes, drop-down menus, and more. They also include features like validation, conditional logic, and responsive design, which can be used to create forms that are user-friendly and easy to use.

Additionally, as these components are open-source, developers have the ability to easily customize and extend the components to match the specific needs of their organization. And, These components are built on BEM methodology which ensures that they are scalable and maintainable.

![](assets/sample-adaptive-form.png)

## Features {#features}

|||
|---|---|
|Production-Ready| The Adaptive Forms Core Components are 24 robust WCM components.|
|Cloud-Ready| Available for  [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html).|
|Versatile| The components represent generic concepts with which the Forms authors can assemble nearly any layout.|
|Configurable| Template-level [content policies](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html#content-policies) define which features are allowed to use or not use.|
|Accessible| They comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)), and  text for assistive technologies such as screen readers.|
|Themeable| The components implement the [Style System](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/).|
|Customizable| Several patterns allow easy customization, from adjusting the HTML to advanced functionality reuse.|
|Versioning| The [versioning policy](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) ensures that the Core Components won't break your site when improving things that might impact you.|
|Open Sourced| If something is not as it should, contribute your improvement.|

## Benefits {#benefits}

Data capture experiences are crucial for lead generation and enrollment, and the Adaptive Forms Core Components provide a powerful solution for creating forms that are optimized for data capture. Some of the reasons to use Core Components to create these experiences over foundation components: 

*   **Availability on GitHub and comprehensive documentation**: The AEM Adaptive Forms Core Components are open-source and available on GitHub, along with comprehensive documentation. This makes it easier for developers to understand the components and how they work, as well as contribute to their development. The aemcomponents.dev website is also a valuable resource, where developers can see the components in action and access detailed documentation.

*   **BEM Model for Styling**: The Core Components follow the BEM (Block Element Modifier) model for styling, which is a well-established and widely-used methodology for organizing CSS. This makes it easier for developers to understand how the styles are organized and how to modify them to fit their specific needs.

*   **No Dependency on Third-Party Libraries**: One of the advantages of the Core Components is that they have no dependency on third-party JavaScript libraries, including JQuery and Underscore. This makes the components faster and more lightweight, as well as easier to integrate into an existing AEM implementation.

*   **Focus on Performance and Accessibility**: The Core Components are built with performance and accessibility in mind, which is reflected in their high Google Lighthouse and web vitals scores. This makes it easier for developers to create accessible and high-performing web pages, which is increasingly important in today's digital landscape.

*   **Form Components in Sites 30 Template and Themes**: The Core Components provide support for form components in the Sites 30 template and themes, making it easier for developers to create and customize forms within AEM.

*   **Easier to Style**: The Core Components are easier to style than their foundation component counterparts. The theme creation process is similar to Sites, with the ability to inherit the same theme/CSS from the parent Sites page. Additionally, the BEM model for styling makes it easier to understand and modify the styles.

*   **Accessibility**: Adaptive Forms Core Components support accessibility standards and guidelines, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->
    
 

## Requirements {#requirements}

The Adaptive Forms Core Components have the following requirements.

|AEM|AEM Forms add-on|Core Components|
|---|---|---|
|AEM as a Cloud Service|Forms - Digital Enrollment|[Release 2.20.8](/help/versions.md)+|


## Adaptive Forms Core Components {#components}

The current version of the Adaptive Forms Core Components features the following components.

* Accordion
* Button
* Check Box Group
* Date Picker
* Drop-down list
* Email-input
* Form Container
* File Attachment
* Footer
* Header
* Horizontal Tabs
* Image
* Number Input
* Panel Container
* Radio Button
* Reset Button
* Submit Button
* Telephone input
* Text Input
* Text
* Title
* Wizard

