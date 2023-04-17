---
title: Adaptive Forms Core Component - Form Container
description: Add an Adaptive Form to a Webpage.
role: Architect, Developer, Admin, User
exl-id: 8df7f862-4d59-4c3f-88dd-f0c937081f4f
---
# Form Container {#form-container-adaptive-forms-core-component}

Forms allow website visitors to interact with the website by providing valuable information, which can increase engagement and user satisfaction. An Adaptive Form Container in Adobe Experience Manager (AEM) Sites enables website owners to easily add forms to their pages. This helps facilitate communication between website visitors and the website owner or organization by providing a streamlined way for visitors to provide feedback, make inquiries, and complete other action

## Usage {#reasons-to-use-forms-container}

There are several reasons why a form may be added to a website:

*   **Data collection**: Forms can be used to collect data from website visitors for various purposes, such as market research, user behavior analysis and more.

*   **Lead generation**: A form can be used to gather information from potential customers, such as name and email address, to generate leads for sales and marketing efforts.

*   **E-commerce**: Forms can be used for online shopping, allowing customers to place orders and make payments through the website.

*   **Contact**: A contact form allows website visitors to easily reach out to the website owner or organization.

*   **Surveys and polls**: Forms can be used to gather feedback and opinions from website visitors through surveys and polls.

*   **Event registration**: Forms can be used for event registration, allowing website visitors to sign up for events or webinars.

*   **Subscriptions**: Forms can be used for website subscriptions, allowing visitors to sign up for a newsletter or other regular communications.

*   **User authentication**: Forms can be used for user authentication, allowing website visitors to create accounts and log in to access exclusive content or features.

*   **Increase conversion rate**: A well-designed form can increase the conversion rate by making it easy for users to complete a desired action, like purchasing a product or signing up for a service.


## Version and Compatibility {#version-and-compatibility}

The Adaptive Forms Accordion Core Component was released in Feb 2023 as part of the Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms or later. Here's a table showing all supported versions, AEM compatibility, and links to corresponding documentation:

|Component Version|AEM as a Cloud Service|AEM 6.5.16.0 Forms or later|
|---|---|---|
|v1|Compatible with<br>[release 2.0.4](/help/adaptive-forms/version.md) and later| Compatible with<br>[release 1.1.12](/help/adaptive-forms/version.md) and later but less than 2.0.0.|

For information on Core Component versions and releases, refer to the [Core Components Versions](/help/adaptive-forms/version.md) document.
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Container Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize your form container experience for visitors with the Configure Dialog. You can also define form container options with ease for a seamless user experience.

### Basic Tab {#basic-tab}

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **Prefill services** - This option allows the user to select a prefill service for retrieving data when the Adaptive Form is rendered. Learn more about [how to create and configure a prefill service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

*   **Client Library category** - The user can configure custom JavaScript library per Adaptive Form. It is recommended to keep only the reusable functions in the library, which have dependency on jquery and underscore.js third-party libraries.

### Submission Tab {#submission-tab}

![Submission tab](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Users can configure different actions for an Adaptive Form submissions. 

* **Redirect URL/Path** - This option allows user to configure a page for each form, to which the form users are redirected after submitting an Adaptive Form. Click here for more information on [how to configure redirect pages](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![Show Message tab](/help/adaptive-forms/assets/formconatiner_showmessage.png)

*   **Show Message** - This option allows users to add a message that is displayed when the Adaptive Form is successfully submitted. The predefined text is included in the dialog box and it can be modified by the user. The Show Message dialog supports rich text formatting tools that allow users to format the added text.

*   **Submit Action** - A Submit Action is triggered when a user clicks the Submit button on an Adaptive Form. The users can select Submit Actions from the drop-down list that are supported out of the box. Learn how to [configure a Submit Action in the Submission tab](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).
