---
title: Form Container Component
description: The Core Component Form Container Component allows for the creation of simple submission forms.
role: Architect, Developer, Admin, User
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
---
# Form Container Component {#form-container-component}

The Core Component Form Container Component allows for the creation of simple submission forms.

## Usage {#usage}

The form Container Component enables the building of simple information submission forms and features by supporting simple WCM forms and by using a nested structure to allow additional form components.

By using the [configure dialog](#configure-dialog) the content editor can define the action triggered by form submission, the URl that should handle the submission, and whether a workflow should be triggered. The template author can use the [design dialog](#design-dialog) to define the allowed components and their mappings similar to the design dialog for the [standard layout container in the template editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>The core components Form Container Component only supports the use of core components form components (button, text, hidden, etc.). Using [foundation components](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html) form components within the core components form container (and vice versa) is not supported.

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Container Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM as a Cloud Service|
|--- |--- |--- |---|
|v2|Compatible with<br>[release 2.17.4](/help/versions.md) and prior|Compatible|Compatible|
|[v1](/help/components/v1/form-container-v1.md)|Compatible|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Form Container Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_container).

## Technical Details {#technical-details}

The latest technical documentation about the Form Container Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define what actions are taken when the component is submitted.

Depending on the selected **Action Type**, the available options within the container will change. The available action types are:

* [Post Form Data](#post-data)
* [Mail](#mail)
* [Store Content](#store-content)

Regardless of the type, there are [general settings](#general-settings) that apply to each action.

### Post Form Data {#post-data}

When the form is submitted, the post form data action type will pass the submitted data on to a third party as JSON for processing.

![Post Form Data options in Form Container Component's edit dialog](/help/assets/form-container-edit-post.png)

* **Endpoint** - The fully-qualified HTTPS service that will process the data
* **Error Message** - Message to display if the submission is not successful

>[!TIP]
>There are additional timeout options which a system administrator can adjust to handle the processing of forwarded form data. [See the technical documentation on GitHub for more information.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Mail {#mail}

When the form is submitted, the mail action type will send an email to designated recipients.

![Mail options in Form Container Component's edit dialog](/help/assets/form-container-edit-mail.png)

* **Subject** - The subject of the email that will be sent on form submission
* **From** - The from email address of the email that will be send on form submission
* **To** - The addresses of the recipients who will receive an email upon form submission
  * Tap or click the **Add** button to add additional addresses
  * Tap or click the **Delete** button to remove an email address
* **CC** - The addresses of recipients who will receive a carbon copy the email sent upon form submission
  * Tap or click the **Add** button to add additional addresses
  * Tap or click the **Delete** button to remove an email address

### Store Content {#store-content}

When the form is submitted, the content of the form will be stored in a designated repository location.

![Store content options in Form Container's edit dialog](/help/assets/form-container-edit-store.png)

* **Content Path** - Content repository path where submitted content is stored
* **View Data** - Tap or click to view stored submitted data as JSON
* **Start Workflow** - Configure to start a workflow with the stored content as payload upon form submission

>[!NOTE]
>
>In order to make the management of user-data simpler and to enforce separation of concerns, it is generally not recommended to store user-generated content within the repository.
>
>Instead use the [Post Form Data](#post-data) action type to pass user content on to a dedicated service provider.

### General Settings {#general-settings}

Regardless of the action type selected, a thank you page can always be defined.

![General options in Form Container Component's edit dialog](/help/assets/form-container-edit-general.png)

* **Thank you page** - The user will be redirected to the specified page after completion of the form submission.
  * Use the Selection Dialog to select a resource within AEM.
  * If the thank you page is not in AEM, specify the absolute URL. Non-absolute URLs will be interpreted relative to AEM.
  * Leave blank to redisplay the form after submission.
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the allowed components and their mappings for the container similar to the design dialog for the [standard layout container in the template editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Styles Tab {#styles-tab}

The Form Container Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
