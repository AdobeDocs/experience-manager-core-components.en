---
title: Form Hidden Component
description: The Core Component Form Hidden component allows for the display of a hidden field.
role: Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
TQID: https://experienceleague.adobe.com/4A6TDfa-zTap73hcgFA-fbjbKqd3dF11Zgs-eEypE0Y
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
---
# Form Hidden Component{#form-hidden-component}

The Core Component Form Hidden component allows for the display of a hidden field.

## Usage {#usage}

The Core Component Form Hidden Component allows for the creation of hidden fields to pass information about the current page back to AEM and is intended to be used along with the [form container component](form-container.md).

The field properties can be defined by the content editor in the [configure dialog](form-hidden.md).

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Hidden Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|--- |--- |--- |---|---|
|v2|Compatible with<br>[release 2.17.4](/help/versions.md) and prior|Compatible|Compatible|Compatible|
|[v1](/help/components/v1/form-hidden-v1.md)|Compatible|Compatible|-|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Form Hidden Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_hidden).

### Technical Details {#technical-details}

The latest technical documentation about the Form Hidden Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the parameters of the hidden field.

![Form hidden edit dialog](/help/assets/form-hidden-edit.png)

* **Name** - The name of the field, which is submitted with the form data
* **Value** - The value of the field, which is submitted with the form data
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

Because the Form Hidden component normally has no visible attributes, the component's placeholder in the editor displays the **Name** and **Value** field values if they are assigned in order to help the author identify the appropriate Form Hidden component.

![Example of Form Hidden Component](/help/assets/form-hidden-example.png)

## Design Dialog {#design-dialog}

### Styles Tab {#styles-tab}

The Form Hidden Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
