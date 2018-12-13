---
title: Form Container Component
seo-title: Form Container Component
description: null
seo-description: The Core Component Form Container Component allows for the creation of simple submission forms.
uuid: 9d556daf-3fe7-4b2a-b5ae-6926acb267a9
contentOwner: User
content-type: reference
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 3d33fe60-a0ac-4ff2-a865-d600b5448aeb
disttype: dist5
gnavtheme: light
groupsectionnavitems: no
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
---

# Form Container Component{#form-container-component}

The Core Component Form Container Component allows for the creation of simple submission forms.

## Usage {#usage}

The form Container Component enables the building of simple information submission forms and features by supporting simple WCM forms and by using a nested structure to allow additional form components.

By using the [configure dialog](../using/form-container.md#main-pars_title) the content editor can define the action triggered by form submission, where the submitted content should be stored, and whether a workflow should be triggered. The template author can use the [design dialog](../using/form-container.md#main-pars_title_1995166862) to define the allowed components and their mappings similar to the design dialog for the [standard layout container in the template editor](/content/help/en/experience-manager/6-3/sites/authoring/using/templates#main-pars_title_1754153843).

>[!NOTE]
>
>The core components Form Container Component only supports the use of core components form components (button, text, hidden, etc.). Using [foundation components](/content/help/en/experience-manager/6-4/sites/authoring/using/default-components-foundation#main-pars_title_14) form components within the core components form container (and vice versa) is not supported.

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Container Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody>
  <tr>
   <td>Component Version<br /> </td> 
   <td>AEM 6.3</td> 
   <td>AEM 6.4</td> 
  </tr>
  <tr>
   <td>v2<br /> </td> 
   <td>Compatible</td> 
   <td>Compatible</td> 
  </tr>
  <tr>
   <td><a href="../using/form-container-v1.md">v1</a></td> 
   <td>Compatible<a href="../using/list-v1.md"></a></td> 
   <td>Compatible</td> 
  </tr>
 </tbody>
</table>

For more information about Core Component versions and releases, see the document [Core Components Versions](../using/versions.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define what actions are taken when the component is submitted. 

![](assets/screen_shot_2018-01-12at122046.png)

Depending on the selected **Action Type**, the available options within the container will change. The available action types are:

* [Mail](../using/form-container.md#main-pars_title_966511656)
* [Store Content](../using/form-container.md#main-pars_title_2065985840)
* [Submit Order](../using/form-container.md#main-pars_title_686874527)
* [Update Order](../using/form-container.md#main-pars_title_410109286)

Regardless of the type, there are [general settings](../using/form-container.md#main-pars_title_375403046) that apply to each action.

### Mail {#mail}

When the form is submitted, the mail action type will send an email to designated recipients.

![](assets/screen_shot_2018-01-12at122554.png)

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

![](assets/screen_shot_2018-01-12at122538.png)

* **Content Path** - Content repository path where submitted content is stored
* **View Data** - Tap or click to view stored submitted data as JSON
* **Start Workflow** - Configure to start a workflow with the stored content as payload upon form submission

### Submit Order {#submit-order}

When the form is submitted, the order will be submitted.

![](assets/chlimage_1.png)

### Update Order {#update-order}

When the form is submitted, the order will be updated.

![](assets/chlimage_1.png)

### General Settings {#general-settings}

Regardless of the action type selected, a thank you page can always be defined.

![](assets/chlimage_1.png)

The user will be redirected to the specified page after completion of the form submission.

* Use the Selection Dialog to select a resource within AEM.
* If the thank you page is not in AEM, specify the absolute URL. Non-absolute URLs will be interpreted relative to AEM.
* Leave blank to redisplay the form after submission.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the allowed components and their mappings for the container similar to the design dialog for the [standard layout container in the template editor](/content/help/en/experience-manager/6-3/sites/authoring/using/templates#main-pars_title_1754153843).

## Technical Details {#technical-details}

The latest technical documentation about the Form Container Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](../using/developing.md). 
