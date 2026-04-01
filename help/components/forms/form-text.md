---
title: Form Text Component
description: The Core Component Form Text component allows the entry of form text for submission.
role: Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
TQID: https://experienceleague.adobe.com/9js-R-LzxStEKmgs59UvZBz-htCWyIx-PQIjpIKJAqc
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
# Form Text Component{#form-text-component}

The Core Component Form Text component allows the entry of form text for submission.

## Usage {#usage}

The Form Text component allows for the submission of different types of text and is intended to be used along with the [form container component](form-container.md). The type of text validation, labels, and help messages can be defined by the content editor in the [configure dialog](#configure-dialog).

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Text Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.4|AEM 6.5|AEM 6.5 LTS|AEM as a Cloud Service|
|--- |--- |--- |---|---|
|v2|Compatible with<br>[release 2.17.4](/help/versions.md) and prior|Compatible|Compatible|Compatible|
|[v1](/help/components/v1/form-text-v1.md)|Compatible|Compatible|-|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](/help/versions.md).

## Sample Component Output {#sample-component-output}

To experience the Form Text Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_form_text).

### Technical Details {#technical-details}

The latest technical documentation about the Form Text Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the type of text to be input as well as default values and labels.

### Properties Tab {#properties-tab}

![Properties tab](/help/assets/form-text-edit-properties.png)

* **Constraint** - The type of text to be input and will be validated against
  * **Text**
  * **Text Area**
  * **Email**
  * **Tel**
  * **Date**
  * **Number**
  * **Password**
* **Text lines** - Number of lines to be displayed in the text area (only displayed when **Constraint** is set to **Text Area**)
* **Label** - The label that will be displayed for the field
* **Hide the label from being displayed** - Needed if the label is required only for accessibility purposes and does not impart any additional visual information about the field
* **Element Name** - The name of the field that is submitted with the form data
* **Value** - Default value that is prepopulated in the field
* **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
  * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
  * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
  * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

### About Tab {#about-tab}

![About tab](/help/assets/form-text-edit-about.png)

* **Help Message** - A hint to the user of what can be entered in the field
* **Display help message as placeholder** - To display the help message inside the form input when it is empty and not focused

### Constraints Tab {#constraints-tab}

![Constraints tab](/help/assets/form-text-edit-constraints.png)

* **Constraint Message**
  * Message displayed as tooltip when submitting the form if the value does not validate the Type chosen
  * Not displayed for **Text** and **Text Area** constraint types
* **Required** - If selected the user must fill in a value before submitting the form
  * **Required Message** - Message displayed as a tooltip if the field is left empty
* **Make read only** - If selected the user cannot modify the value of the field

## Design Dialog {#design-dialog}

### Styles Tab {#styles-tab}

The Form Text Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
