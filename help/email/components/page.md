---
title: Email Page Component
description: The Email Page component
role: Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
index: false
TQID: https://experienceleague.adobe.com/gfT1Y890ffKiJ61V72C3YIRiz2cEO9LvRU1gUaldG1A
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
    internal-label: Authoring
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
    internal-label: Editable templates
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
# Email Page Component {#email-page-component}

The Email Page Component is an extensible page component designed to work with the [template editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) and allows page header/footer and structure components to be assembled with the template editor, tailored for creating Adobe Campaign content.

## Usage {#usage}

The Email Page Component forms the basis of all pages designed with the Email Core Components and editable templates. By using the Email Page Component, headers, footers, and the structure of the page can be defined as a template using the other Email Core Components.

* Using the [design dialog,](#design-dialog) custom client-side libraries can be defined for the page. 
* Unlike other components which have an edit dialog accessible directly from the component, because the Email Page Component is the page itself, the [edit dialog](#edit-dialog) of the Email Page Component is the page properties window.

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Page Component is v1, which was introduced with release X of the Email Core Components in October 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|---|---|---|---|
|v1|Compatible|-|-|

For more information about Email Core Component versions and releases, see the document [Email Core Components Versions](/help/email/versions.md)

### Technical Details {#technical-details}

The latest technical documentation about the Page Component [can be found on GitHub.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Edit Dialog {#edit-dialog}

Because the component represents the entire page, settings that would normally be in an edit dialog are found in the [Page Properties](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) window.

### Cloud Services Tab {#cloud-services}

In order for the Email Core Components to be able to retrieve campaign variables and data, the page must be linked to an Adobe Campaign configuration. 

![Email Page Properties](/help/email/assets/email-page-properties.png)

Under **Cloud Service Configuration** heading, in the drop-down select **Add Configuration**.

Under **Adobe Campaign** heading, select the configuration for your integration with Adobe Campaign.

See the document [Using Email Core Components](/help/email/using.md) for more information about setting up the Email Core Components.

### Email Tab {#email-tab}

The Email tab defines properties of emails sent via Adobe Campaign based on the content of this page such as the email subject and plain text content.

![Email Page Properties](/help/email/assets/email-page-properties-email.png)

* **Subject** - The subject of the email sent by Adobe Campaign based on this page
  * Click the **Select Adobe Campaign Variable** icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
* **Pre-header**
  * Click the **Select Adobe Campaign Variable** icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
* **Plain text** - The plain text version of the email sent by Adobe Campaign
  * Click the **Select Adobe Campaign Variable** icon to open the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.
* **Reference Url**

## Design Dialog {#design-dialog}

Because the component represents the entire page, the design dialog is accessed via **Page Information -&gt; Page Policy** when editing the page template.

![Page Policy](/help/assets/page-policy.png)

### Properties Tab {#properties-tab}

Using the Page Design window, you can define the client libraries to be loaded as well as the web resources library for the page.

![Email Page Component design dialog](/help/email/assets/email-page-design.png)

* **Client Libraries** - This defines the client library categories to load. JavaScript is added at the body end and the CSS is added to the page head.
* **Client Libraries JavaScript Page Head** - This defines the JavaScript client library categories to load in the page head.
  * Categories defined here that are also present in the **Client Libraries** field will have JavaScript loaded in the page head instead of at body end.  
  * No CSS will be loaded unless the category is also present in the **Client Libraries** field.
* **Load JavaScript Libraries asynchronously** - If enabled, the custom JavaScript libraries will be loaded asynchronously.
* **Web Resources Client Library** - The client library category that is used to serve web resources such as favicons.
* **Skip to main content element selector** - Used as an accessibility feature to skip directly to the main content of the page

Libraries can be configured for both the **Client Libraries** and **Client Libraries JavaScript Page Head** fields as follows:

* To add a new field, click or tap the **Add** button below the fields.
* To remove a field, click or tap the trash can icon next to the field to be removed.
* To rearrange the load order, click or tap and drag the handle next to the field to be moved.

For more information about using client-side libraries, see [Using Client Side Libraries.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)

### Styles Tab {#styles-tab}

The Page Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
